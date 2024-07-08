# Arduino and Servo Motor Circuit Setup
## Introduction:
This report describes the setup of a circuit that uses an Arduino Uno to control six servo motors. The circuit includes the necessary connections for power, ground, and signal lines, ensuring proper operation and control of each servo motor.

## Components:
* Arduino Uno
* Breadboard
* 6 Servo Motors
* Wires
  
## Simulation:
Circuit Digram: 

![image](https://github.com/nswtnw/Task2_servo-motors/assets/173661012/f5356df0-311b-406d-a7c8-f70c18da3de1)

## Step to Step the Circuit:
1. Arduino Setup:
   Place the Ardunio Uno on and ensure it is properly powered via USB or an external power source>
2. Breadboard:
   Place the breadboard beside the Arduino Uno to facilitate easy connections between the two.
3. Power and Ground Connections:
   * Connect the 5V pin on the ardunio to the positive power rail on the breadboard using a red wire.
   * Connect the GND pin on the arduino to the ground rail on the breadboard using a black wire.
4. Servo Motor Connections:
* Servo 1:
   * Connect the red (VCC) wire of the first servo motor to the positive power rail on the breadboard.
   * Connect the black (GND) wire of the first servo motor to the ground rail on the breadboard.
   * Connect the orange (Signal) wire of the first servo motor to digital pin 3 on the Arduino.
* Servo 2:
  * Connect the red (VCC) wire of the second servo motor to the positive power rail on the breadboard.
  * Connect the black (GND) wire of the second servo motor to the ground rail on the breadboard.
  * Connect the orange (Signal) wire of the second servo motor to digital pin 5 on the Arduino.
* Servo 3:
  * Connect the red (VCC) wire of the third servo motor to the positive power rail on the breadboard.
  * Connect the black (GND) wire of the third servo motor to the ground rail on the breadboard.
  * Connect the orange (Signal) wire of the third servo motor to digital pin 6 on the Arduino.
* Servo 4:
  * Connect the red (VCC) wire of the fourth servo motor to the positive power rail on the breadboard.
  * Connect the black (GND) wire of the fourth servo motor to the ground rail on the breadboard.
  * Connect the orange (Signal) wire of the fourth servo motor to digital pin 9 on the Arduino.
* Servo 5:
  * Connect the red (VCC) wire of the fifth servo motor to the positive power rail on the breadboard.
  * Connect the black (GND) wire of the fifth servo motor to the ground rail on the breadboard.
  * Connect the orange (Signal) wire of the fifth servo motor to digital pin 10 on the Arduino.
* Servo 6:
  * Connect the red (VCC) wire of the sixth servo motor to the positive power rail on the breadboard.
  * Connect the black (GND) wire of the sixth servo motor to the ground rail on the breadboard.
  * Connect the orange (Signal) wire of the sixth servo motor to digital pin 11 on the Arduino.
5. Power Considerations:
* Ensure the Arduino is properly powered via USB or an external power source. Due to the potential high current draw of multiple servo motors, it is recommended to use an external power supply connected to the power and ground rails of the breadboard.
  
* Connect the positive terminal of the external power supply to the positive power rail on the breadboard.
  
* Connect the ground terminal of the external power supply to the ground rail on the breadboard. Ensure this is also connected to the Arduino's GND to maintain a common ground.

## The Code:
```
#include <Servo.h>

Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;
Servo servo6;

void setup() {
  servo1.attach(3);  // Attach servo 1 to pin 3
  servo2.attach(5);  // Attach servo 2 to pin 5
  servo3.attach(6);  // Attach servo 3 to pin 6
  servo4.attach(9);  // Attach servo 4 to pin 9
  servo5.attach(10); // Attach servo 5 to pin 10
  servo6.attach(11); // Attach servo 6 to pin 11
}

void loop() {
  for (int pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    servo1.write(pos);
    servo2.write(pos);
    servo3.write(pos);
    servo4.write(pos);
    servo5.write(pos);
    servo6.write(pos);
    delay(15); // waits 15ms for the servos to reach the position
  }
  for (int pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    servo1.write(pos);
    servo2.write(pos);
    servo3.write(pos);
    servo4.write(pos);
    servo5.write(pos);
    servo6.write(pos);
    delay(15); // waits 15ms for the servos to reach the position
  }
}
```

## Concuusion:
This setup ensures that each of the six servo motors is properly powered and can receive control signals from the Arduino. By following the steps outlined above, the circuit can be successfully assembled to control multiple servo motors for various applications.






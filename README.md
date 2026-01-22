Project Description

This project is a simple line follower robot built using an Arduino UNO, IR sensors, and DC motors.
The robot is designed to automatically follow a black line drawn on a white surface by continuously reading sensor inputs and adjusting its movement.
The main goal of this project is to understand basic robotics concepts, including sensor interfacing, motor control, and real-time decision making using embedded programming.

Hardware Used:
Arduino UNO
2 × IR Sensor Modules (Left and Right)
DC Motors (6V, 60 RPM)
Motor Driver (L298N)
Robot Chassis with Wheels
12V Battery
Connecting Wires

How the Robot Works:
The robot uses two IR sensors placed at the front of the chassis.
Each sensor detects whether it is over a black line or a white surface.
The Arduino reads the sensor values continuously.
Based on the sensor readings, the Arduino decides how the motors should move.
The motor driver controls the direction of the motors accordingly.
This allows the robot to stay on the line and correct its path whenever it moves away.

Navigation Logic:
The movement of the robot is controlled using simple condition checks.
Right Sensor	Left Sensor	  Robot Action
White (0)    	White (0)	    Move Forward
Black (1)	    White (0)	    Turn Right
White (0)	    Black (1)	    Turn Left
Black (1)	    Black (1)	    Stop

This logic helps the robot follow straight paths and handle basic curves.

Motor Control:
The motors are connected through a motor driver to protect the Arduino and supply enough current.
Enable pins are kept HIGH to allow continuous motor operation.
Direction pins are controlled by the Arduino to move the robot forward, left, right, or stop.

Troubleshooting:
Issue	Cause                                  	Solution
Not following the line	                      IR sensor not tuned	Adjust sensor potentiometers
Erratic movement	                            Low battery	Charge or replace battery
Circling or spinning	                        Motor wire polarity	Reverse motor wires
No motion	Power                               Check enable pins and connections
Line loss on curves	                          Sensor position issue	Set sensor height ~5mm above surface

Technical Specifications:
Parameter	            Value
Controller          	Arduino UNO
Motor Driver	        L298N
Sensors	              2 × IR Sensor Modules
Motors	              6V DC Motors 
Operating Voltage	    12V Battery
Motion Types	        Forward, Left, Right, Stop

What I Learned:
Basics of embedded C programming using Arduino
Interfacing IR sensors with a microcontroller
Controlling DC motors using a motor driver
Implementing simple decision-based navigation logic
Understanding real-time behavior in robotics systems

Future Improvements:
Add more IR sensors for better curve detection
Implement PWM speed control
Improve turning accuracy using PID control
Add obstacle detection using ultrasonic sensors

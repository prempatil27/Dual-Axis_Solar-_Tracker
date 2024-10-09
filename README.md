# Dual-Axis_Solar-_Tracker
Project Overview
This project is a Dual Axis Solar Tracker built using an Arduino Uno, 2 servo motors, and 4 Light Dependent Resistors (LDRs). The system detects the position of the sun using the LDRs and moves the servos to ensure that the solar panel (or any other object attached to the tracker) is always aligned for optimal sunlight exposure. The horizontal and vertical movements of the servos adjust the angle to track the sun’s position across the sky.

Components
Arduino Uno
4 LDRs (Light Dependent Resistors) for detecting light intensity.
2 Servo Motors for horizontal and vertical axis movement.
Resistors for the LDR circuits.
Breadboard and jumper wires for connections.
Circuit Diagram
Refer to the attached circuit diagram file named "Circuit Diagram of Dual axis Solar Tracker.png" for the connections.

Connections:
LDRs:
LDR 1 (Top Left): Connected to A0
LDR 2 (Top Right): Connected to A3
LDR 3 (Bottom Left): Connected to A1
LDR 4 (Bottom Right): Connected to A3
Servo Motors:
Horizontal Servo: Pin 9
Vertical Servo: Pin 10
Code Explanation
The code uses the Servo.h library to control the two servo motors, which adjust the tracker in both horizontal and vertical directions.

Code Logic:
Initialization:

Horizontal servo is initialized at 180° and the vertical servo at 45°.
Delay of 2.5 seconds is added for initialization.
LDR Readings:

LDRs are used to measure the light intensity from four different directions (top-left, top-right, bottom-left, bottom-right).
The code calculates the average intensity from the top, bottom, left, and right LDRs.
Servo Movement:

The difference between top and bottom LDRs controls the vertical servo.
The difference between left and right LDRs controls the horizontal servo.
If the difference exceeds a set tolerance level, the servos adjust their angles to reposition the tracker.
Limits:

Servo movement is restricted within a predefined limit (servoh and servov) to avoid over-rotation.
Delay:

A small delay is added between each loop iteration to give time for the servos to adjust smoothly.
How to Run the Project
Set up the hardware according to the provided circuit diagram.
Upload the Arduino Code:
Open the Arduino IDE.
Copy and paste the provided code into the IDE.
Upload the code to the Arduino Uno.
Power the Arduino, and the system will start tracking the sunlight automatically by adjusting the servo angles based on the LDR readings.
Future Improvements
Integrate a power-saving feature to optimize energy consumption.
Add a reset button to realign the servos to their initial positions.
Incorporate a larger solar panel to test real-world performance.

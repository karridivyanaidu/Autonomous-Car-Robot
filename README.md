# Autonomous-Car-Robot
This project involves the design and development of an autonomous mobile robot capable of environment sensing, obstacle detection, and controlled motion. The robot integrates mechanical design, electronics, and embedded programming to demonstrate core mechatronics concept

The system uses DC geared motors with encoders, IR and ultrasonic sensors, and an H-bridge motor driver, controlled by a microcontroller (Raspberry Pi Pico / Arduino). The robot can move forward, adjust speed using PWM, and avoid obstacles based on real-time sensor feedback.

Hardware components we used:
Chassis (2 wheel differential drive), DC Motors with quadrature encoders, Motor Driver (L298N), Ultrasonic Sensor, IR Sensor, Micro controllers, Power supply

Strategy used:
After getting on the ramp, and reaching the center of the playing field, The robot turns 90 degrees to the right, and then goes forwared till the ultrasonic sensor senses the can. Once the ultrasonic sensor notices the distance less than 7cm, The IR Sensors starts, if it senses black, it is coded in such a way that it moves 2.5cm back every second, until it reaches the center, and then turns 30 degrees, and continues the same.
And if there is another robot coming, it detects it as obstacle, it either pushes the robot (which happend in the 3rd round), or moves back. And if the robot is at the edge of playing field, the IR Sensors sense the black, and move backwards, to the center of the circle. Another strategy we used was 'robot dance', which i call it. It is that, the robot moves front and back for 3 seconds, to confuse the enemy robot. 

Key Concepts used:
1. Pulse Width Modulation
2. H bridge motor control
3. Encoder pulse counting and RPM
4. Feedback based control
5. Analog to Digital Convertion

# Introduction
### Problem:
Develop a Robot Car that can navigate through a maze, avoid obstacles, and collect ore.

### Solution:
Use different sensors and actuators such as heat and ultrasonic sensors in order to detect obstacles such as “lava” and to sense the “cave walls”. The robot car will be autonomous and will use sensor data to make decisions.

# Design
The planned solution to navigating the cave is to implement 3 main sensors in the robot car. The chassis of the robot car contains a Raspberry Pi 3, Two Servos, an Ultrasonic Sensor, and a Camera. The drive train consists of a 4 motor drive with mecanum wheels. The ultrasonic sensor will be used to detect the distance from walls of the cavern as well as objects like ores. The camera will be used to differentiate the types of objects. The final sensor will be a heat sensor to sense where the lava is in order to avoid it while traversing the maze.

# Implementation
The robot will be coded in Python. The code will be split into separate classes to keep things clean. We plan to use TinyML for image processing to detect different ores. For heat detection the heat sensor will be connected to an analog-to-digital converter that corresponds to temperature shifts. The robot will use these changes to detect lava. Functions will include SensorData (GetDistance, HeatSignal), ObjectRecognition (ProccessImage), and Movement (move, turn, stop). The outputs from these functions will be used in the robot's decision making A main_loop() will be used to check sensors.

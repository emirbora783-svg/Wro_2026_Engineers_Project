WRO Future Engineers 2026 Engineering Documentation

Team Introduction

Our team participated in the WRO Future Engineers category with the aim of developing a fully autonomous vehicle. This project integrates mechanical design, electronic systems, vehicle control systems, image processing, and engineering principles.

The design, assembly, and software development of the vehicle were carried out by the team members. The chassis design, power system, sensor placement, software structure, and testing processes were developed according to specific design criteria. Throughout the project, reliability, ease of development, and maintainability were our main goals.

The main objective of our vehicle is to move autonomously and stably on the competition track. For this purpose, an ESP32-CAM is used for environmental perception, an ultrasonic sensor for distance measurement, and an ESP32 as the main controller.

⸻

Engineering Design Process

The development process began with analyzing the rules of the WRO Future Engineers category. Based on the dimensions of the competition field and task requirements, the following design goals were defined:

* Reliable driving performance
* Reliable obstacle detection
* Fast image processing
* Vehicle control system structure
* Easy maintenance and development

In the initial stage, different chassis designs were evaluated and several prototypes were built. After analysis, a design with sufficient space for electronic components, a low center of gravity, and high maneuverability was selected.

Throughout the development process, sensor positions, camera angle, wheel alignment, and software parameters were continuously tested and improved.

⸻

Mechanical Design

The mechanical structure of the vehicle is based on a lightweight and durable chassis. The chassis is designed to securely hold all electronic components and withstand vibrations during operation.

The vehicle uses a single-motor differential drive system, which allows the motor to control both wheels efficiently. This system reduces mechanical complexity while simplifying software control.

The ESP32-CAM is mounted on the upper part of the vehicle to provide a wider field of view. Ultrasonic sensors are placed at the front for more accurate obstacle detection.

A 3S Li-ion battery and other heavy components are positioned to maintain a balanced center of gravity, resulting in more stable cornering.

⸻

Electronic System

The main electronic components used in the vehicle are described below.

Main Controller

ESP32

The ESP32 acts as the brain of the vehicle. All tasks such as image processing, decision-making, and motor control are performed on this board.

Motor Driver

TB6612FNG

The motor driver receives control signals from the ESP32 and adjusts motor speed and direction accordingly.

Vision System

ESP32-CAM

The camera continuously captures images of the environment. These images are processed by the software to extract track information.

Distance Measurement System

HC-SR04 Ultrasonic Sensor

The ultrasonic sensor is used to measure the distance of obstacles in front of the vehicle.

Power System

The vehicle is powered by a 3S Li-ion battery pack. Voltage regulators ensure stable and appropriate power distribution to all electronic components.

Energy consumption was tested to ensure sufficient runtime during competition runs.

DC Motor

A 150 RPM geared DC motor is used for vehicle movement in the autonomous system.

Servo Motor

An MG90 servo motor is used in the steering mechanism to provide precise and repeatable steering angle control.

⸻

Software Architecture

The software is built using a modular structure where each module performs a specific task. The system operates by processing sensor data, making decisions, and sending commands to the motors.

⸻

Image Processing

Images captured by the ESP32-CAM are processed to extract track information. A color-based analysis method is used for navigation:

* When green is detected, the vehicle turns left
* When red is detected, the vehicle turns right

⸻

Ultrasonic Sensor

The ultrasonic sensor measures the distance in front of the vehicle. When an obstacle is detected at a distance of less than 10 cm, the system triggers the decision-making module for safe maneuvering.

⸻

Decision-Making Module

Camera and sensor data are evaluated together to determine the vehicle’s movement. Visual data defines direction, while the ultrasonic sensor ensures safety.

⸻

Motor Control Module

A single-motor driving system is used in the vehicle. Motor control is handled via the TB6612FNG motor driver, allowing forward and reverse movement.

* Forward movement: Motor runs with a defined PWM value
* Reverse movement: Motor direction is reversed
* Speed control: Adjusted using PWM signals

⸻

Testing and Validation Process

A large number of tests were conducted during development.

Test scenarios included:

* Straight-line driving
* Turning performance
* Obstacle detection
* Obstacle avoidance
* Operation under different lighting conditions
* Long-duration driving tests

After each test, results were analyzed and improvements were made. Software parameters were continuously tuned to improve system reliability.

⸻

Safety Measures

Safety was an important consideration throughout the project development.

Measures included:

* Secure mounting of electronic components
* Organized cable management
* 3S Li-ion battery protection
* Software-based error handling mechanisms

The vehicle is checked before each test to ensure all systems function correctly.

⸻

Future Improvements

The following improvements are planned for future development:

* More advanced image processing algorithms
* Sensor fusion techniques
* More precise obstacle detection
* Advanced path planning algorithms
* Lighter mechanical structure
* Improved energy efficiency

These improvements are expected to increase both performance and reliability.

⸻

Repository Structure

t-photos:
Contains team photos.

v-photos:
Contains vehicle photos from different angles.

video:
Contains the driving demonstration video link.

schemes:
Contains wiring diagrams and system schematics.

src:
Contains all source code of the vehicle.

models:
Contains 3D printing and manufacturing files.

other:
Contains additional technical documentation.

⸻

Conclusion

This project is a comprehensive engineering work combining mechanical design, electronic systems, software development, and autonomous vehicle technologies.

Throughout the development process, our team applied engineering principles to build a reliable and autonomous vehicle. This repository documents the development process, technologies used, software structure, and testing activities in detail.

The project provided valuable experience in robotics, programming, electronics, and problem-solving for all team members.

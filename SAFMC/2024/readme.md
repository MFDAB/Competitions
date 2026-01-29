# SAFMC-2024

https://www.youtube.com/watch?v=T9ukNSgo-kk

This README template is based on the documentation for Team DOTA7's project for the Singapore Amazing Flying Machine Competition (SAFMC) 2024.
SAFMC 2024: Operation Drone Rescuers
Team DOTA7 | Nanyang Polytechnic
Welcome to the official repository for Team DOTA7’s SAFMC 2024 project. Our mission, "Operation Drone Rescuers," involved leading a squad of autonomous drones through a complex indoor environment to locate and rescue victims amidst challenging obstacles.
📖 Table of Contents
 * Introduction
 * Hardware Architecture
 * Software & Localization
 * Mission Strategy
 * Innovation & Lessons
🤝 Introduction
Following a comprehensive analysis of previous performances, our team focused on technology upgrades and scenario simulation to emerge victorious in the 2024 competition.
The Team
 * Sanjeev: Team Lead / General
 * Armando: Commander
 * Lynuz: Camera Specialist
 * Ashween: Design & Media Specialist
 * Rishi: Hardware Specialist
 * Aldrin: Logistics Specialist
 * Pierce: HR Specialist
🛠 Hardware Architecture
Our drones are equipped with a specialized sensor suite designed for precise indoor flight and victim detection:
 * Vision Positioning System: Includes a high-resolution camera and 3D Infrared sensor for stable hovering.
 * ESP32-CAM: Dual 2-megapixel cameras used for stereoscopic imagery, obstacle avoidance, and victim detection.
 * IMU (Inertial Measurement Unit): Measures orientation and movement using an accelerometer, gyroscope, and magnetometer.
Design Rationale
We iterated through multiple designs for our ESP32-CAM mounts, eventually downscaling to a single-camera configuration to reduce weight and extend battery life.
💻 Software & Localization
We utilized a three-step localization process to ensure high-accuracy navigation without GPS:
 * IMU (Dead Reckoning): Uses sensor fusion (2D-Kalman filter) and double integration of acceleration to calculate position.
 * RSSI (Radio Signal Strength): Employs Bluetooth Low Energy (BLE) nodes and a Raspberry Pi 5. Signals are processed via an artificial neural network and Particle Swarm Optimization.
 * SLAM & Visual Localization: Uses LIDAR to pre-scan the arena, creating a virtual image database. Real-time images are compared using Perceptual Hashing to pinpoint coordinates.
Pathfinding & Obstacle Avoidance
 * A Algorithm*: Guides the drones along the most efficient path using cost and heuristic functions.
 * ZoeDepth AI: A monocular depth estimation model that divides images into a 3x3 grid to calculate obstacle proximity and adjust flight trajectories.
🚀 Mission Strategy
The search area is divided into sectors, with specific drones assigned as "scouts".
 * Victim Detection: Drones identify victims (Blue for Single, Red for Double) and relay coordinates to a central server.
 * Swarm Control: A "Divide and Conquer" approach where four laptops control groups of drones simultaneously to manage the heavy computational load.
💡 Innovation & Lessons
 * Chilled Mission Pads: To prevent overheating during pre-flight, we developed chilled takeoff pads to passively cool the drones.
 * Parallel Processing: We utilized multiprocessing and multithreading to run localization and obstacle avoidance concurrently.
For more information, please refer to our Final Presentation or contact Team DOTA7.

# SAFMC-2024

https://www.youtube.com/watch?v=T9ukNSgo-kk

# Team DOTA7 - Search and Rescue Swarm (SAFMC 2024)
Welcome to the official repository for Team DOTA7 from Nanyang Polytechnic. This project features an autonomous search and rescue system developed for the SAFMC 2024 Category E competition. Our system utilizes a coordinated swarm of drones designed to navigate complex indoor environments and identify victims under challenging conditions.

# The Drone: System Specifications
Each drone in our fleet is equipped with a specialized sensor suite to handle indoor localization and obstacle avoidance.
| Feature | Specification |
|---|---|
| Primary Sensors | Vision Positioning System (Camera + IR Sensor) |
| Localization | IMU (Inertial Measurement Unit) & ESP32-CAM |
| Stability | IR Sensors for precise indoor hovering |
| Processing | ESP32-CAM for AI-based detection and mapping |

# Custom Modifications & Design Rationale
Our hardware underwent multiple iterations to balance weight, battery life, and thermal performance.
 * ESP32-CAM Mount Evolution: We transitioned from a dual-camera mount to a single-camera downscaled design to reduce weight and extend battery life.
 * Thermal Management: We innovated by chilling the mission pads at takeoff points. This passively cools the drones pre-flight, combatting overheating issues during the mission.
 * Interference Reduction: The final mount design flipped the ESP32-CAM to make the antennas more visible, significantly reducing signal interference.
 * External Power: Added an external battery specifically to power the ESP32-CAM, ensuring the drone's primary flight battery remained dedicated to propulsion.

# Software & Strategy
Our system uses a sophisticated 3-step localization process and AI-driven obstacle avoidance.
1. 3-Step Localization Process
 * IMU (Inertial Measurement Unit): Uses sensor fusion (gyroscope, accelerometer, magnetometer) and a 2D-Kalman filter to calculate yaw, pitch, roll, and distance via double integration.
 * RSSI Localization: Uses BLE (Bluetooth Low Energy) via base stations and a Raspberry Pi 5. Data is processed through an Artificial Neural Network optimized with a particle swarm algorithm.
 * Visual SLAM: Uses LIDAR pre-scanning to create a 3D mesh of the arena. The drones compare real-time images to a virtual database using Perceptual Hashing to pinpoint coordinates.
2. Pathfinding & Obstacle Avoidance
 * A Algorithm*: Guides the swarm along the most efficient route using a cost function and heuristics.
 * Zoe Depth AI: Employs monocular depth estimation to divide the drone's FOV into a 3x3 grid, calculating proximity to obstacles to make trajectory corrections.
# Connection & Swarm Architecture
To manage the high computational load, we implemented a "Divide and Conquer" architecture.
 * Central Server: One laptop acts as the master controller for the entire swarm.
 * Client Laptops: Four laptops each control a sub-group of 4 drones (16 drones total) to distribute the processing power.
 * Optimized WiFi: Used routers with beam-forming technology and AI traffic optimizers to reduce latency and data loss during simultaneous image transmission.

# The Team: DOTA7
 * General/Team Lead: Sanjeev
 * Commander: Armando
 * Camera Specialist: Lynuz
 * Design & Media Specialist: Ashween
 * Hardware Specialist: Rishi
 * Logistics Specialist: Aldrin
 * HR Specialist: Pierce

# Demonstration Highlights
 * Concurrent Operations: Leveraging multiprocessing and multithreading to run localization and obstacle avoidance simultaneously.
 * Search Strategy: Dividing the map into 4 sectors with designated "scout" drones for blue (single-rescue) and red (double-rescue) victims.
 * Precision Landing: Using onboard magnetometers and trigonometry to center on victims and land precisely for a successful "rescue".
Would you like me to generate a Python code snippet for the RSSI Kalman filter or the A pathfinding logic to include in your "Software" section?*

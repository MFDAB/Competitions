# SAFMC-2023

https://www.youtube.com/watch?v=Xq0oRhGTwyc

Welcome to the official repository for Tellix (our Team Name for SAFMC) a specialized search and rescue drone swarm developed by our team where we represent Nanyang Polytechnic for the SAFMC commpetition. Our mission was to engineer an autonomous system using a swarm of 10-25 drones capable of navigating complex arenas to identify and locate Victims in disaster-simulated environments.

# The Drone (DJI Tello) Specifications
We were given DJI Tello by the school as an option due to first time applying to the competition and also budget restriction

| Features | Specification |
| :--- | :---: |
| Weight | 80g |
| Max Flight Time | 13 mins (Modified) |
| Max Speed | 8 m/s |
| Camera | 5MP (2592x1936)/720p video |
| Sensor | Vision Positioning System & IR Sensor |

# Custom Modifications
To meet the rigorous demands of the mission using this budget drone with many limitations we modified the hardware to push the Tello beyond its original performance:

- Thermal Managment: Applied thermal Paste to the heat sinks for faster cooling, extending flight time by approximatetly 1min by our own testing.
- Repurposed Camera: Because the default bottom camera only provides black and white low-res imagery, which we were not able to acess after prolonged period of trial we repurpoused the front 720p camera to face 90 degrees downards using a Custom 3D Printed bracket.
- Weight Reduction: Removed the propeller guards and top covers to save weight, gaining an additional 30 seconds of battery life but as a con we the drone is more likley to break
- 360 Lighting: Added green LEDs to the top of the chasis for full visibility during swarm operations.

# Failed Prototypes
We initially tried to siphon of power for the led from the motors by soldering the Led directly to the motherboard, but this resulted in the motor faliur so we shifted to a battery powered Led to protect the circuitry.


# Stratergy & Localization
 Our swarm uses a hybrid localization system combining Mission Pads and colour Detection.

# 1. Localisation Markers
- Mission Pads: The drone scan these Patterns using their bottom camera to receive specific Coordinate-based commands
- Color detection: in specific areas like the "Bonus Room" drones follow colored lines or markers to execute movments as long as the color is in view

# 2. Room Scouting Logic
- The arena is divided into sectors.
- One drone is designated to a specific "column" within a room.
- If a Victim Marker (Mission Pad) is detected, the drone lands immediately to "rescue" the survivor; otherwise, it exits the room to continue the search.

# Connection Architecture
We established a 3-way connection system:
- Laptops: Running Python with the djitellopy library.
- Router: A D-Link router acts as the central hub.
- Drones: Each assigned a permanent static IP address via MAC address binding to ensure instant connection upon boot.
# The Team
- Executive Director: Irshaad
- Coding & Hardware Directors: Sanjeev & Caleb
- Hardware Specialists: Harsha, Benjamin, Ritvik & Armando
- Operations & Marketing: Dylan & Abbie

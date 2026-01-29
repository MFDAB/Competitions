# Worldskills Singapore 2023: Mechatronics

This repository documents the preparation and execution of the **Mechatronics** competition during **Worldskills Singapore 2023**. Representing **Nanyang Polytechnic** from the **Diploma in Electronic & Computer Engineering**, this project showcases the assembly, programming, and commissioning of complex industrial automation systems.

## Competition Objective

The primary goal was to **assemble and commission** a Modular Production System (MPS) in the shortest time possible while adhering to all functional and technical requirements.

---

## Technical Stack & Hardware

The competition utilized industrial-grade equipment and software to simulate real-world production environments:

* **PLC:** Panasonic FP7 PLC.
* **Programming Language:** Ladder diagrams and graph sets for pre-programming.
* **Hardware:** Modular Production System (MPS).
* **Interface:** Human Machine Interface (HMI) for machine control and monitoring.
* **Connectivity:** Netgear EN100, Ethernet hubs, and PC integration.

---
### MPS Stations
The system comprised seven distinct stations that required individual and collective integration:

1. **Distribution Station**
This station is responsible for the initial stage of the production cycle. It separates workpieces from a stack magazine using a pneumatic cylinder and pushes them out to the next station or onto a conveyor belt.

2. **Measuring Station**
The measuring station identifies the characteristics of the workpieces. It uses various sensors to detect the material type (metallic vs. non-metallic) and measures the physical height of the workpiece to ensure it meets quality standards.

3. **Process Station**
This station simulates an industrial processing task, such as drilling. It typically utilizes a rotary indexing table to move workpieces through different sub-stages, where they are checked for correct orientation before the "drilling" or "milling" simulation occurs.

4. **Handling Station**
Equipped with a pneumatic gripper , the handling station provides the necessary logistics to transport workpieces. It uses a 2-axis system to pick up a workpiece from one location and transfer it precisely to the input of a neighboring station.

5. **Pick and Place Station**
The pick and place station is a high-precision handling module. It is designed for tasks that require specific component placement, often involving a 2-axis movement to grab a lid or a secondary part and place it onto the primary workpiece.

6. **Fluid Muscle Station**
This station is distinct for its use of pneumatic muscle technology. Unlike standard cylinders, these contracting tubes act like biological muscles to perform pressing operations with a high degree of force and smooth motion to move the workpiece to the next station.

7. **Sorting Station**
Usally as the final stage, the sorting station organizes the finished workpieces. Using a conveyor belt and optical or inductive sensors, it identifies the workpiece's properties and activates pneumatic gates to sort them into one of three distinct slides.
---

## Competition Schedule

The event was structured over four days at Nanyang Polytechnic (NP):

* **Day 0:** Arena setup, unpacking MPS stations, and equipment testing.
* **Day 1:** Initial assembly, commissioning, and re-programming tasks (3 hours each).
* **Day 2:** Working with unknown stations and components, followed by reprogramming.
* **Day 3:** Reverting the MPS to original specifications and final commissioning.



---

## Evaluation Criteria

Performances were scored out of a **total of 60 points** across several categories:

| Category | Maximum Points |
| --- | --- |
| **Function (PLC Program)** | 25 Points |
| **Commissioning (Sorting Station)** | 15 Points |
| **Assembly Section** | 10 Points |
| **Time Evaluation** | 10 Points |
---
## 🧠 Personal Strategy & Reflections

* **Team Synergy:** Adopted a strategy of helping partners with the physical build before focusing on individual programming tasks.
* **Challenges:** Managed high-stress situations involving unfamiliar products, remembering specific I/O ports, and program retention under pressure.
* **Growth:** Emphasized the importance of drawing graph sets manually before transferring them to the computer and seeking "unknown" products from coaches during training.

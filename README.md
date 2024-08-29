# Cooperative Merging in Mixed Traffic Based on Strategic Influence of Connected Automated Vehicles on Human-Driven Vehicle Behavior

This study proposes a cooperative merging strategy for connected and automated vehicles (CAVs) in mixed traffic environments with human-driven vehicles (HDVs). By optimizing CAV arrival times and strategically influencing HDV behavior, the strategy enhances traffic throughput and fuel efficiency at highway merging points.



## Modeling Framework

This study addresses the coordination of multiple CAVs alongside HDVs at a highway merging point, focusing on a scenario with one main road and one on-ramp. A control zone allows a coordinator to monitor and manage vehicle movements, optimizing CAV control inputs to ensure safe merging. The merging strategy enforces safe time gaps between vehicles to prevent both lateral and rear-end collisions, ultimately coordinating vehicle arrival times to enhance traffic flow.

![image](https://github.com/user-attachments/assets/19bad611-b024-4371-85b8-62dbaff23f3c)



### Arrival Time Optimization

**Objective:** The Arrival Time Optimization problem aims to determine the optimal arrival times of connected autonomous vehicles (CAVs) at a merging point to improve traffic flow and minimize collision risks. 

**Formulation:**

- **Objective Function:** Minimize the sum of the squares of the arrival times \( <img src="https://latex.codecogs.com/gif.latex?T_i " />  \) for all CAVs.
- **Constraints:** Includes conditions to avoid lateral and rear-end collisions, but does not consider vehicle dynamics or control inputs.
- **Rewritten Form:** The problem can be expressed in vector form considering both CAV and human-driven vehicle (HDV) arrival times, with constraints depending on HDV arrival times.

**Solution:** The solution provides optimal arrival times \( <img src="https://latex.codecogs.com/gif.latex?T^*_i " /> \) for the CAVs, which are then used in the subsequent energy-optimal control phase.



### Energy-Optimal Control

**Objective:** The Energy-Optimal Control problem focuses on determining the control inputs for each CAV to reach the merging point at the specified optimal arrival times with minimum energy consumption.

**Formulation:**

- **Objective Function:** Minimize the integral of the squared control input over time, reflecting the effort required for control.
- **Constraints:** Includes vehicle dynamics, control input constraints, and requirements to avoid rear-end collisions. Constraints are relaxed for practical implementation:
  - **Velocity Constraints:** Applied only at the arrival time.
  - **Position Constraints:** Applied at the next time step due to difficulties in predicting HDV positions.

**Unconstrained Solution:** Provides a baseline for control inputs, velocities, and positions assuming no active constraints. This is used to determine feasible control actions within the relaxed constraints.



![image](https://github.com/user-attachments/assets/242f794c-25a6-4b22-8962-389e7ed40638)



## Demo

https://github.com/user-attachments/assets/afab4ac5-6ed9-4508-9f12-00304ac6257a

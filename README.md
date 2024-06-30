# Traffic_Light_Controller
The objective of this project is to develop a Verilog-based methodology for traffic control, specifically designed for a T-shaped road configuration, incorporating precise time delays to manage traffic flow efficiently.

## Introduction

Traffic control presents significant challenges in urban environments due to the high volume of vehicles and dynamic nature of traffic systems. Inefficient traffic management contributes to accidents and wasted time. This project addresses these issues by optimizing vehicle wait times at traffic signals using a Verilog-based hardware design approach.

### Verilog for Hardware Design

Verilog, a hardware description language (HDL), is specifically tailored for designing and simulating digital circuits. Unlike traditional methods involving physical components on breadboards or PCBs, Verilog streamlines the simulation process, reducing errors and implementation time. Designs can be directly coded and simulated, ensuring accurate functionality before physical construction.

Verilog is particularly suited for sequential circuits like shift registers and combinational logic circuits such as adders and subtractors. It abstractly describes digital systems like microprocessors and memories, facilitating easy simulation, design, and debugging compared to schematic-based approaches, especially for complex circuits.

## Project Overview

This project focuses on developing a basic traffic light control system for a T-shaped road.

### Traffic Light Control System

A traffic light system regulates intersection traffic flow using standard red, yellow, and green signals, coordinating with pedestrian signals for safe crossing.

### Traffic Light Functionality

- Red light: Stops all traffic in all directions.
- Yellow light: Signals cross-town traffic to slow down.
- Green light: Allows traffic to proceed.

### Challenges Addressed

Common traffic issues, such as congestion due to unregulated traffic levels and unnecessary waiting times, are mitigated through precise traffic level detection and configurable delay times.

## Explanation
### Considered directions
![](configurations.png)

The directions M1, MT, M2, and S considered for our problem analysis are illustrated in the figure.
### States
Furthermore, the problem statement is also explained in the figure. We have taken six states (S1, S2, S3, S4, S5, S6) into consideration, and the state diagram and state table are created based on the logic explained in the figure.

![](states.png)

- A green light indicates a clear route with no traffic, allowing an easy flow of vehicles.
- A red light signals a traffic jam, blocking the route for vehicle movement.
- While a yellow light signifies medium traffic flow in the route.

The time delays for transitioning from one state to another are defined as follows:

- TMG: from S1 to S2
- TY: from S2 to S3
- TTG: from S3 to S4
- TY: from S4 to S5
- TSG: from S5 to S6
- TY: from S6 to S1

This sequence continues in a cycle.

### State Diagram

The signal will stay in state S1 for TMG seconds before transitioning to state S2. It will then remain in state S2 for TY seconds before moving to state S3. This pattern continues, with the signal staying in each state for the specified duration. After TY seconds in state S6, the signal returns to state S1, and the cycle repeats.


![](State diagram.png)

In the figure, the time delays are as follows:

- TMG: 7 seconds
- TY: 2 seconds
- TTG: 5 seconds
- TSG: 3 seconds







# ECP205 ESP32 Control Algorithm
The ECP-205 Torsional Control System is a laboratory apparatus designed for teaching and research in control engineering. This repository is used to replaced the old DSP of ECP205 with ESP32 based on the same Control Algorithm on the documentation.

## Project Overview
The project explores the transition from the original DSP hardware used in the ECP-205 system to a modern embedded controller. Legacy control algorithms such as PID and PID + feedforward were analyzed, simulated, and adapted to ensure compatibility with new hardware constraints.  

The work is structured in three phases:
1. **Analysis of Legacy DSP Algorithms** – Review of sampling limitations, transfer functions, and control implementations on the original DSP system.  
2. **Algorithm Rewrite in Simulink** – Adaptation of the old algorithms into Simulink, with modular blocks for encoder parsing, control computation, and PWM output.  
3. **Deployment to ESP32** – Implementation of the algorithms on an ESP32 board with profiling of execution time and performance comparison against the legacy DSP.

---

## Features
- Legacy DSP analysis with minimum sampling time of 0.884 ms (≈1.1 kHz).  
- Simulink models for open-loop and closed-loop simulations with various plant configurations.  
- Control algorithms including:
  - General form controllers  
  - PID and PID + feedforward  
- Serial encoder input parsing and selection.  
- PWM-based voltage control using BTS7960 motor driver.  
- Deployment to ESP32 with automatic code generation and execution profiling.  
- Comparison of performance and limitations between the old DSP and the ESP32 platform.  

---

## Hardware & References
- **Plant**: ECP-205 Torsional Control System (multi-disk torsional dynamics)  
- **Actuator**: BLH-S1-4/15 driver, torque constant 0.0865 Nm/A  
- **Controller (legacy)**: DSP board with 16-bit resolution  
- **Controller (new)**: ESP32 (8-bit resolution in Simulink), programmable via Arduino IDE, Python, or Simulink  
- **Reference**: ECP-205 Lab Manual (esp. sections on modeling, pp. 70–72 and 124)  

---

## Presentation
You can see "Torsional System Algorithm Developer.pdf" to get some insight on how to build the project (but it's in Indonesian)

## Acknowledgment

This work was developed as part of Mechatronics Lecture Project by Muhammad Hanif Hibatullah.

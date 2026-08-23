# BJT Programmable Gain Amplifier (PGA)
![Header Strip](https://placehold.co/1000x8/0052cc/0052cc.png)

## Overview
![Overview Strip](https://placehold.co/1000x4/17a2b8/17a2b8.png)
This repository contains the design, simulation, and physical hardware implementation of a Programmable Gain Amplifier constructed entirely using discrete Bipolar Junction Transistors (BJTs). 

**Important Note on Application:**
This amplifier is purely built for low-frequency message signal applications. It is not intended for use with high-frequency carrier signals.

**Key Specifications:**
*   **Operating Input Voltage Range:** 1 mV to 1.2 V
*   **Amplification Factor:** 8x amplification
*   **Gain Control:** 3-bit programmable digital control (8 discrete gain steps)

## Circuit Design
![Circuit Strip](https://placehold.co/1000x4/28a745/28a745.png)
The circuit is based on a discrete operational amplifier topology, utilizing a differential input pair, a current mirror active load, a voltage amplifier stage, and an output buffer. Gain switching is achieved via a digitally controlled transistor network that alters the feedback loop impedance.

![Circuit Schematic](Circuit/Circuit.jpeg)

## Simulation and Software
![Software Strip](https://placehold.co/1000x4/ffc107/ffc107.png)
The circuit has been simulated using SPICE to verify transient response and stability across all programmable gain states.

![Simulation Plot](Software/Software_Simulation.jpeg)

## Hardware Implementation
![Hardware Strip](https://placehold.co/1000x4/dc3545/dc3545.png)
The physical hardware has been constructed and tested on a breadboard. The following images demonstrate the physical setup and the oscilloscope outputs across various gain steps.

### Breadboard Setup
![Hardware Setup 1](Hardware/Hardware-1.jpeg)

![Hardware Setup 2](Hardware/Hardware-2.jpeg)

![Hardware Setup 3](Hardware/Hardware-3.jpeg)

### Gain Steps Validation
The gain is controlled through a 3-bit binary input, providing 8 distinct amplification steps (Step 0 through Step 7).

#### Step 0
![Step 0](Hardware/Step-0.jpeg)

#### Step 1
![Step 1](Hardware/Step-1.jpeg)

#### Step 2
![Step 2](Hardware/Step-2.jpeg)

#### Step 3
![Step 3](Hardware/Step-3.jpeg)

#### Step 4
![Step 4](Hardware/Step-4.jpeg)

#### Step 5
![Step 5](Hardware/Step-5.jpeg)

#### Step 6
![Step 6](Hardware/Step-6.jpeg)

#### Step 7
![Step 7](Hardware/Step-7.jpeg)

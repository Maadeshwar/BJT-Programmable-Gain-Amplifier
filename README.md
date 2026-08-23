<p align="center">
  <img src="https://placehold.co/900x80/004d99/ffffff?text=BJT+Programmable+Gain+Amplifier+(PGA)&font=Montserrat" alt="BJT Programmable Gain Amplifier">
</p>

<br>

<p align="center">
  <img src="https://placehold.co/900x50/17a2b8/ffffff?text=Overview+and+Specifications&font=Montserrat" alt="Overview and Specifications">
</p>

This repository contains the design, simulation, and physical hardware implementation of a Programmable Gain Amplifier constructed entirely using discrete Bipolar Junction Transistors (BJTs).

**Important Note on Application:**
This amplifier is purely built for **low-frequency message signal applications**. It is strictly not intended for use with high-frequency carrier signals.

**Key Specifications:**
*   **Operating Input Voltage Range:** 1 mV to 1.2 V
*   **Amplification Factor:** Up to 8x amplification
*   **Gain Control:** 3-bit programmable digital control (8 discrete gain steps)

<br>

<p align="center">
  <img src="https://placehold.co/900x50/6f42c1/ffffff?text=3-Bit+Gain+Control+Theory&font=Montserrat" alt="3-Bit Gain Control Theory">
</p>

The amplification factor is controlled digitally using a 3-bit binary input system, yielding 8 distinct gain levels (Step 0 through Step 7). 

*   **Binary Inputs:** The system takes three digital inputs: **B2** (Most Significant Bit), **B1**, and **B0** (Least Significant Bit).
*   **Switching Mechanism:** These digital signals are applied to the bases of three switching transistors in the input network. 
*   **Impedance Modulation:** When a control bit is driven to logic HIGH, its corresponding transistor turns on, acting as a switch that connects a specific parallel resistor to ground. This alters the equivalent AC impedance of the feedback network connected to the differential amplifier.
*   **Gain Adjustment:** As the binary input value increments (from `000` up to `111`), the equivalent resistance to ground decreases. This decrease in resistance proportionately increases the closed-loop voltage gain of the amplifier, allowing precise scaling up to the maximum 8x amplification.

<br>

<p align="center">
  <img src="https://placehold.co/900x50/28a745/ffffff?text=Circuit+Design&font=Montserrat" alt="Circuit Design">
</p>

The core circuit is based on a discrete operational amplifier topology, utilizing a differential input pair, a current mirror active load, a voltage amplifier stage, and an output buffer.

<p align="center">
  <img src="Circuit/Circuit.jpeg" alt="Circuit Schematic">
</p>

<br>

<p align="center">
  <img src="https://placehold.co/900x50/ffc107/333333?text=Simulation+and+Software&font=Montserrat" alt="Simulation and Software">
</p>

The circuit has been simulated using SPICE to verify the transient response, signal integrity, and stability across all programmable gain states for low-frequency message signals.

<p align="center">
  <img src="Software/Software_Simulation.jpeg" alt="Simulation Plot">
</p>

<br>

<p align="center">
  <img src="https://placehold.co/900x50/dc3545/ffffff?text=Hardware+Implementation&font=Montserrat" alt="Hardware Implementation">
</p>

The physical hardware has been constructed and tested on a breadboard. The following images demonstrate the physical setup and the oscilloscope outputs validating the 8 distinct gain steps.

### Breadboard Setup
<p align="center">
  <img src="Hardware/Hardware-1.jpeg" width="32%">
  <img src="Hardware/Hardware-2.jpeg" width="32%">
  <img src="Hardware/Hardware-3.jpeg" width="32%">
</p>

### Gain Steps Validation

#### Step 0 (Binary: 000)
<p align="center"><img src="Hardware/Step-0.jpeg" alt="Step 0"></p>

#### Step 1 (Binary: 001)
<p align="center"><img src="Hardware/Step-1.jpeg" alt="Step 1"></p>

#### Step 2 (Binary: 010)
<p align="center"><img src="Hardware/Step-2.jpeg" alt="Step 2"></p>

#### Step 3 (Binary: 011)
<p align="center"><img src="Hardware/Step-3.jpeg" alt="Step 3"></p>

#### Step 4 (Binary: 100)
<p align="center"><img src="Hardware/Step-4.jpeg" alt="Step 4"></p>

#### Step 5 (Binary: 101)
<p align="center"><img src="Hardware/Step-5.jpeg" alt="Step 5"></p>

#### Step 6 (Binary: 110)
<p align="center"><img src="Hardware/Step-6.jpeg" alt="Step 6"></p>

#### Step 7 (Binary: 111)
<p align="center"><img src="Hardware/Step-7.jpeg" alt="Step 7"></p>

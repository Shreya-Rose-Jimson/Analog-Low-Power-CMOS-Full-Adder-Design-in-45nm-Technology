# Analog-Low-Power-CMOS-Full-Adder-Design-in-45nm-Technology
Designed and optimized a Low-Power Hybrid 10T CMOS Full Adder in 45nm technology using Cadence Virtuoso, focusing on  analog transistor-level VLSI design and low-power circuit implementation.

# Design and Analysis of Hybrid 10T Adder for Low-Power Applications

## Overview

This project presents the design and analysis of a **Hybrid 10-Transistor (10T) Full Adder** optimized for low-power VLSI applications. The work is based on the Hybrid 10T adder architecture proposed by Srinivas et al. and further enhanced using transistor-level low-power techniques such as supply voltage scaling, high-threshold voltage (HVT) transistors, and glitch reduction methods.

The design was implemented and simulated using **Cadence Virtuoso** in **45 nm CMOS technology**, demonstrating significant reductions in power consumption while maintaining correct functionality.

---

## Project Information

| Parameter | Details |
|------------|----------|
| Course | Low Power VLSI (UE23EC342BB4) |
| Institution | PES University |
| Department | Electronics and Communication Engineering |
| Student | Shreya Rose Jimson (PES1UG23EC289) |
| Guide | Prof. Babitha S Ullal |
| Technology Node | 45 nm CMOS |
| Design Tool | Cadence Virtuoso |
| Duration | Jan – May 2026 |

---

## Abstract

Power consumption has become a critical concern in modern VLSI systems, especially for portable and battery-operated devices. Adders are fundamental building blocks in digital systems, and their optimization significantly impacts overall system efficiency.

This project investigates a Hybrid 10T Full Adder and introduces additional low-power optimization techniques including:

- Supply voltage scaling
- High Threshold Voltage (HVT) transistor implementation
- Controlled input switching for glitch reduction

Simulation results demonstrate substantial power savings compared to the baseline design, making the proposed implementation suitable for low-power VLSI applications.

---

## Introduction

With the rapid advancement of portable electronics, minimizing power consumption has become a primary objective in VLSI design.

Arithmetic circuits, particularly full adders, are extensively used in:

- Arithmetic Logic Units (ALUs)
- Digital Signal Processors (DSPs)
- Microprocessors
- Embedded Systems

Conventional CMOS adders often consume considerable dynamic and leakage power. Hybrid adder designs, such as the 10T Full Adder, provide a balance between transistor count, speed, and power efficiency.

This project focuses on enhancing the power efficiency of a Hybrid 10T Full Adder through transistor-level optimizations while preserving the original architecture.

---

## Circuit Schematic

### Base Paper Circuit

> Insert Figure 1 here

```text
Figure 1: Base Paper Hybrid 10T Adder Schematic
```

### Project Implementation

```text
Figure 2: Hybrid 10T Adder Schematic Implemented in Cadence Virtuoso
```

> Insert Figure 2 here

---

## Proposed Low-Power Techniques

### 1. Supply Voltage Scaling

Dynamic power consumption is proportional to the square of the supply voltage:

\[
P \propto V_{DD}^{2}
\]

Reducing the supply voltage significantly lowers switching power consumption.

### 2. High Threshold Voltage (HVT) Transistors

Advantages:

- Reduced leakage current
- Lower static power dissipation
- Improved energy efficiency

Trade-off:

- Slight increase in propagation delay

### 3. Glitch Reduction Through Input Control

Controlled input transitions were used to:

- Avoid simultaneous switching events
- Reduce spurious transitions
- Minimize glitch power

### 4. Voltage Restoration

Voltage restoration techniques were employed to prevent output voltage degradation and maintain reliable logic levels.

---

## Methodology

### Design Environment

- Cadence Virtuoso
- 45 nm CMOS Technology

### Transistor Sizing

The circuit was implemented at transistor level with:

- Minimum channel length = 45 nm
- PMOS devices sized larger than NMOS devices
- Optimized W/L ratios for balanced rise and fall times
- Reduced leakage current

### Power Optimization Strategy

The following optimizations were incorporated:

1. Supply voltage scaling from 1.2 V to 0.8 V
2. HVT transistor implementation
3. Controlled input switching
4. Voltage restoration

### Functional Verification

Simulations were performed for all possible combinations of:

- A
- B
- Cin

Outputs verified:

- SUM
- CARRY

Transient analysis was run for **10 µs** to ensure complete functionality verification.

---

## Input Signal Configuration

| Signal | Time Period |
|----------|------------|
| A | 200 ns |
| B | 340 ns |
| Cin | 780 ns |

Common Parameters:

- Rise Time = 5 ns
- Fall Time = 5 ns

---

## Results

### Waveform Verification

- Correct SUM output observed
- Correct CARRY output observed
- All input combinations successfully verified

### Output Waveforms

> Insert waveform screenshots here

```text
Figure 3: Base Design Waveforms
Figure 4: Voltage Scaled Design Waveforms
Figure 5: HVT Cell Implementation
Figure 6: Final Optimized Design Waveforms
```

---

## Power Analysis

### 1. Base Design

Configuration:

- Controlled Input Switching
- Voltage Restoration
- VDD = 1.2 V

| Parameter | Value |
|------------|--------|
| Average Current | 67.59 nA |
| Supply Voltage | 1.2 V |
| Power Consumption | 81.08 nW |

---

### 2. Voltage Scaled Design

Configuration:

- VDD = 0.8 V

| Parameter | Value |
|------------|--------|
| Average Current | 12.36 nA |
| Supply Voltage | 0.8 V |
| Power Consumption | 9.88 nW |

---

### 3. Final Optimized Design

Configuration:

- VDD = 0.8 V
- HVT Transistors
- Controlled Input Switching
- Voltage Restoration

| Parameter | Value |
|------------|--------|
| Average Current | 2.834 nA |
| Supply Voltage | 0.8 V |
| Power Consumption | 2.2672 nW |

---

## Performance Comparison

| Design | Power Consumption |
|----------|------------------|
| Base Design | 81.08 nW |
| Voltage Scaled Design | 9.88 nW |
| Final Optimized Design | 2.2672 nW |

### Power Reduction Achieved

| Comparison | Reduction |
|------------|------------|
| Base → Voltage Scaled Design | 87.81% |
| Base → Final Optimized Design | 97.20% |

---

## Key Contributions

- Designed and implemented a Hybrid 10T Full Adder in 45 nm CMOS technology.
- Applied supply voltage scaling from 1.2 V to 0.8 V.
- Incorporated High Threshold Voltage (HVT) transistors for leakage reduction.
- Reduced glitch power using controlled input switching.
- Implemented voltage restoration to maintain signal integrity.
- Achieved approximately **97% reduction in power consumption** compared to the baseline implementation.

---

## Tools and Technologies

- Cadence Virtuoso
- CMOS 45 nm Technology Library
- Analog Design Environment (ADE)
- Transient Analysis
- Power Measurement Tools

---

## Future Work

- Layout design and post-layout simulation
- Process, Voltage and Temperature (PVT) analysis
- Delay and Power-Delay Product (PDP) optimization
- Comparison with 8T, 12T and conventional CMOS full adders
- Migration to advanced technology nodes such as 28 nm and 16 nm

---

## Reference

D. Srinivas, N. Siva, and Rajendra Naik Bhukya,

**"Design and Analysis of Hybrid 10T Adder for Low Power Applications"**

*e-Prime*, Volume 6, 2023, Article 100379.

DOI: https://doi.org/10.1016/j.prime.2023.100379

---

## Repository Structure

```text
├── README.md
├── schematics/
│   ├── base_10T_adder.png
│   └── optimized_10T_adder.png
├── waveforms/
│   ├── base_design.png
│   ├── voltage_scaled.png
│   └── final_optimized.png
├── simulations/
│   └── cadence_results
└── report/
    └── Project_Report.pdf
```

---
**Author:** Shreya Rose Jimson  
**Course:** Low Power VLSI (UE23EC342BB4)  
**PES University, Bengaluru**

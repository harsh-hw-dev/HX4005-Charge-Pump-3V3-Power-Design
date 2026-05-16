# HX4005 Charge Pump 3.3V Power Supply

<p align="center">
  <img src="docs/schematic.png" width="700">
</p>

## Overview
This project demonstrates a compact **HX4005 Charge Pump IC** based power supply designed to generate a stable **3.3V output** from a **5V input source** without using an inductor.

The design is suitable for:
- Embedded systems
- Low-power electronics
- Sensor modules
- Portable devices
- Logic level power rails

The schematic was designed by **Harsh Saini**.

---

# Features
- 5V to 3.3V conversion
- Inductor-free charge pump topology
- Compact and low-cost design
- Low component count
- Suitable for PCB integration
- Output filtering capacitors for stable voltage
- Simple enable control

---

# Specifications

| Parameter | Value |
|---|---|
| Input Voltage | 5V |
| Output Voltage | 3.3V |
| IC Used | HX4005 |
| Topology | Charge Pump |
| Switching Components | Capacitors |
| Output Filtering | 10uF + 100nF |
| Enable Pin | Supported |

---

# Circuit Description

## Main Components

### HX4005 IC
The HX4005 is a charge pump voltage conversion IC used for generating regulated output voltage without magnetic components.

### Capacitors
- **C1 (2.2uF)** → Charge transfer capacitor
- **C2 (10uF)** → Input filtering
- **C3 (100nF)** → High-frequency bypass capacitor
- **C4 (10uF)** → Output filtering
- **C5 (100nF)** → Output decoupling

### Diodes
The diode network provides input protection and voltage routing for external 5V supply connections.

### Resistor
- **R1 (10kΩ)** → Enable pin pull configuration

---

# Working Principle

The HX4005 operates using a switched-capacitor charge pump architecture.

1. Input voltage is applied at 5V.
2. Internal switching circuitry transfers charge through C1.
3. Output voltage is regulated internally.
4. Output capacitors smooth ripple and stabilize 3.3V output.

Unlike buck converters, this design does not require:
- Inductors
- Transformers
- Large magnetic components

This makes the circuit compact and PCB-friendly.

---

# Applications

## Embedded Systems
Powering:
- ESP32
- STM32
- Arduino peripherals
- Logic circuits

## Sensor Power Supply
Ideal for:
- I2C sensors
- Environmental sensors
- IMU modules
- Wireless sensor nodes

## Portable Electronics
Useful in:
- Battery-operated devices
- Wearables
- Compact gadgets
- Handheld instruments

## Communication Modules
Can power:
- Bluetooth modules
- WiFi modules
- RF transceivers

## PCB Designs
Great for:
- Space-constrained designs
- Two-layer PCB projects
- Lightweight electronics

---

# Advantages

- Compact design
- Low EMI compared to inductive converters
- Easy PCB routing
- Reduced BOM size
- Lightweight implementation

---

# Limitations

- Lower current capability compared to buck converters
- Efficiency depends on load conditions
- Not suitable for high-power applications

---

# Repository Structure

```text
HX4005-Charge-Pump-3V3-Power-Design/
│
├── docs/
│   └── schematic.png
│
├── hardware/
│   └── HX4005_Schematic.SchDoc
│
├── pcb/
│   └── PCB_Files
│
└── README.md
Future Improvements
PCB layout optimization
Output ripple measurements
Efficiency testing
Thermal analysis
Load regulation testing
Author

Harsh Saini
Electronics & Embedded Systems Enthusiast

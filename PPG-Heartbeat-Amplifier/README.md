# PPG-Based Heartbeat Amplifier and Pulse Detection System

## Overview
This project implements a PPG (Photoplethysmography) based heartbeat amplifier capable of detecting heartbeat pulses from a fingertip and generating a buzzer output corresponding to systolic peaks.

The system processes weak millivolt-level PPG signals obtained from a pulse sensor module using:

- Active Low Pass Filtering
- Two-stage BJT Amplification
- Buffer Stage
- Threshold-based Buzzer Output

The complete circuit was designed, simulated in LTSpice, fabricated on PCB, and tested on hardware.

---

# Project Objective

The objective of this project is to:

- Detect cardiac pulse signals using a PPG sensor
- Remove motion artifacts and environmental noise
- Amplify weak heartbeat signals
- Generate an audible indication of heartbeat
- Maintain amplifier operation within the linear region

---

# Working Principle

The pulse sensor module contains:

- IR LED
- Photodiode

The IR LED emits infrared light into the fingertip. Variations in blood volume during the cardiac cycle change the reflected IR intensity.

The photodiode senses these variations and generates a weak PPG signal in the millivolt range.

This signal passes through multiple stages:

```text
Pulse Sensor → Active LPF → Amplifier Stage 1 → Amplifier Stage 2 → Buffer Stage → Buzzer
```

The buzzer activates whenever the systolic peak is detected.

---

# Circuit Stages

## 1. Active Low Pass Filter

### Purpose
- Remove motion artifacts
- Remove environmental noise
- Smooth the PPG waveform

### Specifications
- Cutoff Frequency: 70–80 Hz
- Adjustable gain using potentiometer
- Implemented using LM741 op-amp

---

## 2. Amplifier Stage 1

### Purpose
- Initial amplification of weak PPG signal
- Maintain transistor operation in active region

### Features
- Implemented using BC547B transistor
- Designed for low distortion
- Prevents clipping of PPG waveform

---

## 3. Amplifier Stage 2

### Purpose
- Additional voltage amplification
- Generate sufficient signal swing for output stage

### Features
- Adjustable gain using variable resistor
- Tuned for different pulse strengths

---

## 4. Buffer Stage

### Purpose
- Prevent loading effect on amplifier
- Drive buzzer safely

### Features
- Adjustable threshold voltage
- Buzzer activates only near systolic peaks

---

# Simulation

The circuit was simulated in LTSpice to verify:

- Filter response
- Amplifier gains
- Q-point stability
- Signal integrity
- Buzzer triggering threshold

Simulation included:
- Transient Analysis
- AC Analysis
- DC Operating Point Verification

---

# PCB Design

The PCB was designed and fabricated for hardware implementation.

### Features
- Compact single-layer PCB
- Adjustable potentiometers for tuning
- Proper grounding and routing
- Easy debugging and testing

---

# Hardware Implementation

The hardware prototype includes:

- Custom fabricated PCB
- Through-hole components
- BC547B transistors
- LM741 Op-Amp
- Variable resistors
- Electrolytic capacitors
- DC buzzer

The circuit was successfully tested with heartbeat pulse detection.

---

# Components Used

| Component | Description |
|---|---|
| Pulse Sensor | PPG Signal Source |
| LM741 | Active LPF |
| BC547B | Amplifier Stages |
| Resistors | Biasing and Gain |
| Capacitors | Coupling and Filtering |
| Potentiometers | Gain/Threshold Control |
| DC Buzzer | Audio Output |
| PCB | Hardware Implementation |

---

# Software Used

- LTSpice
- PCB Design Software

---

# Results

- Successfully amplified weak PPG signals
- Stable amplifier operation achieved
- Noise significantly reduced
- Reliable buzzer triggering observed
- Adjustable gain and threshold operation verified

---

# Constraints Followed

- Amplifier stages implemented using BJTs only
- No op-amps used in amplifier stages
- Power derived from lab supply
- Hardware fabricated using available lab components

---

# Applications

- Heartbeat Monitoring
- Biomedical Signal Processing
- Wearable Health Devices
- Pulse Detection Systems
- Educational Biomedical Electronics Projects

---

# Future Improvements

- Digital BPM Display
- Wireless Monitoring
- Microcontroller Integration
- PCB Miniaturization
- Battery Powered System

---

# Repository Structure

```text
PPG-Heartbeat-Amplifier/
│
├── README.md
├── LTSpice-Simulation/
├── PCB-Design/
├── Hardware-Images/
├── Circuit-Diagrams/
└── Project-Report/
```

---

# Hardware Images

## PCB Bottom Layer
Copper trace layout of fabricated PCB.

## Assembled Hardware
Fully assembled heartbeat amplifier circuit.

## PCB Design Layout
PCB routing and component placement.

## LTSpice Simulation
Complete multistage simulation schematic.

---

# Course Information

Course: ECE214  
Semester: Winter 2026  
Project: PPG-Based Heartbeat Amplifier

---

# References

- PPG Sensor Documentation
- Analog Electronics Design
- LTSpice Documentation
- Biomedical Instrumentation Concepts

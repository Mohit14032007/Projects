# PPG-Based Heartbeat Amplifier and Pulse Detection System

## Overview
This project implements a PPG (Photoplethysmography) based heartbeat amplifier system capable of detecting cardiac pulse signals from a fingertip using an IR LED and photodiode sensor module. The detected pulse signal is filtered, amplified, and used to drive a buzzer whenever a systolic peak occurs.

The project was developed as part of the ECE214 course project.

---

## Objective
The main objective of this project is to:

- Acquire weak PPG signals from a pulse sensor
- Remove noise and motion artifacts
- Amplify the signal while maintaining linear operation
- Detect systolic peaks
- Generate an audible buzzer output corresponding to heartbeat pulses

---

## Working Principle
The pulse sensor module contains:

- An IR LED
- A photodiode

The IR LED emits infrared light into the fingertip. Due to blood volume variations during the cardiac cycle, the reflected light intensity changes. The photodiode senses these variations and produces a weak PPG signal in the millivolt range.

The signal then passes through:

1. Active Low Pass Filter
2. Amplifier Stage 1
3. Amplifier Stage 2
4. Buffer Stage
5. Buzzer Output

The buzzer produces a beep whenever a systolic peak is detected.

---

## System Block Diagram

Pulse Sensor → Active LPF → Amplifier Stage 1 → Amplifier Stage 2 → Buffer → Buzzer

---

## Features

- Noise reduction using Active LPF
- Adjustable filter gain
- Two-stage BJT amplification
- Adjustable amplifier gain
- Buffer stage to prevent loading effect
- Threshold-controlled buzzer activation
- Real-time heartbeat indication

---

## Design Specifications

### Active Low Pass Filter
- 3dB cutoff frequency: 70–80 Hz
- Adjustable gain using variable resistor

### Amplifier Stages
- Designed using BJTs only
- Operate in linear/active region
- Variable gain adjustment in stage 2

### Buffer Stage
- Prevents loading effect from buzzer
- Adjustable threshold voltage for systolic peak detection

---

## Components Used

- Pulse Sensor Module
- Operational Amplifier (for LPF only)
- BJTs
- Resistors
- Capacitors
- Variable Resistors
- DC Buzzer
- Breadboard
- Power Supply
- Oscilloscope
- LTSpice

---

## Software Used

- LTSpice for circuit simulation

---

## Simulation and Testing

The project was first simulated in LTSpice to verify:

- Filter cutoff frequency
- Amplifier gain
- Signal integrity
- Buzzer triggering

Hardware implementation was then performed on breadboard.

---

## Constraints

- Amplifier stages cannot use op-amps
- Only BJTs and passive components allowed for amplification
- Power supplies derived from ±12V lab supply

---

## Applications

- Heart rate monitoring
- Biomedical instrumentation
- Wearable health devices
- Pulse detection systems

---

## Future Improvements

- Digital heart rate display
- Wireless monitoring
- Noise-adaptive filtering
- PCB implementation
- Battery-powered portable design

---

## Course Information

Course: ECE214  
Semester: Winter 2026

---

## References

- Pulse Sensor Documentation
- Analog Electronics Concepts
- LTSpice Simulation Manual

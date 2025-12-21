3rd Order Active Low Pass Filter (LPF)/////
Project Overview:

This project implements a 3rd order active low-pass filter designed as part of ECE215 (Monsoon 2025).
The filter is designed for:

Cutoff frequency: 1 kHz

Passband gain: 12 dB

Roll-off: 60 dB/decade

The complete workflow includes theoretical design, LTspice simulation, KiCad schematic capture, and PCB layout.

The design follows the official course problem statement and Butterworth filter theory

Theory & Design Approach:

The filter is based on a 3rd order Butterworth response for a maximally flat passband.

It is implemented using two cascaded stages:

Stage 1: First-order active RC low-pass filter

Stage 2: Second-order Sallen–Key low-pass filter

Butterworth polynomial for 3rd order:

𝐻(𝑠)=1/(𝑠+1)(𝑠2+𝑠+1)

Component values were obtained by denormalizing the transfer function for a cutoff frequency of 1 kHz and matching it with the circuit transfer function.

LTspice Simulation:

The circuit was first validated in LTspice using AC analysis.

Objectives of simulation:

Verify cutoff frequency (~1 kHz)

Confirm gain (~12 dB)

Observe roll-off slope (~60 dB/decade)

Component Value Selection:

Resistors and capacitors were chosen from available lab components

One resistor is kept variable to allow gain tuning

Capacitor values (0.1 µF) simplify matching and reduce error

Gain tolerance and cutoff deviation are within allowed limits

KiCad Schematic:

The verified LTspice circuit was recreated in KiCad.

Schematic includes:

LM741 op-amps

RC networks for both stages

Power supply connections (±12 V)

Input/output connectors

PCB Design:

The PCB was designed using KiCad PCB Editor.

Design considerations:

Short signal paths for analog integrity

Proper grounding

Clean routing and spacing

DRC-verified layout


Tools Used:

LTspice – Circuit simulation

KiCad 9.0 – Schematic & PCB design

LM741 Op-Amps

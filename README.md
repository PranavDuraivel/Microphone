# Electrostatic Microphone Design

This project presents the design, analysis, and modelling of an **electrostatic microphone capsule**. The microphone is tailored for omnidirectional speech recording with high sensitivity and clarity across the 20 Hz to 10 kHz range.

---

## 🔧 Project Overview

Electrostatic microphones operate using a capacitor structure formed by a thin, tensioned diaphragm and a rigid backplate. This project focuses on optimising:

- Diaphragm material and tension for high-frequency response
- Backplate geometry for sensitivity
- Acoustic circuit modelling using lumped parameters
- Conversion of acoustic pressure to voltage (sensitivity)
- Design extension for **hyper-cardioid** directionality

---

## 📐 Technical Summary

| Component               | Description                               |
|-------------------------|-------------------------------------------|
| **Microphone Type**     | Capacitor-based Electrostatic Microphone  |
| **Diaphragm**           | Beryllium (8 µm, 9 mm radius)             |
| **Backplate**           | Machined Aluminium                        |
| **Polarisation Voltage**| 200 V                                     |
| **Static Separation**   | 22.5 µm                                   |
| **Sensitivity**         | −25 dB (ref 1 V/Pa)                       |
| **Fundamental Frequency**| ~13.97 kHz                                |
| **Output Capacitance**  | ~10 pF                                    |
| **Time Constant**       | 0.5 s (using 5 GΩ resistor)               |
| **Estimated Cost**      | £40                                       |

---

## 🧮 Features & Analysis

### ✅ Analytical Model (Python)
- Lumped parameter model
- Diaphragm resonance frequency calculation
- Sensitivity vs frequency plot
- Acoustic and electrical domain interaction
- Frequency response shaped by:
  - Diaphragm tension
  - Backplate separation
  - Polarisation voltage

### ✅ Acoustic Circuit
- Lumped-element simulation of:
  - Diaphragm compliance
  - Air vent resistance and inertance
  - Capsule cavity compliance
- Extended for **hyper-cardioid** design with directional phase-shift venting

---

## 📊 Key Results

- **Sensitivity (Flat Response):** −25 dB V/Pa across 20 Hz – 10 kHz
- **High-Frequency Roll-Off:** Begins beyond 10 kHz due to diaphragm inertia
- **Low Cutoff Frequency:** ~0.64 Hz, enabling excellent low-frequency capture
- **Hyper-Cardioid Option:** Achieved via rear vent tuning and resistance control

---

## 📁 Repository Structure

```bash
📦 Microphone-Design
├── 📂 models
│   ├── analytical_model_microphone.py   # Python code for mic analysis
│   └── acoustic_circuit_diagram/        # Circuit schematics and vent design
├── 📂 figures
│   └── *.png                            # Sensitivity curves, polar plots, etc.
├── 📄 report.pdf                        # Full design report
└── README.md                           # This file

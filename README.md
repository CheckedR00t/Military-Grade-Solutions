

# — Open Source Pulse Linear Frequency Modulated Phased Array Radar

Hardware License: CERN-OHL-P (Strongly Recommended)
Software License:Surafel
Status: Alpha (Work in Progress)
Frequency: 10.5 GHz
Contribution: Pull Requests Welcome

---

## 📡 Overview

The Hasse Cyber Security Radar Platform is an open-source, low-cost 10.5 GHz phased array radar system based on Pulse Linear Frequency Modulated (LFM) modulation.

It is designed and developed under the research initiative to explore advanced RF sensing, radar signal processing, and cybersecurity-aware detection systems.

The platform is available in two configurations:

* Short-range (3 km) experimental version
* Extended-range (20 km) high-power version

It is intended for:

* Cybersecurity and RF research
* Drone detection and counter-UAS systems
* SDR experimentation and education
* Academic and advanced engineering development

---

## 📄 Licensing Model

This project follows a dual-license structure:

### 💻 Software (MIT License)

All software components including:

* Python GUI
* FPGA control software
* STM32 firmware
* Signal processing tools

are released under the MIT License, allowing open use, modification, and distribution.



### 🔧 Hardware (CERN-OHL-P License)

All hardware components including:

* PCB designs
* RF layouts
* Antenna systems
* Schematic files

are released under CERN Open Hardware License v2 (Strongly Reciprocal)**.

This ensures that:

* Hardware remains open-source
* Modifications must remain open
* Derivatives preserve attribution

---

### ⚠️ Responsible Use Policy

This system is intended strictly for:

* Educational research
* Cybersecurity and RF experimentation
* Academic and prototype development

It must NOT be used for:

* Unauthorized surveillance
* Illegal interception or monitoring
* Harmful or unregulated deployment

---

## 📡 Key Features

* 🟢 Fully Open Source Radar Stack (Hardware + Software)
* 🟢 Dual Configuration System:

  * HCS-RADAR-N (3 km range)
  * HCS-RADAR-X (20 km range)
* 🟢 Electronic Beam Steering (±45°)
* 🟢 FPGA-Based Signal Processing Pipeline
* 🟢 Doppler, MTI, CFAR Detection Algorithms
* 🟢 Python Real-Time Visualization Dashboard
* 🟢 GPS + IMU Sensor Fusion Integration
* 🟢 Modular RF and Power Architecture

---

## 🏗️ System Architecture

### ⚡ Power System

* Sequenced power distribution controlled via STM32 MCU

---

### ⏱ Frequency Synthesizer

* AD9523-1 low-jitter clock generator
* ADF4382 RF synthesizers
* Phase-aligned system timing for FPGA, DAC, ADC

---

### 🧠 Main Processing Unit

* FPGA: XC7A50T
* STM32F746 system controller
* RF components:

  * ADAR1000 phase shifters
  * LTC5552 mixers
  * ADTR1107 RF front-end

---

### 📡 Antenna Systems

* HCS-RADAR-N

  * 8×16 patch antenna array

* HCS-RADAR-X

  * 32×16 slotted waveguide array
  * High-power GaN amplification stage

---

## ⚙️ Signal Processing Pipeline

* LFM chirp generation (DAC)
* RF up/down conversion (mixers)
* Beam steering (phase shifters)
* FPGA processing:

  * ADC acquisition
  * I/Q demodulation
  * Filtering & decimation
  * FFT & Doppler analysis
  * MTI & CFAR detection
* Real-time visualization via Python GUI

---

## 📊 Technical Specifications

| Parameter     | HCS-RADAR-N  | HCS-RADAR-X      |
| ------------- | ------------ | ---------------- |
| Frequency     | 10.5 GHz     | 10.5 GHz         |
| Range         | 3 km         | 20 km            |
| Antenna       | 8×16 Patch   | 32×16 Waveguide  |
| Beam Steering | ±45°         | ±45°             |
| Output Power  | Low Power    | High Power (GaN) |
| Processing    | FPGA + STM32 | FPGA + STM32     |

---

## 🚀 Project Structure Policy

To maintain a clean and production-grade repository:

* 📄 `docs/` → Documentation and published reports
* 📊 `5_Simulations/generated/` → Simulation outputs (gitignored)
* ⚙️ `9_Firmware/9_2_FPGA/reports/` → FPGA artifacts (gitignored)
* 🔧 `9_Firmware/9_2_FPGA/scripts/` → Build automation scripts

---

## 🧰 Requirements

* RF and radar fundamentals
* PCB assembly experience
* Python 3.8+ environment
* FPGA development tools (Vivado recommended)

---

## 🔧 Hardware Build

* Schematics: `4_Schematics and Boards Layout/4_6_Schematics`
* Production files: `4_Schematics and Boards Layout/4_7_Production Files`
* Mechanical design: `8_Utils/Mechanical_Drawings`

---

## ⚠️ Project Status

This is an Alpha-stage research platform under active development by Surafel.

Expect frequent updates, architectural changes, and experimental features.



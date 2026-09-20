# ICOM IC-M710 VFO Controller

**Professional Windows VFO control software for the ICOM IC-M710**

**Developed by 4S6GGS**

---

## Latest Release

### ICOM IC-M710 VFO Controller — v1.0.6

**Current Beta release: `v1.0.6`**

**Real-Time S-Meter**

Portable Windows application — no Python installation required.

### Download

`ICOM_M710_VFO_Controller_1.0.6.exe`

---

## Screenshots

### v1.0.6

![ICOM IC-M710 VFO Controller v1.0.6](screenshot-v1.0.6.png)

### v1.0.5

![ICOM IC-M710 VFO Controller v1.0.5](screenshot.png)

---

# Overview

ICOM IC-M710 VFO Controller is a Windows desktop application designed to provide computer-based control of the ICOM IC-M710 through its CI-V serial interface.

The application provides frequency control, operating-mode selection, band shortcuts, mouse-wheel tuning, RX/TX status indication, real-time signal-strength monitoring, serial communication configuration, and other radio-control functions through a graphical user interface.

---

# Features

* Full VFO frequency control
* Configured VFO range: **1.6000–30.0000 MHz**
* Amateur radio band quick selection
* USB
* LSB
* AM
* AFS
* CW
* FSK
* Frequency readback
* RX/TX status indication
* Remote-control status
* Speaker mute control
* Volume control
* CI-V serial communication
* COM-port selection
* Configurable baud rate
* Radio ID configuration
* Controller ID configuration
* Mouse-wheel VFO tuning
* Manual tuning-speed selection
* Automatic tuning acceleration
* **Real-time S-Meter**
* Portable Windows executable

---

# Real-Time S-Meter

Version **1.0.6** adds real-time signal-strength monitoring.

### S-Meter Features

* S0–S8 signal-level indication
* Automatic signal polling while connected and receiving
* Approximately 300 ms polling interval
* CI-V `SIGM` / `ALY` response handling
* Signal polling stops during TX
* S-Meter resets to S0 when disconnected

The S-Meter display is intended to provide a live indication of received signal strength from the connected IC-M710.

---

# VFO Frequency Range

The controller provides a configured full-VFO range of:

**1.6000 MHz → 30.0000 MHz**

---

# Amateur Radio Band Shortcuts

| Band  | Frequency Range   | Default Start |
| ----- | ----------------- | ------------- |
| 160 m | 1.800–2.000 MHz   | 1.800 MHz     |
| 80 m  | 3.500–4.000 MHz   | 3.500 MHz     |
| 60 m  | 5.250–5.450 MHz   | 5.250 MHz     |
| 40 m  | 7.000–7.300 MHz   | 7.000 MHz     |
| 30 m  | 10.100–10.150 MHz | 10.100 MHz    |
| 20 m  | 14.000–14.350 MHz | 14.000 MHz    |
| 17 m  | 18.068–18.168 MHz | 18.068 MHz    |
| 15 m  | 21.000–21.450 MHz | 21.000 MHz    |
| 12 m  | 24.890–24.990 MHz | 24.890 MHz    |
| 10 m  | 28.000–29.700 MHz | 28.000 MHz    |

---

# VFO Tuning

The mouse wheel provides rapid frequency adjustment.

## Manual Tuning

Available tuning steps:

* 100 Hz
* 1 kHz
* 10 kHz
* 100 kHz
* 1 MHz

## Automatic Acceleration

The controller can automatically increase the tuning step while the mouse wheel is being operated.

The acceleration mode provides:

* Start tuning level
* Maximum tuning level
* Automatic step acceleration
* Reset control

Press **ESC** to stop active wheel tuning.

---

# Operating Modes

| Mode | Description            |
| ---- | ---------------------- |
| USB  | Upper Side Band        |
| LSB  | Lower Side Band        |
| AM   | Amplitude Modulation   |
| AFS  | AFS mode               |
| CW   | Continuous Wave        |
| FSK  | Frequency Shift Keying |

---

# CI-V Serial Communication

The controller communicates with the IC-M710 through the ICOM CI-V serial interface.

## Default Configuration

| Parameter     | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

## Supported Baud Rates

* 1200
* 2400
* 4800
* 9600
* 19200

The actual settings must match the configuration of the connected radio and CI-V interface.

---

# RX / TX Status

The application provides a graphical indication of the radio state:

* RX — Receive
* TX — Transmit

The interface also provides a remote-control status indication.

---

# Audio Controls

The controller provides available audio-related controls including:

* Speaker mute
* Volume control

Actual operation depends on the functions supported by the IC-M710 and the CI-V interface.

---

# System Requirements

## Operating System

* Windows 10
* Windows 11

## Hardware

* ICOM IC-M710
* Compatible CI-V interface
* Available Windows COM port

## Software

The portable EXE does not require Python to be installed.

---

# Installation

The current release is provided as a portable Windows executable.

### Installation Procedure

1. Download the latest release from GitHub.
2. Connect the IC-M710 CI-V interface to the computer.
3. Start the application.
4. Select the correct COM port.
5. Select the correct baud rate.
6. Verify the Radio ID.
7. Press **CONNECT**.

No traditional installation package is required for the portable version.

---

# Default Application State

The controller starts with the following default operating values:

| Parameter     | Default            |
| ------------- | ------------------ |
| Frequency     | 14.2000 MHz        |
| Mode          | USB                |
| VFO Range     | FULL               |
| VFO Range     | 1.6000–30.0000 MHz |
| COM Port      | COM1               |
| Baud Rate     | 4800               |
| Controller ID | 90                 |
| Radio ID      | 01                 |
| Wheel Mode    | MANUAL             |
| Wheel Step    | 100 Hz             |
| Auto Maximum  | 1 MHz              |
| TRX State     | RX                 |
| Remote Status | OFF                |

---

# Releases

## v1.0.6 — Current Release

**ICOM IC-M710 VFO Controller v1.0.6**

### Main Addition

**Real-Time S-Meter**

The v1.0.6 release adds real-time signal-strength monitoring with S0–S8 indication and automatic CI-V signal polling while receiving.

### Download

`ICOM_M710_VFO_Controller_1.0.6.exe`

### SHA-256

`2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d`

---

## v1.0.5 — Previous Release

**ICOM IC-M710 VFO Controller v1.0.5**

Previous stable release.

### Download

`ICOM_M710_VFO_Controller.exe`

The v1.0.5 release remains available for users who need the previous version.

---

# Version History

| Version | Status   | Description                           |
| ------- | -------- | ------------------------------------- |
| v1.0.6  | Current  | Real-Time S-Meter and current release |
| v1.0.5  | Previous | Previous stable release               |

Older releases remain available through the GitHub Releases archive.

---

# File Integrity

SHA-256 checksums correspond to the exact executable published with each release.

## v1.0.6

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

Generate the checksum on Windows with:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.6.exe -Algorithm SHA256
```

## v1.0.5

The v1.0.5 checksum is retained with the historical release information.

Do not use the v1.0.5 checksum for v1.0.6.

---

# Troubleshooting

## Cannot Connect to Radio

Check:

1. IC-M710 power.
2. CI-V interface connection.
3. Windows COM-port number.
4. Baud rate.
5. Radio ID.
6. CI-V wiring.
7. Another application is not already using the COM port.

## Wrong Frequency or No Frequency Response

Check the CI-V connection and confirm that the configured Radio ID matches the radio.

## Connection Drops

Check the physical serial/CI-V connection and confirm that no other software is accessing the same COM port.

## S-Meter Does Not Update

Check:

1. The radio is connected.
2. The application shows RX.
3. The CI-V interface is operating correctly.
4. The configured Radio ID is correct.

S-Meter polling is active while connected and receiving and stops during TX.

---

# Safety and Operating Notes

This software communicates directly with radio equipment.

Before transmitting:

* Verify the selected frequency.
* Verify the operating mode.
* Verify the antenna and RF system.
* Confirm the radio is configured correctly.
* Observe applicable radio regulations and operating procedures.

The software should be used with appropriate care when connected to transmitting equipment.

---

# Project

**GitHub Repository:**
https://github.com/4s6ggs/icom-icm710-vfo

**Latest Release:**
https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

**All Releases:**
https://github.com/4s6ggs/icom-icm710-vfo/releases

---

# Developer

**4S6GGS**

**ICOM IC-M710 VFO Controller**

---

# Disclaimer

This is an independent software project.

ICOM and IC-M710 are trademarks of their respective owner.

The software is provided for controlling compatible equipment through its available CI-V interface. Users are responsible for verifying their hardware configuration, serial settings, radio configuration, and operating environment.

The developer is not responsible for damage resulting from incorrect wiring, configuration, operation, or use of the software.

---

# License

See the repository license information for applicable terms.

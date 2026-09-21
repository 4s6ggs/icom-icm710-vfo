# ICOM IC-M710 VFO Controller

**Professional Windows VFO control software for the ICOM IC-M710**

**Developed by 4S6GGS**

---

## Latest Release

### ICOM IC-M710 VFO Controller — v1.0.7

**Current stable release: `v1.0.7`**

### What's New in v1.0.7

- Added a separate **COM Port Setup** page.
- Added **COM Monitor** to the COM Port Setup page.
- Added **RIT Control** to the Main page.
- Improved COM port configuration and monitoring.
- Improved radio control workflow.

Portable Windows application — **no Python installation required**.

### Download

**[Download ICOM IC-M710 VFO Controller v1.0.7](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)**

`ICOM_M710_VFO_Controller_1.0.7.exe`

---

## Screenshots

### v1.0.7

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.7.png)

### v1.0.6

![ICOM IC-M710 VFO Controller v1.0.6](screenshot-v1.0.6.png)

### v1.0.5

![ICOM IC-M710 VFO Controller v1.0.5](screenshot.png)

---

# Overview

ICOM IC-M710 VFO Controller is a Windows desktop application designed to provide computer-based control of the ICOM IC-M710 through its CI-V serial interface.

The application provides frequency control, operating-mode selection, band shortcuts, mouse-wheel tuning, RIT control, RX/TX status indication, signal-strength monitoring, serial communication configuration, COM monitoring, and other radio-control functions through a graphical user interface.

The application is provided as a portable Windows executable.

**Python source code is not included in the public release.**

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
* RIT control
* CI-V serial communication
* Separate COM Port Setup page
* COM-port selection
* Configurable baud rate
* Radio ID configuration
* Controller ID configuration
* **COM Monitor**
* Mouse-wheel VFO tuning
* Manual tuning-speed selection
* Automatic tuning acceleration
* Real-time S-Meter
* Portable Windows executable

---

# v1.0.7

Version **1.0.7** introduces improvements to the radio-control interface and serial communication configuration.

## COM Port Setup

COM Port Setup is provided as a **separate page**.

The page provides:

* COM-port selection
* Baud-rate selection
* Radio ID configuration
* Controller ID configuration
* Connection control
* COM Monitor
* Serial communication monitoring

Separating COM configuration from the main VFO control interface keeps radio operation and communication configuration organized.

## COM Monitor

The **COM Monitor** is available on the COM Port Setup page.

It is intended to provide visibility into serial communication between the computer and the ICOM IC-M710.

The monitor can be used when checking:

* COM-port communication
* Connection status
* CI-V communication
* Radio responses
* Communication problems

## RIT Control

**RIT Control is available on the Main page.**

RIT provides receiver incremental tuning adjustment while using the main VFO control interface.

---

# Real-Time S-Meter

The application provides real-time signal-strength monitoring while connected to the IC-M710.

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

# RIT Control

RIT Control is available from the **Main page**.

RIT is used for receiver incremental tuning around the selected operating frequency.

The RIT control allows the operator to make small receiver-frequency adjustments without changing the main VFO operating frequency.

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

# COM Port Setup

The COM Port Setup page provides configuration for the serial connection.

## Available Controls

* COM Port
* Baud Rate
* Radio ID
* Controller ID
* CONNECT / DISCONNECT
* COM Monitor

Use the COM Port Setup page to configure and verify the serial connection before operating the VFO.

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
4. Open **COM Port Setup**.
5. Select the correct COM port.
6. Select the correct baud rate.
7. Verify the Radio ID.
8. Verify the Controller ID if required.
9. Press **CONNECT**.
10. Use **COM Monitor** to verify serial communication.
11. Return to the Main page for VFO and RIT control.

No traditional installation package is required for the portable version.

---

# Default Application State

The controller starts with the following default operating values:

| Parameter     | Default            |
| ------------- | ------------------ |
| Frequency     | 14.2000 MHz        |
| Mode          | USB                |
| VFO Range     | FULL               |
| VFO Frequency Range | 1.6000–30.0000 MHz |
| COM Port      | COM1               |
| Baud Rate     | 4800               |
| Controller ID | 90                 |
| Radio ID      | 01                 |
| Wheel Mode    | MANUAL             |
| Wheel Step    | 100 Hz             |
| Auto Maximum  | 1 MHz              |
| TRX State     | RX                 |
| Remote Status | OFF                 |

---

# Releases

## v1.0.7 — Current Release

**ICOM IC-M710 VFO Controller v1.0.7**

### Main Changes

* Separate COM Port Setup page
* COM Monitor on the COM Port Setup page
* RIT Control on the Main page
* Improved COM-port configuration and monitoring
* Improved radio-control workflow

### Download

`ICOM_M710_VFO_Controller_1.0.7.exe`

**[Download v1.0.7](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7)**

### SHA-256

The SHA-256 checksum for v1.0.7 should be generated from the exact published executable.

Do not use the checksum from an earlier release.

---

## v1.0.6 — Previous Release

**ICOM IC-M710 VFO Controller v1.0.6**

### Main Addition

**Real-Time S-Meter**

The v1.0.6 release added real-time signal-strength monitoring with S0–S8 indication and automatic CI-V signal polling while receiving.

### Download

`ICOM_M710_VFO_Controller_1.0.6.exe`

### SHA-256

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d

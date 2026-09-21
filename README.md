# ICOM IC-M710 VFO Controller

Windows desktop VFO controller for the **ICOM IC-M710 HF Marine / General Coverage Transceiver**.

**Developed by 4S6GGS**

---

## Latest Release

### ICOM IC-M710 VFO Controller — v1.0.7

**Current release:** `v1.0.7`

Version 1.0.7 adds a dedicated **COM Port Setup** page, **COM Monitor**, and **RIT Control**, together with improvements to COM-port configuration and radio-control workflow.

### Download

Windows portable executable:

`ICOM_M710_VFO_Controller_1.0.7.exe`

No Python installation is required to run the compiled Windows executable.

[Download v1.0.7 from GitHub Releases](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7)

[View all releases](https://github.com/4s6ggs/icom-icm710-vfo/releases)

---

## v1.0.7 Screenshot

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.7.png)

---

## What's New in v1.0.7

### COM Port Setup

Version 1.0.7 introduces a separate **COM Port Setup** page for serial communication configuration.

The page provides:

* COM-port selection
* Baud-rate selection
* Controller ID configuration
* Radio ID configuration
* COM-port refresh
* Connection control
* Serial communication monitoring

### COM Monitor

A **COM Monitor** has been added to the COM Port Setup page.

The monitor provides visibility into serial communication between the computer and the IC-M710 and can be used for:

* Checking serial communication
* Troubleshooting connection problems
* Verifying commands and responses
* Monitoring the CI-V connection

### RIT Control

**RIT Control** has been added to the Main page in v1.0.7.

This allows fine receiver-frequency adjustment around the selected operating frequency.

### Other Improvements

* Improved COM-port configuration
* Improved serial communication monitoring
* Improved radio-control workflow
* Improved separation of communication settings from the main operating controls

---

# Overview

The **ICOM IC-M710 VFO Controller** is a Windows desktop application for controlling the ICOM IC-M710 through its serial / CI-V interface.

The controller provides:

* Full VFO frequency control
* Amateur-band quick selection
* Operating-mode selection
* RIT control
* Mouse-wheel VFO tuning
* Frequency readback
* RX/TX status
* Remote status
* Volume control
* Speaker mute
* COM-port configuration
* Serial communication monitoring
* Real-time S-Meter monitoring
* Radio synchronization

---

# Features

* Full VFO frequency control
* Configured VFO range: **1.6000–30.0000 MHz**
* Amateur-band quick selection
* USB, LSB, AM, AFS, CW and FSK modes
* Frequency readback
* RX/TX status display
* Remote ON/OFF status
* RIT control
* Volume control
* Speaker MUTE/UNMUTE
* Serial CI-V communication
* COM-port selection
* Baud-rate selection
* Radio ID configuration
* Controller ID configuration
* COM Monitor
* Mouse-wheel VFO tuning
* Manual tuning-speed selection
* Automatic tuning acceleration
* Real-time S-Meter
* Windows portable executable

---

# Full VFO Range

The controller supports the configured full VFO range:

```text
1.6000 MHz → 30.0000 MHz
```

---

# Amateur Radio Bands

The controller provides quick-access controls for the following bands:

| Band  |   Frequency Range |
| ----- | ----------------: |
| 160 m |   1.800–2.000 MHz |
| 80 m  |   3.500–4.000 MHz |
| 60 m  |   5.250–5.450 MHz |
| 40 m  |   7.000–7.300 MHz |
| 30 m  | 10.100–10.150 MHz |
| 20 m  | 14.000–14.350 MHz |
| 17 m  | 18.068–18.168 MHz |
| 15 m  | 21.000–21.450 MHz |
| 12 m  | 24.890–24.990 MHz |
| 10 m  | 28.000–29.700 MHz |

The controller also supports the complete configured VFO range:

```text
1.6000 MHz → 30.0000 MHz
```

---

# Operating Modes

The controller provides the following operating modes:

* **USB** — Upper Side Band
* **LSB** — Lower Side Band
* **AM** — Amplitude Modulation
* **AFS**
* **CW** — Continuous Wave
* **FSK** — Frequency Shift Keying

---

# VFO Tuning

The mouse wheel can be used to tune the VFO.

Available tuning steps:

| Step | Resolution |
| ---- | ---------: |
| 1    |     100 Hz |
| 2    |      1 kHz |
| 3    |     10 kHz |
| 4    |    100 kHz |
| 5    |      1 MHz |

## Manual Mode

In **MANUAL** mode, the selected tuning step is used for each mouse-wheel operation.

## Auto Acceleration

**AUTO ACCELERATION** increases the tuning speed while the mouse wheel is being operated continuously.

The maximum acceleration level can be selected from the controller.

Press:

```text
ESC
```

to stop active wheel tuning.

---

# RIT Control

The RIT control is available on the Main page in **v1.0.7**.

RIT provides fine receiver-frequency adjustment around the selected operating frequency.

This can be useful when receiving a signal that is slightly offset from the main operating frequency.

---

# Radio Control

The application communicates with the IC-M710 using the ICOM CI-V serial interface.

Supported controller functions include:

* Frequency setting
* Frequency reading
* VFO tuning
* Operating-mode control
* RIT control
* RX/TX status
* Remote status
* Speaker mute
* Volume control
* Radio synchronization
* Serial communication status
* Signal-strength monitoring

---

# COM Port Setup

Version 1.0.7 provides a dedicated **COM Port Setup** page.

## Configuration

The following communication parameters can be configured:

* COM Port
* Baud Rate
* Controller ID
* Radio ID

## Supported Baud Rates

```text
1200
2400
4800
9600
19200
```

Select the COM port and baud rate appropriate for the connected CI-V interface and radio configuration.

---

# COM Monitor

The **COM Monitor** is available on the COM Port Setup page.

It is intended to help verify communication between the application and the radio.

The monitor can be useful for:

* Confirming that data is being transmitted
* Confirming that responses are being received
* Diagnosing communication problems
* Checking serial configuration
* Troubleshooting CI-V connections

---

# S-Meter

Real-time S-Meter monitoring was introduced in **v1.0.6**.

The S-Meter provides:

* Real-time signal-strength display
* S0–S8 indication
* Automatic polling while connected and receiving
* ICOM IC-M710 `SIGM` / `ALY` response parsing
* Automatic reset to S0 when disconnected
* Automatic polling stop during TX
* Signal-level range from 0 to 8

The S-Meter polling interval is approximately **300 ms** while connected and receiving.

## S-Meter CI-V Command

```text
PICOA,90,<RADIO_ID>,SIGM,
```

S-Meter polling stops during transmit operation.

---

# Serial Communication

## Default Settings

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

## Available Baud Rates

```text
1200
2400
4800
9600
19200
```

---

# Default Application Settings

The controller starts with the following default values:

| Setting       | Default     |
| ------------- | ----------- |
| COM Port      | COM1        |
| Baud Rate     | 4800        |
| Controller ID | 90          |
| Radio ID      | 01          |
| Frequency     | 14.2000 MHz |
| Mode          | USB         |
| VFO Range     | FULL        |
| Wheel Mode    | MANUAL      |
| Wheel Step    | 100 Hz      |
| Auto Maximum  | 1 MHz       |
| TRX State     | RX          |
| Remote Status | OFF         |

---

# System Requirements

## Operating System

* Windows 10
* Windows 11

## Hardware

* ICOM IC-M710
* Compatible CI-V serial interface
* Available Windows COM port

## Software

The compiled Windows executable does **not** require Python to be installed.

---

# Installation

The application is distributed as a portable Windows executable.

No traditional Windows installer is required.

### Installation Steps

1. Download the latest release executable.
2. Connect the CI-V serial interface to the computer and IC-M710.
3. Start the executable.
4. Open **COM Port Setup**.
5. Select the correct COM port.
6. Select the correct baud rate.
7. Confirm the Controller ID.
8. Confirm the Radio ID.
9. Connect to the radio.
10. Use the COM Monitor to verify communication.

---

# Connection

Before connecting:

1. Make sure the IC-M710 is powered on.
2. Connect the CI-V interface correctly.
3. Confirm the Windows COM-port number.
4. Open **COM Port Setup**.
5. Select the correct COM port.
6. Select the correct baud rate.
7. Confirm the Radio ID.
8. Confirm the Controller ID.
9. Connect the controller.

The connection status is displayed by the application.

---

# RX / TX Status

The controller provides visual RX/TX status indication.

```text
RX
```

indicates receive operation.

```text
TX
```

indicates transmit operation.

The application also displays the remote-control status.

S-Meter polling operates while connected and receiving and stops during TX.

---

# Audio Controls

The controller includes radio audio-related controls such as:

* Speaker mute
* Volume control
* Radio status synchronization

Actual operation depends on the functions supported by the connected IC-M710 and its CI-V interface.

---

# Troubleshooting

## Cannot Connect to Radio

Check:

1. The IC-M710 is powered on.
2. The CI-V interface is connected correctly.
3. The correct Windows COM port is selected.
4. The baud rate matches the radio configuration.
5. The Radio ID is correct.
6. The Controller ID is correct.
7. No other application is using the COM port.
8. The COM Monitor is checked for communication activity.

---

## COM Port Does Not Appear

Try:

1. Disconnect and reconnect the serial interface.
2. Check Windows Device Manager.
3. Confirm that the serial-interface driver is installed if required.
4. Press **REFRESH** in COM Port Setup.
5. Restart the application if necessary.

---

## Frequency Does Not Change

Check:

* CI-V connection
* COM port
* Baud rate
* Radio ID
* Controller ID
* Serial wiring
* Radio configuration

Use the COM Monitor to verify whether commands are being transmitted and responses are being received.

---

## S-Meter Does Not Update

Check:

1. The radio is connected.
2. The controller shows RX.
3. The CI-V interface is operating correctly.
4. The Radio ID is correct.
5. The COM Monitor shows communication.

The S-Meter polling function operates while connected and receiving and stops during TX.

---

# Release History

## v1.0.7 — Current Release

**Release:** `v1.0.7`

### Changes

* Added separate COM Port Setup page
* Added COM Monitor
* Added RIT Control to Main page
* Improved COM-port configuration
* Improved communication monitoring
* Improved radio-control workflow

### Screenshot

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.7.png)

### Executable

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

### SHA-256

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

### Verify the Download

On Windows PowerShell:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.7.exe -Algorithm SHA256
```

Expected result:

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

[View v1.0.7 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7)

---

## v1.0.6

**Release:** `v1.0.6`

Version 1.0.6 introduced **real-time S-Meter monitoring**.

### v1.0.6 Screenshot

![ICOM IC-M710 VFO Controller v1.0.6](screenshot-v1.0.6.png)

### v1.0.6 Feature

Real-time S-Meter:

* S0–S8 display
* Approximately 300 ms polling
* `SIGM` / `ALY` response parsing
* Polling while connected and receiving
* Polling stops during TX
* S-meter resets to S0 when disconnected

### Executable

```text
ICOM_M710_VFO_Controller_1.0.6.exe
```

### SHA-256

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

### Verify the Download

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.6.exe -Algorithm SHA256
```

[View v1.0.6 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.6)

---

## v1.0.5

**Release:** `v1.0.5`

Version 1.0.5 is retained as an earlier release of the ICOM IC-M710 VFO Controller.

### v1.0.5 Screenshot

![ICOM IC-M710 VFO Controller v1.0.5](screenshot.png)

### Executable

```text
ICOM_M710_VFO_Controller.exe
```

### SHA-256

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

### Verify the Download

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller.exe -Algorithm SHA256
```

---

# Version Summary

| Version    | Release Focus                                                                     |
| ---------- | --------------------------------------------------------------------------------- |
| **v1.0.7** | COM Port Setup, COM Monitor, RIT Control, communication and workflow improvements |
| **v1.0.6** | Real-time S-Meter                                                                 |
| **v1.0.5** | Earlier VFO controller release                                                    |

---

# File Integrity

SHA-256 checksums are provided for released executables so downloaded files can be independently verified.

### v1.0.7

```text
ICOM_M710_VFO_Controller_1.0.7.exe

85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

### v1.0.6

```text
ICOM_M710_VFO_Controller_1.0.6.exe

2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

### v1.0.5

```text
ICOM_M710_VFO_Controller.exe

60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

---

# Public Repository

GitHub repository:

https://github.com/4s6ggs/icom-icm710-vfo

Latest release:

https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

All releases:

https://github.com/4s6ggs/icom-icm710-vfo/releases

---

# Source Code

The Python source code is **not included in the public release repository**.

The released application is distributed as a compiled Windows executable.

---

# Important Notes

This software is designed for controlling the ICOM IC-M710 through an appropriate serial / CI-V interface.

Correct operation depends on:

* Radio configuration
* CI-V interface hardware
* Serial wiring
* COM-port configuration
* Baud rate
* Controller ID
* Radio ID

Always verify the configuration before operating the radio.

---

# Safety

The operator is responsible for:

* Correct radio configuration
* Frequency selection
* Transmit operation
* Antenna system
* RF exposure
* Applicable radio regulations
* Compliance with local licensing requirements

Do not transmit on frequencies where you are not authorized to operate.

---

# Disclaimer

This is an independent software project for controlling the ICOM IC-M710 through its serial / CI-V interface.

ICOM and IC-M710 are trademarks of their respective owner.

Use the software at your own risk and verify the correct CI-V configuration for your equipment before operating the radio.

The developer is not responsible for damage resulting from incorrect configuration, wiring, serial-interface settings, or operation of connected equipment.

---

# Developer

**4S6GGS**

ICOM IC-M710 VFO Controller

---

# License

See the `LICENSE` file included with this repository for the applicable license terms.

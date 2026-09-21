# ICOM IC-M710 VFO Controller

**Windows VFO and remote-control application for the ICOM IC-M710 HF Marine / General Coverage Transceiver**

**Developer:** 4S6GGS
**Current Version:** `v1.0.7`
**Platform:** Windows 10 / Windows 11

---

## Overview

The **ICOM IC-M710 VFO Controller** is a Windows desktop application for controlling and monitoring the **ICOM IC-M710** through a compatible serial / CI-V remote-control interface.

The application provides a graphical interface for:

* Frequency control
* Full VFO operation
* Amateur-band quick selection
* Operating-mode selection
* Mouse-wheel VFO tuning
* Automatic tuning acceleration
* RX/TX status
* Remote status
* Volume control
* Speaker mute
* Real-time S-Meter
* RIT control
* RF Level control
* Serial communication configuration
* COM Port monitoring
* Radio synchronization

The project is designed to provide a simple and practical Windows control interface for the IC-M710.

> **Important:** The radio, remote-control interface, connector wiring, electrical interface, and CI-V configuration must be correctly configured before using this application.

---

# Current Release — v1.0.7

## What's New in v1.0.7

Version **1.0.7** adds a dedicated communication page and new radio-control functions while keeping the v1.0.6 S-Meter functionality.

### v1.0.7 Features

* Separate Communication / COM Port page
* COM Port selection
* Baud Rate selection
* Controller ID configuration
* Radio ID configuration
* Connect / Disconnect control
* COM Port Monitor
* RIT Control
* RF Level Control
* Improved communication workflow
* Improved communication monitoring
* Main-page radio controls

---

# v1.0.7 — Communication Page

Version 1.0.7 moves communication configuration into a dedicated page.

The Communication page contains:

* COM Port
* Baud Rate
* Controller ID
* Radio ID
* CONNECT / DISCONNECT
* COM Port Monitor

This keeps serial communication settings separate from the normal radio-control interface.

---

# v1.0.7 — COM Port Monitor

The COM Port Monitor allows the operator to observe communication between the Windows controller and the IC-M710.

It can be used for:

* Checking the serial connection
* Troubleshooting communication problems
* Monitoring transmitted commands
* Monitoring radio responses
* Testing a new interface
* Checking the selected COM port
* Confirming that the interface is active

The monitor is particularly useful when setting up the controller for the first time.

---

# v1.0.7 — RIT Control

Version 1.0.7 adds **RIT — Receive Incremental Tuning** control to the Main page.

RIT allows the receive frequency to be adjusted independently for fine receive-frequency correction.

This can be useful when a received station is slightly offset from the desired receive frequency.

---

# v1.0.7 — RF Level Control

Version 1.0.7 adds **RF Level Control** to the Main page.

The RF Level control provides additional control and monitoring of the radio's RF/signal level during operation.

This control is available directly from the main radio-control interface.

> The actual RF-level behavior depends on the IC-M710, its CI-V implementation, and the connected interface.

---

# Main Features

## VFO and Frequency Control

The controller provides:

* Direct frequency entry
* Direct frequency setting
* Frequency readback
* Full VFO operation
* Amateur-band quick selection
* Mouse-wheel tuning
* Manual tuning-speed selection
* Automatic tuning acceleration

### Full VFO Range

```text
1.6000 MHz – 30.0000 MHz
```

### Mouse-Wheel Tuning Steps

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

---

# Amateur Radio Band Selection

Quick-access band buttons are provided for the following ranges:

| Band  | Frequency Range   |
| ----- | ----------------- |
| 160 m | 1.800–2.000 MHz   |
| 80 m  | 3.500–4.000 MHz   |
| 60 m  | 5.250–5.450 MHz   |
| 40 m  | 7.000–7.300 MHz   |
| 30 m  | 10.100–10.150 MHz |
| 20 m  | 14.000–14.350 MHz |
| 17 m  | 18.068–18.168 MHz |
| 15 m  | 21.000–21.450 MHz |
| 12 m  | 24.890–24.990 MHz |
| 10 m  | 28.000–29.700 MHz |

The controller also provides the complete configured VFO range:

```text
1.6000 MHz → 30.0000 MHz
```

> These are the frequency ranges configured in the application. Always operate according to the regulations and band plan applicable to your location and service.

---

# Operating Modes

The controller provides the following mode selections:

```text
USB
LSB
AM
AFS
CW
FSK
```

### Mode Description

| Mode | Description            |
| ---- | ---------------------- |
| USB  | Upper Side Band        |
| LSB  | Lower Side Band        |
| AM   | Amplitude Modulation   |
| AFS  | AFS mode               |
| CW   | Continuous Wave        |
| FSK  | Frequency Shift Keying |

---

# Mouse-Wheel VFO Tuning

The mouse wheel can be used for fast VFO tuning.

## Manual Mode

In **MANUAL** mode, the operator selects the required tuning step.

Available steps:

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

## Auto Acceleration

In **AUTO ACCELERATION** mode, the tuning step automatically increases while the mouse wheel is continuously used.

The maximum acceleration level can be selected.

Press:

```text
ESC
```

to stop active wheel tuning.

---

# Real-Time S-Meter — v1.0.6

The real-time S-Meter was introduced in **v1.0.6**.

The controller displays received signal strength using:

```text
S0 – S8
```

## S-Meter Operation

The S-Meter:

* Polls the radio periodically while connected
* Operates during RX
* Stops during TX
* Resets to S0 after disconnect

The polling interval is approximately:

```text
300 ms
```

The controller uses the IC-M710 signal-level response to update the displayed S-Meter value.

---

# Radio Control

The controller communicates with the IC-M710 using its serial / CI-V remote-control interface.

Supported functions include:

* Frequency setting
* Frequency readback
* VFO tuning
* Operating-mode control
* RX/TX status
* Remote status
* Volume control
* Speaker mute
* S-Meter monitoring
* RIT control
* RF Level control
* Serial communication monitoring

---

# Communication Configuration

Communication settings are configured from the dedicated **Communication / COM Port** page.

## Default Settings

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

## Supported Baud Rates

```text
1200
2400
4800
9600
19200
```

Select the COM port and baud rate that match the connected interface and radio configuration.

---

# Controller ID and Radio ID

The application uses two identifiers for communication.

### Controller ID

Default:

```text
90
```

### Radio ID

Default:

```text
01
```

The Radio ID must correspond to the IC-M710 `REMT-ID` configuration.

For example:

```text
REMT-ID = 01
```

The controller should then use:

```text
Radio ID = 01
```

The normal Radio ID range is:

```text
01 – 99
```

---

# REMT-ID and REMT-IF

These are two different IC-M710 settings.

## REMT-ID

`REMT-ID` identifies the radio.

Example:

```text
REMT-ID = 01
```

The controller should use the same Radio ID.

## REMT-IF

`REMT-IF` selects the remote-control interface.

It is **not** the Radio ID.

The selected interface must correspond to the physical connection being used.

---

# Quick Start

## 1. Connect the Interface

Connect a compatible USB / serial interface between the computer and IC-M710.

Typical arrangement:

```text
Windows PC
    │
    │ USB
    ▼
USB / Serial Interface
    │
    │ Serial / CI-V
    ▼
Radio-Side Interface
    │
    ▼
ICOM IC-M710
```

---

## 2. Check the Windows COM Port

Open:

```text
Device Manager
    └── Ports (COM & LPT)
```

Identify the COM port assigned to the radio interface.

Example:

```text
CP210x USB to UART Bridge (COM4)
```

In this example:

```text
COM4
```

is the required COM port.

---

## 3. Configure the IC-M710

Before connecting the controller, verify the radio's remote-control settings.

Check:

```text
REMT-ID
REMT-IF
```

The `REMT-ID` must match the Radio ID entered in the application.

---

## 4. Start the Application

Run:

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

No Python installation is required for the compiled Windows executable.

---

## 5. Open Communication / COM Port

Enter the appropriate:

```text
COM Port
Baud Rate
Controller ID
Radio ID
```

Default values:

```text
COM Port     = COM1
Baud Rate    = 4800
Controller ID = 90
Radio ID     = 01
```

---

## 6. Check the COM Monitor

Open the COM Monitor and check for:

* Transmitted commands
* Radio responses
* Communication activity

The monitor can help identify configuration or interface problems before normal operation.

---

## 7. Connect

Press:

```text
CONNECT
```

After communication is established, return to the Main page.

---

## 8. Test the Radio

Check:

* Frequency
* Operating mode
* RX/TX state
* Remote status
* S-Meter
* RIT
* RF Level
* Volume
* Speaker mute

---

# Default Application Settings

| Setting       | Default            |
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
| Remote        | OFF                |
| S-Meter       | S0                 |

---

# Hardware Interface

The controller requires a suitable interface between the Windows computer and IC-M710.

Typical arrangement:

```text
PC
 │
 │ USB
 ▼
USB / Serial Interface
 │
 ▼
Radio-Side Interface
 │
 ▼
IC-M710
```

> **Do not assume that a generic USB-to-UART adapter can be connected directly to the IC-M710.**

The following must be verified before connecting:

* IC-M710 connector
* Connector pinout
* Electrical signal levels
* TX/RX routing
* Ground/reference
* Interface circuitry

---

# DIY CP2102 Interface

A CP2102 USB-to-UART module may be used as the USB/serial portion of a suitable interface.

A general CP2102 radio-cable reference is available here:

[DIY Universal Radio Clone Cable Using CP2102](https://www.instructables.com/DIY-Universal-Radio-Clone-Cable-Using-CP2102/)

This is a **general radio interface reference** and is **not an IC-M710 wiring diagram**.

The IC-M710 connector, electrical interface, pinout, and signal levels must be independently verified.

> **Never connect an unverified CP2102 circuit directly to the IC-M710.**

---

# Troubleshooting

## COM Port Not Available

Check:

* USB cable
* USB interface
* Windows Device Manager
* USB/serial driver
* COM port assignment
* Whether another application is using the COM port

Use the **REFRESH** function after connecting the interface.

---

## CONNECT Does Not Work

Check:

```text
COM Port
Baud Rate
Controller ID
Radio ID
REMT-ID
REMT-IF
Cable
Radio power
```

Also check the COM Monitor for communication activity.

---

## COM Monitor Shows No Activity

Check:

* Correct COM port
* USB interface
* Cable connection
* Controller connection
* Whether another application has opened the COM port

---

## Commands Are Sent but the Radio Does Not Respond

If the COM Monitor shows transmitted commands but no radio response, check:

* IC-M710 connector
* Radio-side interface
* TX/RX routing
* Ground/reference
* `REMT-IF`
* `REMT-ID`
* Baud rate
* Radio power

---

## Frequency Does Not Change

Check:

* Radio connection
* COM port
* Radio ID
* Controller ID
* Frequency range
* COM Monitor activity

---

## S-Meter Remains at S0

Check:

* Controller connection
* Radio RX state
* Serial communication
* COM Monitor
* Radio response

Remember that S-Meter polling stops during TX.

---

## RIT Does Not Respond

Check:

* Controller connection
* Radio communication
* COM Monitor
* Radio operating state

---

## RF Level Does Not Respond

Check:

* Controller connection
* Radio communication
* COM Monitor
* Radio operating state
* IC-M710 remote-control configuration
* Interface wiring

The available RF-level functionality depends on the radio's supported remote-control functions.

---

# Release History

## v1.0.7

**Communication and Main-page Control Update**

Added:

* Separate Communication / COM Port page
* COM Port Monitor
* RIT Control
* RF Level Control
* Improved communication configuration
* Improved communication monitoring
* Improved radio-control workflow

---

## v1.0.6

**Real-Time S-Meter Update**

Added:

* Real-time S-Meter
* S0–S8 signal indication
* Periodic signal-level polling
* RX/TX-aware S-Meter polling
* S0 reset after disconnect

---

## v1.0.5

**Core VFO Controller**

Established the original core controller functionality:

* Frequency control
* Full VFO operation
* Amateur-band selection
* Operating-mode selection
* Frequency readback
* Mouse-wheel tuning
* Automatic tuning acceleration
* RX/TX indication
* Remote status
* Volume control
* Speaker mute
* CI-V serial communication

---

# Download

## Latest Release — v1.0.7

Windows executable:

**`ICOM_M710_VFO_Controller_1.0.7.exe`**

[Download the latest release](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)

[View the v1.0.7 release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7)

[View all releases](https://github.com/4s6ggs/icom-icm710-vfo/releases)

---

# SHA-256 Checksum

The SHA-256 checksum for the v1.0.7 executable is:

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

Verify the downloaded file with PowerShell:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.7.exe -Algorithm SHA256
```

The calculated hash should match:

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

---

# Previous Release Checksums

## v1.0.6

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

## v1.0.5

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

---

# Project Structure

The project repository contains the application, documentation, executable releases, and screenshots.

Typical structure:

```text
icom-icm710-vfo/
│
├── README.md
│
├── docs/
│   └── USER_GUIDE.md
│
├── Software/
│   ├── ICOM_M710_VFO_Controller_1.0.7.exe
│   ├── ICOM_M710_VFO_Controller_1.0.6.exe
│   └── ICOM_M710_VFO_Controller.exe
│
└── screenshot/
    ├── screenshot-v1.0.7.png
    ├── screenshot-v1.0.6.png
    └── screenshot.png
```

For detailed operating and hardware information, see:

`docs/USER_GUIDE.md`

---

# Source Code

The public release is distributed as a compiled Windows executable.

The Python source code is not included in the public GitHub release.

---

# Screenshots

## v1.0.7

The v1.0.7 screenshot shows the updated controller interface, including the new communication controls and Main-page functions.

![ICOM IC-M710 VFO Controller v1.0.7](screenshot/screenshot-v1.0.7.png)

---

## v1.0.6

![ICOM IC-M710 VFO Controller v1.0.6](screenshot/screenshot-v1.0.6.png)

---

## v1.0.5

![ICOM IC-M710 VFO Controller v1.0.5](screenshot/screenshot.png)

---

# System Requirements

## Computer

* Windows 10
* Windows 11
* Available USB or serial connection
* Available Windows COM port

## Radio

* ICOM IC-M710
* Correctly configured remote-control interface
* Compatible serial / CI-V interface

## Software

The released application is a compiled Windows executable.

```text
Python installation: Not required
```

---

# Hardware and Safety Notes

Before connecting a DIY interface:

* Verify the IC-M710 connector.
* Verify the connector pinout.
* Verify the electrical interface.
* Verify TX/RX routing.
* Verify the signal reference/ground.
* Check for accidental shorts.
* Verify `REMT-ID`.
* Verify `REMT-IF`.
* Test the interface before normal operation.

> **Do not assume that a CP2102 UART output is electrically compatible with the IC-M710.**

Incorrect electrical connections can damage the radio, interface, or computer.

---

# Operating Responsibility

The operator is responsible for:

* Correct radio configuration
* Correct frequency selection
* Correct operating mode
* Appropriate transmit operation
* Correct hardware installation
* Applicable licensing requirements
* Applicable radio regulations

Always follow the regulations applicable to your location and operating service.

---

# Project Information

**Project:** ICOM IC-M710 VFO Controller
**Developer:** 4S6GGS
**Current Version:** `v1.0.7`
**Platform:** Windows 10 / Windows 11
**Radio:** ICOM IC-M710

---

# GitHub

**Repository:**

https://github.com/4s6ggs/icom-icm710-vfo

**Latest Release:**

https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

---

# License

See the repository for the applicable project license and distribution terms.

---

## 4S6GGS

**ICOM IC-M710 VFO Controller**

`v1.0.7`

# ICOM IC-M710 VFO Controller

**Windows VFO and remote-control application for the ICOM IC-M710**

**Developer:** 4S6GGS
**Current Version:** **v1.0.7**
**Platform:** Windows 10 / Windows 11

---

## Overview

The **ICOM IC-M710 VFO Controller** is a Windows desktop application for controlling the **ICOM IC-M710** through a compatible serial/CI-V remote-control interface.

The application provides a graphical interface for frequency control, VFO tuning, operating-mode selection, radio status, audio control, RIT, RF level control, and serial communication monitoring.

The project is designed to provide a simple Windows interface for operating and monitoring an IC-M710 from a computer.

> **Important:** The radio, remote interface, connector wiring, and electrical interface must be correctly configured before using the application.

---

# Features

## VFO and Frequency Control

* Frequency entry and direct frequency setting
* Frequency readback
* Full VFO operation
* Amateur-band quick selection
* Mouse-wheel tuning
* Manual tuning steps
* Automatic tuning acceleration
* 100 Hz to 1 MHz tuning steps

### Full VFO Range

```text
1.6000 MHz – 30.0000 MHz
```

### Available Tuning Steps

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

---

## Amateur Band Selection

Quick-access band ranges are provided for:

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

---

## Operating Modes

The controller provides:

```text
USB
LSB
AM
AFS
CW
FSK
```

---

# v1.0.7

Version **1.0.7** introduces a new communication page and additional Main-page controls.

## New in v1.0.7

### Separate Communication / COM Port Page

Communication settings are now organized on a dedicated page.

The page provides:

* COM Port selection
* Baud Rate selection
* Controller ID
* Radio ID
* Connect / Disconnect
* COM Port Monitor

This separates communication configuration from normal radio operation.

---

### COM Port Monitor

The new **COM Port Monitor** allows the operator to monitor communication between the controller and the IC-M710.

It is useful for:

* Checking the serial connection
* Troubleshooting a communication problem
* Checking transmitted commands
* Checking radio responses
* Testing a new interface or cable
* Confirming that the selected COM port is active

The COM Monitor is especially useful during initial interface testing.

---

### RIT Control

**RIT Control** has been added to the Main page.

RIT (**Receive Incremental Tuning**) allows the receive frequency to be adjusted independently for fine receive-frequency correction.

---

### RF Level Control

**RF Level Control** has also been added to the Main page.

It provides the operator with additional control/monitoring of the radio RF/signal level during operation.

---

### Communication Improvements

Version 1.0.7 also improves the communication configuration and operating workflow by separating communication settings from the main radio-control interface.

---

# v1.0.6

Version **1.0.6** introduced the real-time S-Meter functionality.

## Real-Time S-Meter

The controller displays received signal level from:

```text
S0 – S8
```

The signal level is periodically requested while the controller is connected and the radio is receiving.

S-Meter polling:

* Runs while connected
* Runs during RX
* Stops during TX
* Resets to S0 after disconnect

The polling interval is approximately:

```text
300 ms
```

---

# v1.0.5

Version **1.0.5** established the original core VFO-control functionality, including:

* Frequency control
* Full VFO
* Amateur-band selection
* Operating-mode selection
* Frequency readback
* Mouse-wheel tuning
* Automatic acceleration
* RX/TX indication
* Remote status
* Volume control
* Speaker mute
* CI-V serial communication

---

# Screenshots

## v1.0.7

![ICOM IC-M710 VFO Controller v1.0.7](screenshot/screenshot-v1.0.7.png)

## v1.0.6

![ICOM IC-M710 VFO Controller v1.0.6](screenshot/screenshot-v1.0.6.png)

## v1.0.5

![ICOM IC-M710 VFO Controller v1.0.5](screenshot/screenshot.png)

---

# Download

## Latest Release — v1.0.7

### Windows Executable

[Download ICOM_M710_VFO_Controller_1.0.7.exe](Software/ICOM_M710_VFO_Controller_1.0.7.exe)

**SHA-256:**

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

### GitHub Release

[Download the latest release](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)

[View v1.0.7 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7)

[View all releases](https://github.com/4s6ggs/icom-icm710-vfo/releases)

---

# System Requirements

## Computer

* Windows 10 or Windows 11
* Available USB or serial connection
* Available Windows COM port

## Radio

* ICOM IC-M710
* Correctly configured remote-control interface
* Compatible serial/CI-V interface

## Software

The released application is a compiled Windows executable.

```text
Python installation: Not required
```

---

# Quick Start

## 1. Connect the Interface

Connect the compatible USB/serial interface between the computer and the IC-M710.

```text
Windows PC
    │
    │ USB
    ▼
USB / Serial Interface
    │
    │ Serial / CI-V
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

Identify the COM port used by the radio interface.

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

The controller requires the correct:

```text
REMT-ID
REMT-IF
```

The **REMT-ID** is the Radio ID used by the controller.

---

## 4. Start the Application

Run:

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

---

## 5. Open Communication / COM Port

Configure:

```text
COM Port
Baud Rate
Controller ID
Radio ID
```

Default settings:

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

Supported baud rates:

```text
1200
2400
4800
9600
19200
```

---

## 6. Check COM Monitor

Use the COM Monitor to verify communication.

Check for:

* Transmitted commands
* Radio responses
* Communication activity

---

## 7. Connect

Press:

```text
CONNECT
```

After successful communication, return to the Main page.

---

## 8. Test the Radio

Check:

* Frequency
* Mode
* RX/TX status
* Remote status
* S-Meter
* RIT
* RF Level

---

# Default Settings

The application starts with the following defaults:

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

The controller requires a suitable interface between the Windows computer and the IC-M710.

A typical arrangement is:

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

The required electrical interface, connector, pinout, signal levels, and wiring must be verified before connection.

---

# DIY CP2102 Interface

A **CP2102 USB-to-UART module** can be used as the USB/serial portion of a suitable interface.

A general CP2102 radio-cable reference is available here:

[DIY Universal Radio Clone Cable Using CP2102](https://www.instructables.com/DIY-Universal-Radio-Clone-Cable-Using-CP2102-USB-I)

This is a general radio interface reference and **not an IC-M710 wiring diagram**.

The IC-M710 connector and electrical interface must be independently verified.

> **Never connect an unverified CP2102 circuit directly to the IC-M710.**

---

# Radio ID

The IC-M710 Radio ID is configured in the radio's Set Mode.

The general procedure is:

```text
Radio OFF
   ↓
Hold FUNC + 1
   ↓
Power ON
   ↓
Enter Set Mode
   ↓
Use GROUP selector
   ↓
Find REMT-ID
```

For example:

```text
REMT-ID 01
```

Then configure:

```text
Radio ID = 01
```

in the controller.

The normal ID range is:

```text
01 – 99
```

The default value is normally:

```text
01
```

---

# REMT-ID and REMT-IF

These are two different settings.

### REMT-ID

Identifies the radio.

Example:

```text
REMT-ID = 01
```

### REMT-IF

Selects the remote-control interface.

It is **not** the Radio ID.

Always select the interface corresponding to the physical connection being used.

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

Press **REFRESH** after connecting the interface.

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

---

## COM Monitor Shows No Activity

Check:

* Correct COM port
* USB interface
* Cable connection
* Controller connection
* Whether another program has opened the COM port

---

## Commands Are Sent but Radio Does Not Respond

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

# Release History

## v1.0.7

* Added separate Communication / COM Port page
* Added COM Port Monitor
* Added RIT Control
* Added RF Level Control
* Improved communication configuration
* Improved communication monitoring
* Improved radio-control workflow

## v1.0.6

* Added real-time S-Meter
* Added periodic signal-level polling
* Added RX/TX-aware S-Meter polling
* Added S0 reset on disconnect

## v1.0.5

* Core VFO control
* Full VFO operation
* Amateur-band quick selection
* Operating-mode control
* Mouse-wheel tuning
* Automatic acceleration
* Frequency readback
* RX/TX indication
* Remote status
* Volume control
* Speaker mute
* CI-V serial communication

---

# SHA-256 Checksums

Checksums are provided to verify downloaded executable files.

## v1.0.7

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

PowerShell:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.7.exe -Algorithm SHA256
```

The calculated hash should match the value above.

---

## v1.0.6

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

## v1.0.5

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

---

# Project Files

The repository contains:

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

The detailed operating and hardware information is available in:

[`docs/USER_GUIDE.md`](docs/USER_GUIDE.md)

---

# Source Code

The public release is distributed as a compiled Windows executable.

The Python source code is **not included in the public GitHub release**.

---

# Safety and Hardware Notes

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

Do not assume that a CP2102 UART output is electrically compatible with the IC-M710.

---

# Operating Responsibility

The operator is responsible for:

* Correct radio configuration
* Correct frequency selection
* Correct operating mode
* Appropriate transmit operation
* Applicable licensing requirements
* Applicable radio regulations
* Correct hardware installation

Always follow the regulations applicable to your location and operating service.

---

# Downloads and Releases

**Latest release:**

https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

**v1.0.7:**

https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7

**v1.0.6:**

https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.6

**All releases:**

https://github.com/4s6ggs/icom-icm710-vfo/releases

---

# Project Information

**Project:** ICOM IC-M710 VFO Controller
**Developer:** 4S6GGS
**Radio:** ICOM IC-M710
**Current Version:** 1.0.7
**Platform:** Windows 10 / Windows 11

**GitHub Repository:**

https://github.com/4s6ggs/icom-icm710-vfo

---

## Disclaimer

This project is an independent radio-control application.

The developer is not responsible for:

* Incorrect hardware wiring
* Damage caused by incorrect interface construction
* Incorrect radio configuration
* Incorrect frequency selection
* Unauthorized transmissions
* Regulatory violations
* Damage caused by unsuitable hardware
* Damage caused by incorrect electrical connections

Users constructing their own interface should verify all electrical and connector connections before connecting the interface to the IC-M710.

The CP2102 reference provided in this repository is a general-purpose reference and should not be considered an IC-M710-specific wiring diagram.

---

**ICOM IC-M710 VFO Controller — 4S6GGS**

**Version 1.0.7**

# ICOM IC-M710 VFO Controller

Professional Windows VFO controller for the **ICOM IC-M710 HF Marine Transceiver**, developed by **4S6GGS**.

The application provides computer-based frequency, mode, VFO tuning, RIT, COM-port configuration, COM monitoring, and radio-control functions through a serial connection.

---

## Current Release

### ICOM IC-M710 VFO Controller v1.0.7

**Release:** v1.0.7
**Platform:** Windows
**Application:** Portable executable
**Source code:** Not included in this repository

### v1.0.7 Screenshot

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.7.png)

### What's New in v1.0.7

* Added a separate **COM Port Setup** page.
* Added **COM Monitor** to the COM Port Setup page.
* Added **RIT Control** to the Main page.
* Improved COM port configuration and monitoring.
* Improved radio control workflow.

---

# Overview

The **ICOM IC-M710 VFO Controller** is a Windows desktop application designed to provide convenient computer control of the ICOM IC-M710.

The controller communicates with the radio through a serial COM port and provides a graphical interface for:

* Frequency control
* VFO tuning
* Operating-mode selection
* RIT control
* Band selection
* COM-port configuration
* Serial communication monitoring
* RX/TX status
* Remote-control status
* S-meter monitoring
* Mouse-wheel frequency tuning

The application is designed for practical operation while keeping the interface simple and easy to use.

---

# Main Features

## Frequency Control

The controller supports frequency entry and direct frequency setting.

The operating frequency can be entered through the frequency field and applied using the **SET** control.

Frequency display uses MHz with four decimal places.

Example:

```text
14.2000 MHz
```

---

## Full VFO Range

The controller supports the configured full VFO range:

```text
1.6000 MHz → 30.0000 MHz
```

The interface provides a dedicated **FULL VFO** selection.

---

# Amateur Radio Band Selection

Quick-access band controls are provided for the following ranges:

| Band  |     Frequency Range |
| ----- | ------------------: |
| 160 m |   1.800 – 2.000 MHz |
| 80 m  |   3.500 – 4.000 MHz |
| 60 m  |   5.250 – 5.450 MHz |
| 40 m  |   7.000 – 7.300 MHz |
| 30 m  | 10.100 – 10.150 MHz |
| 20 m  | 14.000 – 14.350 MHz |
| 17 m  | 18.068 – 18.168 MHz |
| 15 m  | 21.000 – 21.450 MHz |
| 12 m  | 24.890 – 24.990 MHz |
| 10 m  | 28.000 – 29.700 MHz |

The application also provides:

```text
FULL VFO
1.6000 – 30.0000 MHz
```

---

# Operating Modes

The controller provides mode selection for:

* USB
* LSB
* AM
* AFS
* CW
* FSK

The default startup mode is:

```text
USB
```

---

# VFO Mouse-Wheel Tuning

The mouse wheel can be used for fast frequency adjustment.

Available tuning steps:

| Step | Resolution |
| ---- | ---------: |
| 1    |     100 Hz |
| 2    |      1 kHz |
| 3    |     10 kHz |
| 4    |    100 kHz |
| 5    |      1 MHz |

Two tuning modes are available:

```text
MANUAL
AUTO ACCELERATION
```

Manual mode uses the selected tuning step.

Auto acceleration allows the tuning speed to increase as the wheel is operated continuously.

The maximum automatic acceleration level can be selected up to:

```text
1 MHz
```

The wheel speed can be reset using the **RESET** control.

Press:

```text
ESC
```

to stop active wheel tuning.

---

# RIT Control

Version 1.0.7 adds **RIT Control** to the Main page.

RIT allows incremental receiver tuning around the selected operating frequency.

This provides convenient fine adjustment when receiving stations that are slightly offset from the main operating frequency.

---

# COM Port Setup

Version 1.0.7 introduces a dedicated **COM Port Setup** page.

The page provides controls for configuring the serial connection between the computer and the ICOM IC-M710.

Available settings include:

* COM port selection
* Baud-rate selection
* Controller ID
* Radio ID
* Connection control
* COM-port refresh

The COM port list can be refreshed using the **REFRESH** control.

---

# COM Monitor

Version 1.0.7 adds a **COM Monitor** to the COM Port Setup page.

The monitor provides visibility into serial communication between the controller and the radio.

This can be useful when:

* Checking the serial connection
* Verifying radio communication
* Diagnosing communication problems
* Confirming commands and responses
* Troubleshooting COM-port configuration

---

# Serial Communication

The controller communicates with the ICOM IC-M710 using a serial interface.

Default communication parameters:

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

# Connection Status

The interface displays the current connection state.

Default startup state:

```text
Disconnected
```

After a successful connection:

```text
Connected
```

The connection control provides:

```text
CONNECT
DISCONNECT
```

---

# RX / TX Status

The controller displays the current transceiver state:

```text
RX
TX
```

The default state at startup is:

```text
RX
```

RX and TX states are visually distinguished in the user interface.

---

# Remote Status

The controller displays the remote-control state.

Default state:

```text
REMOTE OFF
```

---

# S-Meter

S-meter monitoring was introduced in **v1.0.6**.

The controller periodically requests signal information from the radio and displays the received signal level.

The S-meter monitoring system includes:

* Periodic signal polling
* Signal-level display
* RX monitoring
* TX protection
* Disconnect reset

S-meter polling is stopped while the radio is transmitting and is reset when the serial connection is disconnected.

---

# Default Settings

The application starts with the following default configuration:

| Parameter     | Default     |
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
| Remote        | OFF         |

---

# System Requirements

## Operating System

Windows 10 or later is recommended.

The application is provided as a Windows executable.

## Hardware

Required:

* ICOM IC-M710 transceiver
* Computer running Windows
* Compatible serial interface
* Appropriate serial connection between the computer and radio

The exact physical serial interface depends on the hardware configuration used with the IC-M710.

---

# Installation

The current release is provided as a portable Windows executable.

No Python installation is required to run the released executable.

### Installation Steps

1. Download the latest `.exe` file from the GitHub Releases page.
2. Place the executable in a suitable folder.
3. Connect the computer to the ICOM IC-M710 serial interface.
4. Start the application.
5. Open **COM Port Setup**.
6. Select the correct COM port.
7. Select the appropriate baud rate.
8. Confirm the Controller ID and Radio ID.
9. Connect to the radio.
10. Verify communication using the COM Monitor.

---

# Recommended Startup Configuration

For a typical configuration, start with:

```text
COM Port     : COM1
Baud Rate    : 4800
Controller ID: 90
Radio ID     : 01
Frequency    : 14.2000 MHz
Mode         : USB
```

The actual COM port depends on the computer and serial-interface hardware.

---

# Radio Connection

Before connecting:

1. Confirm that the ICOM IC-M710 is powered on.
2. Confirm that the serial interface is correctly connected.
3. Confirm the Windows COM port assigned to the interface.
4. Open **COM Port Setup**.
5. Select the correct COM port.
6. Select the correct baud rate.
7. Verify the Controller ID and Radio ID.
8. Connect the controller.
9. Use the COM Monitor to verify communication.

---

# Troubleshooting

## Controller Cannot Connect

Check:

* The radio is powered on.
* The serial cable/interface is connected.
* The correct COM port is selected.
* The COM port is not being used by another application.
* The baud rate is correct.
* The Controller ID is correct.
* The Radio ID is correct.

---

## COM Port Does Not Appear

Try:

1. Disconnect and reconnect the serial interface.
2. Check Windows Device Manager.
3. Confirm that the USB-to-serial driver is installed if applicable.
4. Press **REFRESH** in COM Port Setup.
5. Restart the application if necessary.

---

## No Radio Response

Check the following:

```text
COM Port
Baud Rate
Controller ID
Radio ID
Serial Wiring
Radio Configuration
```

Use the **COM Monitor** to determine whether commands are being transmitted and whether responses are being received.

---

## Frequency Does Not Change

Check:

* Serial connection status.
* COM Monitor communication.
* Radio ID.
* Controller ID.
* Selected frequency range.
* Radio operating condition.

---

## S-Meter Does Not Update

Check:

* The controller is connected.
* The radio is receiving.
* Serial communication is working.
* The COM Monitor shows radio responses.

S-meter monitoring is intended for receive operation and does not continuously poll during TX.

---

# Release Information

## v1.0.7

### Release Features

* Separate COM Port Setup page
* COM Monitor
* RIT Control on Main page
* Improved COM-port configuration
* Improved communication monitoring
* Improved radio control workflow

### Screenshot

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.7.png)

### SHA-256

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

### Verify the Download

PowerShell:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.7.exe -Algorithm SHA256
```

The resulting hash should be:

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

---

# Previous Releases

## v1.0.6

Version 1.0.6 introduced real-time **S-Meter monitoring**.

### v1.0.6 Screenshot

![ICOM IC-M710 VFO Controller v1.0.6](screenshot-v1.0.6.png)

### v1.0.6 SHA-256

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

### Verify the v1.0.6 Download

PowerShell:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.6.exe -Algorithm SHA256
```

---

## v1.0.5

Version 1.0.5 provided the earlier stable controller interface and VFO-control functionality.

### v1.0.5 Screenshot

![ICOM IC-M710 VFO Controller v1.0.5](screenshot.png)

### v1.0.5 SHA-256

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

### Verify the v1.0.5 Download

PowerShell:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.5.exe -Algorithm SHA256
```

---

# Version History

| Version   | Main Changes                                                                                         |
| --------- | ---------------------------------------------------------------------------------------------------- |
| **1.0.7** | COM Port Setup page, COM Monitor, RIT Control, improved COM configuration and radio-control workflow |
| **1.0.6** | Real-time S-Meter monitoring                                                                         |
| **1.0.5** | Earlier stable VFO controller functionality                                                          |

---

# File Integrity

SHA-256 hashes are provided for released executables so downloaded files can be independently verified.

Current release:

```text
ICOM_M710_VFO_Controller_1.0.7.exe

SHA-256:
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

---

# Project Structure

The GitHub repository contains the public release documentation and release files.

The Python source code is intentionally **not included** in the public repository.

The released application is distributed as a compiled Windows executable.

---

# Important Notes

This software is designed specifically for controlling the ICOM IC-M710 through an appropriate serial interface.

Correct operation depends on:

* Radio configuration
* Serial-interface hardware
* COM-port configuration
* Communication parameters
* Radio ID
* Controller ID
* Proper serial wiring

Always verify the configuration before operating the radio.

---

# Safety

This software is a computer-control interface for the ICOM IC-M710.

The operator remains responsible for:

* Correct radio configuration
* Frequency selection
* Transmit operation
* Antenna system
* RF exposure
* Applicable radio regulations
* Compliance with local licensing requirements

Do not transmit on frequencies where you are not authorized to operate.

---

# Project

**Project:** ICOM IC-M710 VFO Controller

**GitHub Repository:**
https://github.com/4s6ggs/icom-icm710-vfo

**Current Version:**
v1.0.7

**Developer:**
4S6GGS

---

# Developer

**4S6GGS**

ICOM IC-M710 VFO Controller project.

---

# Disclaimer

This project is an independent software project and is not affiliated with, endorsed by, or sponsored by ICOM Incorporated.

ICOM and IC-M710 are trademarks of their respective owner.

Use the software at your own risk.

The developer is not responsible for damage to radio equipment, computer equipment, serial interfaces, antennas, or other hardware resulting from use of this software.

---

# License

Copyright © 2026 4S6GGS.

See the `LICENSE` file included with this repository for the applicable license terms.

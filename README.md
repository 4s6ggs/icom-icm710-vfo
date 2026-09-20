# ICOM IC-M710 VFO Controller

**Windows desktop VFO controller for the ICOM IC-M710 HF Marine/General Coverage Transceiver**

**Developed by 4S6GGS**

---

## Latest Release

### ICOM IC-M710 VFO Controller — v1.0.6

**Current release:** `v1.0.6`

Version 1.0.6 adds a **real-time S-Meter** for the ICOM IC-M710.

### Download

**Windows executable:**

`ICOM_M710_VFO_Controller_1.0.6.exe`

No Python installation is required to run the compiled Windows executable.

[View all releases](https://github.com/4s6ggs/icom-icm710-vfo/releases)

---

## Screenshots

### v1.0.6

![ICOM IC-M710 VFO Controller v1.0.6](screenshot-v1.0.6.png)

### v1.0.5

![ICOM IC-M710 VFO Controller v1.0.5](screenshot.png)

---

## Overview

ICOM IC-M710 VFO Controller is a Windows desktop application for controlling the ICOM IC-M710 through its CI-V serial interface.

The controller provides frequency control, amateur-band quick access, operating-mode selection, mouse-wheel VFO tuning, RX/TX status, radio synchronization, audio controls, and real-time signal-strength monitoring.

---

## v1.0.6 — Real-Time S-Meter

Version 1.0.6 adds real-time signal-strength monitoring.

### S-Meter

- Real-time S-meter display
- S0–S8 signal-strength indication
- Automatic polling every 300 ms while connected and receiving
- ICOM IC-M710 `SIGM` / `ALY` response parsing
- S-meter resets to S0 when disconnected
- Polling automatically stops during TX
- Signal-level range: 0–8

### S-Meter CI-V Command

```text
PICOA,90,<RADIO_ID>,SIGM,
```

---

## Features

- Full VFO frequency control
- Configured VFO range: **1.6000–30.0000 MHz**
- Amateur-band quick selection
- USB, LSB, AM, AFS, CW and FSK modes
- Frequency readback
- RX/TX status display
- Remote ON/OFF status
- Volume control
- Speaker MUTE/UNMUTE
- Serial CI-V communication
- COM-port selection
- Baud-rate selection
- Radio ID configuration
- Controller ID configuration
- Mouse-wheel VFO tuning
- Manual tuning-speed selection
- Automatic tuning acceleration
- Real-time S-Meter
- Windows portable executable

---

## Amateur Radio Bands

| Band | Frequency Range |
|---|---|
| 160 m | 1.800–2.000 MHz |
| 80 m | 3.500–4.000 MHz |
| 60 m | 5.250–5.450 MHz |
| 40 m | 7.000–7.300 MHz |
| 30 m | 10.100–10.150 MHz |
| 20 m | 14.000–14.350 MHz |
| 17 m | 18.068–18.168 MHz |
| 15 m | 21.000–21.450 MHz |
| 12 m | 24.890–24.990 MHz |
| 10 m | 28.000–29.700 MHz |

The controller also supports the complete configured VFO range:

**1.6000 MHz → 30.0000 MHz**

---

## Operating Modes

- USB — Upper Side Band
- LSB — Lower Side Band
- AM — Amplitude Modulation
- AFS
- CW — Continuous Wave
- FSK — Frequency Shift Keying

---

## VFO Tuning

The mouse wheel can be used to tune the VFO.

Available tuning steps:

- 100 Hz
- 1 kHz
- 10 kHz
- 100 kHz
- 1 MHz

### Manual Mode

Select the required tuning step manually.

### Auto Acceleration

The tuning speed automatically increases while the mouse wheel is being used.

The maximum acceleration level can be selected from the controller.

Press **ESC** to stop active wheel tuning.

---

## Radio Control

The application communicates with the IC-M710 using the ICOM CI-V serial interface.

Supported controller functions include:

- Frequency setting
- Frequency reading
- VFO tuning
- Operating-mode control
- RX/TX status
- Remote status
- Speaker mute
- Volume control
- Radio synchronization
- Serial communication status
- Signal-strength monitoring

---

## Serial Communication

### Default Settings

| Setting | Default |
|---|---|
| COM Port | COM1 |
| Baud Rate | 4800 |
| Controller ID | 90 |
| Radio ID | 01 |

### Available Baud Rates

- 1200
- 2400
- 4800
- 9600
- 19200

Select the correct COM port and baud rate for the connected CI-V interface.

---

## System Requirements

### Operating System

- Windows 10
- Windows 11

### Hardware

- ICOM IC-M710
- Compatible CI-V serial interface
- Available Windows COM port

### Software

The compiled Windows application does not require Python to be installed.

---

## Installation

### Portable Version

1. Download `ICOM_M710_VFO_Controller_1.0.6.exe` from the v1.0.6 release.
2. Connect the IC-M710 CI-V interface.
3. Start the executable.
4. Select the correct COM port.
5. Select the correct baud rate.
6. Confirm the Radio ID.
7. Press **CONNECT**.

The application is portable and does not require a traditional Windows installation.

---

## Default Application Settings

On first startup, the controller uses:

| Setting | Default |
|---|---|
| COM Port | COM1 |
| Baud Rate | 4800 |
| Controller ID | 90 |
| Radio ID | 01 |
| Frequency | 14.2000 MHz |
| Mode | USB |
| VFO Range | FULL |
| Wheel Mode | MANUAL |
| Wheel Step | 100 Hz |
| Auto Maximum | 1 MHz |
| TRX State | RX |
| Remote Status | OFF |

---

## Connection

Before connecting:

1. Make sure the IC-M710 is powered on.
2. Connect the CI-V interface to the computer.
3. Confirm the Windows COM-port number.
4. Select the COM port in the application.
5. Select the radio's baud rate.
6. Confirm the Radio ID.
7. Press **CONNECT**.

The connection status is displayed in the controller window.

---

## RX / TX Status

The controller provides visual RX/TX status indication.

**RX**  
Indicates receive operation.

**TX**  
Indicates transmit operation.

The application also displays remote-control status.

S-Meter polling is active while connected and receiving and is stopped during TX.

---

## Audio Controls

The controller includes radio audio-related controls such as:

- Speaker mute
- Volume control
- Radio status synchronization

Actual operation depends on the functions supported by the connected IC-M710 and CI-V interface.

---

## Releases

### v1.0.6 — Current Release

**ICOM IC-M710 VFO Controller v1.0.6**

Main addition:

**Real-Time S-Meter**

Release tag:

`v1.0.6`

Executable:

`ICOM_M710_VFO_Controller_1.0.6.exe`

[View v1.0.6 release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.6)

### v1.0.5 — Previous Release

**ICOM IC-M710 VFO Controller v1.0.5**

Previous release retained in the GitHub release history.

Executable:

`ICOM_M710_VFO_Controller.exe`

[View all releases](https://github.com/4s6ggs/icom-icm710-vfo/releases)

---

## SHA-256

### v1.0.6

Executable:

`ICOM_M710_VFO_Controller_1.0.6.exe`

SHA-256:

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

Verify on Windows with:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.6.exe -Algorithm SHA256
```

### v1.0.5

Executable:

`ICOM_M710_VFO_Controller.exe`

SHA-256:

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

---

## Troubleshooting

### Cannot Connect to Radio

Check:

1. The IC-M710 is powered on.
2. The CI-V interface is connected correctly.
3. The correct Windows COM port is selected.
4. The baud rate matches the radio configuration.
5. The Radio ID is correct.
6. No other application is using the COM port.

### Frequency Does Not Change

Check the CI-V connection and confirm that the configured Radio ID matches the radio.

### S-Meter Does Not Update

Check:

1. The radio is connected.
2. The application is showing RX.
3. The CI-V interface is operating correctly.
4. The configured Radio ID is correct.

The S-Meter polling function operates while connected and receiving and stops during TX.

---

## Project

**GitHub Repository**

https://github.com/4s6ggs/icom-icm710-vfo

**Latest Release**

https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

---

## Disclaimer

This is an independent software project for controlling the ICOM IC-M710 through its serial/CI-V interface.

ICOM and IC-M710 are trademarks of their respective owner.

Use the software at your own risk and verify the correct CI-V configuration for your equipment before operating the radio.

The developer is not responsible for damage resulting from incorrect configuration, wiring, serial-interface settings, or operation of connected equipment.

---

## Developer

**4S6GGS**

**ICOM IC-M710 VFO Controller**

---

## License

See the `LICENSE` file included with this repository for the applicable license terms.

# ICOM IC-M710 VFO Controller

**Version 1.0.6**
**Developer:** 4S6GGS
**Radio:** ICOM IC-M710
**Platform:** Windows

![ICOM IC-M710 VFO Controller v1.0.6](screenshot-v1.0.6.png)

*Current v1.0.6 interface*

![ICOM IC-M710 VFO Controller v1.0.5](screenshot.png)

*Previous v1.0.5 interface*

---

## Overview

**ICOM IC-M710 VFO Controller** is a Windows desktop application for controlling the ICOM IC-M710 HF marine transceiver through its serial CI-V interface.

The application provides a graphical VFO controller with frequency selection, amateur-band shortcuts, operating-mode selection, RX/TX status, serial connection control, and mouse-wheel frequency tuning.

---

## Features

* Full VFO frequency control
* Frequency range: **1.6000 MHz – 30.0000 MHz**
* Direct frequency entry
* 100 Hz to 1 MHz mouse-wheel tuning
* Manual and automatic acceleration modes
* Amateur-band quick selection
* USB, LSB, AM, AFS, CW and FSK mode selection
* RX/TX status indication
* Remote-control status indication
* Serial COM-port selection
* Adjustable CI-V baud rate
* Radio ID and controller ID configuration
* Speaker mute control
* Volume control
* Windows standalone executable

---

## VFO Frequency Range

| Range   |   Frequency |
| ------- | ----------: |
| Minimum |  1.6000 MHz |
| Maximum | 30.0000 MHz |

---

## Amateur Band Quick Access

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

---

## Operating Modes

* USB
* LSB
* AM
* AFS
* CW
* FSK

---

## Mouse-Wheel VFO Control

Available tuning steps:

* 100 Hz
* 1 kHz
* 10 kHz
* 100 kHz
* 1 MHz

Two tuning modes are available:

* **MANUAL**
* **AUTO ACCELERATION**

---

## CI-V Serial Settings

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

Available baud rates:

* 1200
* 2400
* 4800
* 9600
* 19200

---

## Installation

The application is provided as a Windows executable.

No Python installation is required to run the packaged executable.

Download the required version from the **Releases** section of this repository and run the executable.

---

## Default Startup

* Frequency: **14.2000 MHz**
* Mode: **USB**
* VFO range: **FULL**
* Tuning step: **100 Hz**
* Wheel mode: **MANUAL**
* Maximum automatic acceleration: **1 MHz**
* Transceiver state: **RX**

---

## Releases

### v1.0.6

Current release.

**Executable:**

`ICOM_M710_VFO_Controller_1.0.6.exe`

### v1.0.5

Previous release retained for version history.

**Executable:**

`ICOM_M710_VFO_Controller.exe`

---

## File Integrity

SHA-256 checksums should be verified against the actual released executable.

The v1.0.6 checksum will be added after calculating it from the final executable.

---

## Troubleshooting

### Radio does not connect

Check:

1. Correct COM port is selected.
2. Serial cable/interface is connected.
3. Baud rate matches the radio configuration.
4. Radio ID is correct.
5. Controller ID is correct.
6. No other application is using the COM port.

### Frequency does not change

Check that:

* The serial connection is active.
* The correct radio ID is configured.
* The ICOM CI-V interface is connected correctly.
* The selected frequency is within the allowed VFO range.

---

## Project

**ICOM IC-M710 VFO Controller**

Developed for controlling the ICOM IC-M710 through the CI-V serial interface.

**Callsign:** 4S6GGS

---

## Disclaimer

This software is provided for experimental and personal use.

Use the software and radio interface at your own risk. Verify the configuration of the transceiver and serial interface before operation.

---

## License

No separate open-source license is currently specified for this project. All rights remain with the project author unless otherwise stated.

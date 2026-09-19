# ICOM IC-M710 VFO Controller
![ICOM IC-M710 VFO Controller](screenshot.png)

**Windows desktop VFO controller for the ICOM IC-M710**

Developed by **4S6GGS**

---

## ⬇️ Download

<a href="https://github.com/4s6ggs/icom-icm710-vfo/releases/latest">
<img src="https://img.shields.io/badge/⬇%20DOWNLOAD%20FOR%20WINDOWS-v1.0.5-2ea44f?style=for-the-badge&logo=windows&logoColor=white" alt="Download for Windows">
</a>

### Current Release — v1.0.5

**Windows executable:** `ICOM_M710_VFO_Controller.exe`

**No Python installation is required.**

[Download the latest Windows release](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest?utm_source=chatgpt.com)

---

## Features

* ICOM IC-M710 VFO frequency control
* Full VFO coverage
* Quick amateur-radio band selection
* Frequency entry and direct frequency setting
* Mouse-wheel VFO tuning
* Manual tuning steps
* Automatic VFO acceleration
* USB, LSB, AM, AFS, CW and FSK mode selection
* RX / TX status display
* Serial COM-port selection
* Adjustable serial baud rate
* Radio ID and controller ID configuration
* Windows desktop GUI
* Ready-to-run Windows executable

---

## Frequency Range

**Full VFO:** `1.6000 MHz – 30.0000 MHz`

Frequency display resolution:

**100 Hz**

---

## Amateur Band Quick Selection

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

## VFO Tuning Steps

The mouse-wheel controller supports:

* **100 Hz**
* **1 kHz**
* **10 kHz**
* **100 kHz**
* **1 MHz**

### Tuning Modes

* **MANUAL**
* **AUTO ACCELERATION**

---

## Operating Modes

The controller provides selection for:

* USB
* LSB
* AM
* AFS
* CW
* FSK

---

## Serial Communication

Default settings:

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

Select the COM port connected to the ICOM IC-M710 interface before connecting.

---

## Requirements

### Operating System

* Windows 10
* Windows 11

### Hardware

* ICOM IC-M710
* Compatible serial interface
* Available Windows COM port

### Software

No Python installation is required when using the released EXE.

---

## Installation

1. Open the latest release.
2. Download `ICOM_M710_VFO_Controller.exe`.
3. Save the EXE to your preferred folder.
4. Connect the ICOM IC-M710 to the computer.
5. Start `ICOM_M710_VFO_Controller.exe`.
6. Select the correct COM port.
7. Select the appropriate baud rate.
8. Click **CONNECT**.

---

## Download Verification

The SHA-256 checksum for the v1.0.5 executable is:

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

To verify the downloaded EXE on Windows, open Command Prompt in the folder containing the file and run:

```bat
certutil -hashfile ICOM_M710_VFO_Controller.exe SHA256
```

The calculated SHA-256 value should match the value shown above.

---

## Release

### v1.0.5

**Application:** ICOM IC-M710 VFO Controller

**Platform:** Windows

**Executable:** `ICOM_M710_VFO_Controller.exe`

[View all releases](https://github.com/4s6ggs/icom-icm710-vfo/releases?utm_source=chatgpt.com)

---

## Project

[GitHub Repository](https://github.com/4s6ggs/icom-icm710-vfo?utm_source=chatgpt.com)

---

## Disclaimer

This software is an independent controller application for the ICOM IC-M710.

ICOM and IC-M710 are trademarks of their respective owners.

Use the software and radio interface according to applicable radio regulations and the equipment manufacturer's documentation.

---

## License

See the repository license for licensing information.

---

**4S6GGS**
**ICOM IC-M710 VFO Controller**

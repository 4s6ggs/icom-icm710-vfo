# ICOM IC-M710 VFO Controller

**Windows desktop VFO controller for the ICOM IC-M710**

**Developer:** 4S6GGS
**Current Version:** v1.0.5

[![Download Windows EXE](https://img.shields.io/badge/Download-Windows%20EXE-blue?style=for-the-badge)](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)

---

## 📻 Download

### Windows EXE — v1.0.5

**[⬇ Download ICOM_M710_VFO_Controller.exe](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)**

The application is distributed as a Windows executable.

**Python is not required to run the released EXE.**

---

## Application

**ICOM IC-M710 VFO Controller** is a Windows desktop application for controlling an ICOM IC-M710 through a compatible computer/radio serial interface.

The controller provides frequency control, VFO tuning, operating-mode selection, radio status monitoring, and other control functions through a graphical interface.

---

## Features

* Full VFO control
* Frequency entry and SET control
* Full VFO range
* Mouse-wheel VFO tuning
* 100 Hz tuning step
* 1 kHz tuning step
* 10 kHz tuning step
* 100 kHz tuning step
* 1 MHz tuning step
* Automatic tuning acceleration
* Amateur-band quick selection
* USB mode
* LSB mode
* AM mode
* AFS mode
* CW mode
* FSK mode
* RX / TX status
* Volume control
* MUTE control
* Remote control
* Radio synchronization
* Frequency readback
* Serial communication
* COM-port selection
* Baud-rate selection

---

## Frequency Range

The controller provides a full VFO range of:

**1.6000 MHz – 30.0000 MHz**

---

## Amateur Band Quick Access

| Band  |     Frequency Range |      Start |
| ----- | ------------------: | ---------: |
| 160 m |   1.800 – 2.000 MHz |  1.800 MHz |
| 80 m  |   3.500 – 4.000 MHz |  3.500 MHz |
| 60 m  |   5.250 – 5.450 MHz |  5.250 MHz |
| 40 m  |   7.000 – 7.300 MHz |  7.000 MHz |
| 30 m  | 10.100 – 10.150 MHz | 10.100 MHz |
| 20 m  | 14.000 – 14.350 MHz | 14.000 MHz |
| 17 m  | 18.068 – 18.168 MHz | 18.068 MHz |
| 15 m  | 21.000 – 21.450 MHz | 21.000 MHz |
| 12 m  | 24.890 – 24.990 MHz | 24.890 MHz |
| 10 m  | 28.000 – 29.700 MHz | 28.000 MHz |

---

## VFO Tuning

Mouse-wheel tuning supports:

* **100 Hz**
* **1 kHz**
* **10 kHz**
* **100 kHz**
* **1 MHz**

### Manual Mode

Select the required tuning step and use the mouse wheel to change the frequency.

### Auto Acceleration

The controller can automatically increase the tuning step while the mouse wheel is being used continuously.

Press:

**ESC**

to stop active wheel tuning.

---

## Operating Modes

The controller provides the following mode selections:

| Mode |
| ---- |
| USB  |
| LSB  |
| AM   |
| AFS  |
| CW   |
| FSK  |

---

## Serial Communication

Default settings:

| Setting       | Value |
| ------------- | ----- |
| COM Port      | COM1  |
| Baud Rate     | 4800  |
| Controller ID | 90    |
| Radio ID      | 01    |

Supported baud rates:

```text
1200
2400
4800
9600
19200
```

---

## How to Use

### 1. Connect the Radio

Connect the IC-M710 to the computer using a compatible serial/CI-V interface.

### 2. Start the Radio

Turn on the IC-M710.

### 3. Start the Controller

Run:

```text
ICOM_M710_VFO_Controller.exe
```

### 4. Select COM Port

Select the COM port used by your radio interface.

### 5. Select Baud Rate

Select the baud rate configured for the radio/interface.

The default is:

```text
4800
```

### 6. Check Radio ID

The default Radio ID is:

```text
01
```

### 7. Connect

Press:

```text
CONNECT
```

### 8. Control the Radio

You can then use the VFO controller to adjust frequency, operating mode, tuning speed, and other available controls.

---

## Windows Requirements

Supported operating systems:

* Windows 10
* Windows 11

The released executable does not require Python to be installed.

A compatible serial/CI-V interface is required to communicate with the radio.

---

## Release

### v1.0.5

**Current stable release**

[Download v1.0.5](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.5)

### SHA-256

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

To verify the downloaded EXE in Windows:

```bat
certutil -hashfile ICOM_M710_VFO_Controller.exe SHA256
```

The calculated SHA-256 value should be:

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

---

## Project

GitHub repository:

https://github.com/4s6ggs/icom-icm710-vfo

Releases:

https://github.com/4s6ggs/icom-icm710-vfo/releases

Latest release:

https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

---

## Developer

**4S6GGS**

ICOM IC-M710 VFO Controller

---

## Important

The actual serial/CI-V interface, wiring, communication settings, and radio configuration must be appropriate for the IC-M710 installation.

Check the radio documentation and interface hardware before connecting the controller.

---

## Disclaimer

This is an independent software project for controlling an ICOM IC-M710 through a compatible computer/radio interface.

ICOM and IC-M710 are trademarks of their respective owners.

This project is not an official ICOM product unless explicitly stated otherwise.

---

## License

See the `LICENSE` file in the repository.

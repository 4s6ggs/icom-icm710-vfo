# ICOM IC-M710 VFO Controller

**Windows desktop VFO controller for the ICOM IC-M710 HF Marine/General Coverage Transceiver.**

Developed by **4S6GGS**

---

## 📷 Screenshot

![ICOM IC-M710 VFO Controller](screenshot.png)

---

## ⬇️ Windows Download

### Latest Release — v1.0.5

[Download the latest release](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest?utm_source=chatgpt.com)

### Portable EXE

Run the program directly without installation.

**File:**
`ICOM_M710_VFO_Controller.exe`

### Windows Installer

Install the controller with desktop and Start Menu shortcuts.

**File:**
`ICOM_M710_VFO_Controller_Setup.exe`

No Python installation is required to run the Windows EXE or installer.

---

## ✨ Features

* ICOM IC-M710 VFO control
* Full VFO frequency control
* Frequency range from **1.6000 MHz to 30.0000 MHz**
* Amateur radio band quick selection
* USB, LSB, AM, AFS, CW and FSK modes
* Frequency readback
* RX/TX status display
* Remote control status
* Speaker mute control
* Volume control
* Signal/status information
* Serial CI-V communication
* COM port selection
* Baud-rate selection
* Radio ID configuration
* Controller ID configuration
* Fast frequency tuning
* Mouse-wheel VFO tuning
* Manual tuning speed selection
* Automatic tuning acceleration
* Windows desktop application
* Portable EXE version
* Windows installer version

---

## 📻 Amateur Radio Bands

| Band | Frequency Range     |
| ---- | ------------------- |
| 160m | 1.800 – 2.000 MHz   |
| 80m  | 3.500 – 4.000 MHz   |
| 60m  | 5.250 – 5.450 MHz   |
| 40m  | 7.000 – 7.300 MHz   |
| 30m  | 10.100 – 10.150 MHz |
| 20m  | 14.000 – 14.350 MHz |
| 17m  | 18.068 – 18.168 MHz |
| 15m  | 21.000 – 21.450 MHz |
| 12m  | 24.890 – 24.990 MHz |
| 10m  | 28.000 – 29.700 MHz |

The controller also supports the complete configured VFO range:

**1.6000 MHz → 30.0000 MHz**

---

## 🎛️ Operating Modes

The controller provides quick access to:

* USB — Upper Side Band
* LSB — Lower Side Band
* AM — Amplitude Modulation
* AFS
* CW — Continuous Wave
* FSK — Frequency Shift Keying

---

## 🎚️ VFO Tuning

The mouse wheel can be used to tune the VFO.

Available tuning steps:

* 100 Hz
* 1 kHz
* 10 kHz
* 100 kHz
* 1 MHz

### Manual Mode

Select the required tuning step manually.

### Auto Acceleration

The tuning speed automatically increases while the mouse wheel is being used.

The maximum acceleration level can be selected from the controller.

---

## 📡 Radio Control

The application communicates with the IC-M710 using the ICOM CI-V serial interface.

Supported controller functions include:

* Frequency setting
* Frequency reading
* VFO tuning
* Operating-mode control
* RX/TX status
* Remote status
* Speaker mute
* Volume control
* Radio synchronization
* Serial communication status

---

## 🔌 Serial Communication

Default settings:

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

Select the correct COM port and baud rate for your CI-V interface.

---

## 💻 System Requirements

### Operating System

* Windows 10
* Windows 11

### Hardware

* ICOM IC-M710
* Compatible CI-V serial interface
* Available COM port

### Software

The compiled Windows application does **not** require Python to be installed.

---

## 📦 Installation

### Portable Version

1. Download `ICOM_M710_VFO_Controller.exe`.
2. Place the EXE anywhere on your Windows computer.
3. Connect the IC-M710 CI-V interface.
4. Start the EXE.
5. Select the correct COM port.
6. Select the correct baud rate.
7. Press **CONNECT**.

### Installer Version

1. Download `ICOM_M710_VFO_Controller_Setup.exe`.
2. Run the installer.
3. Follow the installation wizard.
4. A desktop shortcut can be created.
5. Start **ICOM IC-M710 VFO Controller**.
6. Configure the serial connection.
7. Press **CONNECT**.

---

## ⚙️ Default Application Settings

On first startup the controller uses:

```text
COM Port       : COM1
Baud Rate      : 4800
Controller ID  : 90
Radio ID       : 01
Frequency      : 14.2000 MHz
Mode           : USB
VFO Range      : FULL
```

---

## 🔄 Connection

Before connecting:

1. Make sure the IC-M710 is powered on.
2. Connect the CI-V interface to the computer.
3. Confirm the Windows COM port number.
4. Select the COM port in the application.
5. Select the radio's baud rate.
6. Confirm the Radio ID.
7. Press **CONNECT**.

The connection status is displayed in the controller window.

---

## 📊 RX / TX Status

The controller provides a visual RX/TX status indication.

**RX**

Indicates receive operation.

**TX**

Indicates transmit operation.

The application also displays the remote-control status.

---

## 🔊 Audio Controls

The controller includes radio audio-related controls such as:

* Speaker mute
* Volume control
* Radio status synchronization

These controls depend on the functions supported by the connected IC-M710 and CI-V interface.

---

## 🛠️ Release

### Version 1.0.5

**ICOM IC-M710 VFO Controller v1.0.5**

Windows desktop release.

This release provides the compiled Windows application for controlling the IC-M710 through the CI-V interface.

[View Release v1.0.5](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.5?utm_source=chatgpt.com)

---

## 🔐 SHA-256

Portable EXE:

```text
ICOM_M710_VFO_Controller.exe

SHA-256:
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

You can use the SHA-256 value to verify the integrity of the downloaded portable EXE.

---

## 📁 Release Files

The Windows release contains:

```text
ICOM_M710_VFO_Controller.exe
ICOM_M710_VFO_Controller_Setup.exe
```

The portable version can be run directly.

The installer version provides a normal Windows installation.

---

## 📺 Project

**GitHub Repository**

[4S6GGS / icom-icm710-vfo](https://github.com/4s6ggs/icom-icm710-vfo?utm_source=chatgpt.com)

**Latest Release**

[ICOM IC-M710 VFO Controller Releases](https://github.com/4s6ggs/icom-icm710-vfo/releases?utm_source=chatgpt.com)

---

## ⚠️ Disclaimer

This is an independent software project for controlling the ICOM IC-M710 through its serial/CI-V interface.

ICOM and IC-M710 are trademarks of their respective owner.

Use the software at your own risk and verify the correct CI-V configuration for your equipment before operating the radio.

The developer is not responsible for damage resulting from incorrect configuration, wiring, serial-interface settings, or operation of connected equipment.

---

## 👨‍💻 Developer

**4S6GGS**

ICOM IC-M710 VFO Controller

---

## 📜 License

See the `LICENSE` file included with this repository for the applicable license terms.

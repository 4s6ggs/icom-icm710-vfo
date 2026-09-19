# ICOM IC-M710 VFO Controller

**Windows desktop VFO controller for the ICOM IC-M710**

**Developed by 4S6GGS**

---

## 📻 About

ICOM IC-M710 VFO Controller is a Windows desktop application for computer-based control of the **ICOM IC-M710 HF marine transceiver** through a compatible serial / CI-V interface.

The controller provides frequency control, VFO tuning, amateur-band selection, operating-mode selection, radio status monitoring, volume and MUTE control, radio synchronization, and serial communication.

**Version:** `v1.0.5`

---

## ⬇️ Download for Windows

### 🟢 Portable EXE

Run the application directly without installation.

**File:**

`ICOM_M710_VFO_Controller.exe`

[Download v1.0.5 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.5?utm_source=chatgpt.com)

### 🔵 Windows Installer

Install the application with Windows shortcuts.

**File:**

`ICOM_M710_VFO_Controller_Setup.exe`

[Download v1.0.5 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.5?utm_source=chatgpt.com)

> Open the release and download the required file from **Assets**.

**No Python installation is required to use the released Windows application.**

---

## ✨ Features

### VFO Frequency Control

* Full VFO coverage from **1.6000 MHz to 30.0000 MHz**
* Direct frequency entry
* Frequency SET control
* Fast mouse-wheel tuning
* 100 Hz tuning
* 1 kHz tuning
* 10 kHz tuning
* 100 kHz tuning
* 1 MHz tuning
* Manual tuning mode
* Automatic acceleration mode
* Configurable automatic acceleration start
* Configurable maximum tuning step
* Wheel-speed reset

### Amateur Radio Band Selection

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

**FULL VFO:** `1.6000 – 30.0000 MHz`

---

## 🎙️ Operating Modes

The controller provides:

* USB
* LSB
* AM
* AFS
* CW
* FSK

The selected operating mode is displayed in the controller interface.

---

## 📡 Radio Control

The application provides:

* RX / TX control
* Speaker MUTE control
* Speaker enable / disable
* Volume control
* Remote control
* Radio synchronization
* Frequency readback
* Radio status monitoring

---

## 🔌 Serial Communication

### Default Settings

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

### Supported Baud Rates

```text
1200
2400
4800
9600
19200
```

The COM port can be selected directly from the application.

---

## 🖥️ System Requirements

### Operating System

* Windows 10
* Windows 11

### Hardware

* ICOM IC-M710
* Compatible serial / CI-V interface
* Available Windows COM port

### Software

The released Windows application is ready to run.

**Python is not required for the released EXE.**

---

## 🚀 Installation

### Portable Version

1. Download `ICOM_M710_VFO_Controller.exe`.
2. Save it anywhere on your Windows computer.
3. Connect the ICOM IC-M710 using the appropriate interface.
4. Start the EXE.
5. Select the correct COM port.
6. Select the appropriate baud rate.
7. Confirm the Radio ID.
8. Click **CONNECT**.

### Installer Version

1. Download `ICOM_M710_VFO_Controller_Setup.exe` from the release Assets.
2. Run the installer.
3. Follow the Windows installation steps.
4. Start the application from the Desktop or Start Menu.
5. Connect the ICOM IC-M710 interface.
6. Configure the COM port and communication settings.
7. Click **CONNECT**.

---

## 🖱️ Mouse-Wheel VFO Tuning

The mouse wheel can be used for rapid VFO adjustment.

Available tuning steps:

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

### Automatic Acceleration

When **AUTO ACCELERATION** is enabled, continued wheel movement can increase the tuning step up to the configured maximum.

Press **ESC** to stop active wheel tuning.

---

## 🔗 Serial Connection

Before connecting:

1. Connect the radio interface to the computer.
2. Power on the IC-M710.
3. Select the correct COM port.
4. Select the radio baud rate.
5. Confirm the Radio ID.
6. Press **CONNECT**.

> **Important:** Use an appropriate interface for your particular IC-M710 installation. Verify the radio documentation, interface hardware, wiring, and serial settings before connecting equipment.

---

## 📦 Release Information

### v1.0.5

| Item         | Information                          |
| ------------ | ------------------------------------ |
| Application  | ICOM IC-M710 VFO Controller          |
| Version      | v1.0.5                               |
| Platform     | Windows                              |
| Portable EXE | `ICOM_M710_VFO_Controller.exe`       |
| Installer    | `ICOM_M710_VFO_Controller_Setup.exe` |
| Developer    | 4S6GGS                               |

[View v1.0.5 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.5?utm_source=chatgpt.com)

[View all releases](https://github.com/4s6ggs/icom-icm710-vfo/releases?utm_source=chatgpt.com)

---

## 🔐 SHA-256 Verification

### v1.0.5 Portable EXE

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

To verify the downloaded EXE in Windows Command Prompt:

```bat
certutil -hashfile ICOM_M710_VFO_Controller.exe SHA256
```

Compare the generated SHA-256 value with the value shown above.

---

## 📸 Application

The project provides a Windows graphical control interface for the ICOM IC-M710, including VFO, band, mode, serial communication, RX/TX, volume, MUTE, and radio-status controls.

---

## ⚠️ Disclaimer

This is an independent software project for controlling an ICOM IC-M710 through a compatible computer/radio interface.

ICOM and IC-M710 are trademarks of their respective owners. This project is not presented as an official ICOM product unless explicitly stated otherwise.

Always verify the correct radio configuration, interface hardware, serial settings, operating limits, and applicable regulations before operating the transceiver.

---

## 📄 License

See the [`LICENSE`](LICENSE) file in this repository for licensing information.

---

## 👨‍💻 Developer

**4S6GGS**

**ICOM IC-M710 VFO Controller**

[GitHub Repository](https://github.com/4s6ggs/icom-icm710-vfo?utm_source=chatgpt.com)

---

### ⭐ Support the Project

If you find the ICOM IC-M710 VFO Controller useful, consider giving the repository a ⭐ on GitHub.

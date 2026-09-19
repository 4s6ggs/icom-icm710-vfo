# ICOM IC-M710 VFO Controller

**Windows desktop VFO controller for the ICOM IC-M710**

**Developed by 4S6GGS**

---

![ICOM IC-M710 VFO Controller](screenshot.png)

## ⬇️ Download

### Windows — v1.0.5

<a href="https://github.com/4s6ggs/icom-icm710-vfo/releases/latest">
<img src="https://img.shields.io/badge/⬇%20DOWNLOAD%20LATEST%20RELEASE-v1.0.5-2ea44f?style=for-the-badge&logo=windows&logoColor=white" alt="Download Latest Release">
</a>

### 🟢 Portable EXE

**`ICOM_M710_VFO_Controller.exe`**

Run the controller directly without installation.

<a href="https://github.com/4s6ggs/icom-icm710-vfo/releases/latest">
<img src="https://img.shields.io/badge/⬇%20DOWNLOAD-PORTABLE%20EXE-4CAF50?style=for-the-badge&logo=windows&logoColor=white" alt="Download Portable EXE">
</a>

### 🔵 Windows Installer

**`ICOM_M710_VFO_Controller_Setup.exe`**

Install the application with Windows Start Menu and Desktop shortcuts.

<a href="https://github.com/4s6ggs/icom-icm710-vfo/releases/latest">
<img src="https://img.shields.io/badge/⬇%20DOWNLOAD-WINDOWS%20INSTALLER-1976D2?style=for-the-badge&logo=windows&logoColor=white" alt="Download Windows Installer">
</a>

> Both files are available under **Assets** in the latest GitHub Release.

**No Python installation is required.**

---

## 📻 About

ICOM IC-M710 VFO Controller is a Windows desktop application designed to provide convenient computer control of the **ICOM IC-M710**.

The application provides frequency control, band selection, operating-mode selection, VFO tuning, serial communication and radio status functions through a simple Windows GUI.

---

## ✨ Features

* Full VFO frequency control
* Frequency range from **1.6000 MHz to 30.0000 MHz**
* Direct frequency entry
* Quick amateur-band selection
* Mouse-wheel VFO tuning
* 100 Hz tuning resolution
* 1 kHz tuning
* 10 kHz tuning
* 100 kHz tuning
* 1 MHz tuning
* Manual tuning mode
* Automatic VFO acceleration
* USB mode
* LSB mode
* AM mode
* AFS mode
* CW mode
* FSK mode
* RX / TX status display
* Serial COM-port selection
* Adjustable baud rate
* Radio ID selection
* Controller ID configuration
* Windows desktop interface
* Portable EXE version
* Windows installer version

---

## 📡 Full VFO Range

**1.6000 MHz – 30.0000 MHz**

Frequency display resolution:

**100 Hz**

---

## 📻 Amateur Radio Bands

| Band  |     Frequency Range | Start Frequency |
| ----- | ------------------: | --------------: |
| 160 m |   1.800 – 2.000 MHz |       1.800 MHz |
| 80 m  |   3.500 – 4.000 MHz |       3.500 MHz |
| 60 m  |   5.250 – 5.450 MHz |       5.250 MHz |
| 40 m  |   7.000 – 7.300 MHz |       7.000 MHz |
| 30 m  | 10.100 – 10.150 MHz |      10.100 MHz |
| 20 m  | 14.000 – 14.350 MHz |      14.000 MHz |
| 17 m  | 18.068 – 18.168 MHz |      18.068 MHz |
| 15 m  | 21.000 – 21.450 MHz |      21.000 MHz |
| 12 m  | 24.890 – 24.990 MHz |      24.890 MHz |
| 10 m  | 28.000 – 29.700 MHz |      28.000 MHz |

---

## 🎛️ VFO Tuning

Available tuning steps:

| Step   | Resolution |
| ------ | ---------: |
| Step 1 |     100 Hz |
| Step 2 |      1 kHz |
| Step 3 |     10 kHz |
| Step 4 |    100 kHz |
| Step 5 |      1 MHz |

### Tuning Modes

* **MANUAL**
* **AUTO ACCELERATION**

Use the mouse wheel over the VFO control for fast frequency adjustment.

Press **ESC** to stop active wheel tuning.

---

## 🎙️ Operating Modes

The controller supports:

* **USB** — Upper Sideband
* **LSB** — Lower Sideband
* **AM** — Amplitude Modulation
* **AFS**
* **CW** — Continuous Wave
* **FSK** — Frequency Shift Keying

---

## 🔌 Serial Communication

Default communication settings:

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

Select the COM port connected to the ICOM IC-M710 interface before pressing **CONNECT**.

---

## 🖥️ System Requirements

### Operating System

* Windows 10
* Windows 11

### Hardware

* ICOM IC-M710
* Compatible serial interface
* Available Windows COM port

### Software

No Python installation is required for the released Windows executable.

---

## 🚀 Installation

### Option 1 — Portable EXE

1. Download `ICOM_M710_VFO_Controller.exe`.
2. Save it anywhere on your Windows computer.
3. Double-click the EXE.
4. Connect your ICOM IC-M710 interface.
5. Select the correct COM port.
6. Select the appropriate baud rate.
7. Click **CONNECT**.

### Option 2 — Windows Installer

1. Download `ICOM_M710_VFO_Controller_Setup.exe`.
2. Run the installer.
3. Follow the installation steps.
4. Use the Desktop or Start Menu shortcut.
5. Connect your ICOM IC-M710 interface.
6. Start the controller.

---

## 🔐 Download Verification

### SHA-256 — v1.0.5

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

To verify the portable EXE on Windows:

```bat
certutil -hashfile ICOM_M710_VFO_Controller.exe SHA256
```

Compare the generated SHA-256 value with the value above.

---

## 📦 Release Information

### Version 1.0.5

| Item          | Information                          |
| ------------- | ------------------------------------ |
| Application   | ICOM IC-M710 VFO Controller          |
| Version       | v1.0.5                               |
| Platform      | Windows                              |
| Portable File | `ICOM_M710_VFO_Controller.exe`       |
| Installer     | `ICOM_M710_VFO_Controller_Setup.exe` |
| Developer     | 4S6GGS                               |

[View v1.0.5 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.5?utm_source=chatgpt.com)

[View All Releases](https://github.com/4s6ggs/icom-icm710-vfo/releases?utm_source=chatgpt.com)

---

## 📂 Project Files

The public repository provides the compiled Windows application and release documentation.

The Python source code is **not included in the public release**.

---

## ⚠️ Disclaimer

This software is an independent controller application for the ICOM IC-M710.

ICOM and IC-M710 are trademarks of their respective owners.

The user is responsible for ensuring that operation of the radio and software complies with applicable laws, regulations, licensing requirements and equipment documentation.

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

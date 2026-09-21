# 📻 ICOM IC-M710 VFO Controller

### Windows VFO Controller for the ICOM IC-M710

**Developer:** 4S6GGS
**Latest Version:** **v1.0.7**
**Platform:** Windows 10 / Windows 11

---

# 📥 Download

## 🆕 ICOM IC-M710 VFO Controller — v1.0.7

**Windows Portable Application**

> The v1.0.7 executable should be added to the GitHub Release before publishing the download link.

### Download v1.0.7

**[⬇️ Download ICOM_M710_VFO_Controller_1.0.7.exe](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)**

No Python installation is required.

The application is portable — run the `.exe` directly.

---

# 📸 Screenshots

## 🆕 v1.0.7 — Main Controller

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.6.png)

## 🆕 v1.0.7 — Controller Interface

![ICOM IC-M710 VFO Controller v1.0.7](screenshot.png)

> These are the two screenshot files currently stored in the repository and are presented as the current v1.0.7 interface screenshots.

---

# ✨ Features

* 🎛️ Full VFO control
* 📻 Amateur-band quick selection
* 🖱️ Mouse-wheel tuning
* ⚡ Automatic tuning acceleration
* 🎚️ USB / LSB / AM / AFS / CW / FSK
* 📶 Real-time S-Meter
* 🎯 RIT control
* 📊 RF Level control
* 🔌 COM-port configuration
* 🖥️ COM-port monitor
* 🟢 RX / 🔴 TX indication
* 📡 Remote status
* 🔊 Volume control
* 🔇 Speaker mute
* 🔄 Frequency readback
* 🔌 ICOM CI-V communication

---

# 🆕 v1.0.7

## 🔌 Communication & Radio Control

### Added

* 🔌 Dedicated Communication / COM page
* 🖥️ COM Port Monitor
* 🎯 RIT Control
* 📊 RF Level Control

### Improved

* Serial communication workflow
* Communication monitoring
* Radio-control operation

---

# 📶 v1.0.6

## S-Meter

Added real-time signal-strength monitoring.

* 📶 S0–S8 display
* 🔄 Automatic polling
* 🟢 RX polling
* 🔴 Stops during TX
* 🔄 Resets to S0 after disconnect

---

# 🎛️ v1.0.5

## Core VFO Controller

The original controller release.

* 🎛️ Frequency control
* 📻 Band selection
* 🎚️ Mode selection
* 🖱️ Mouse-wheel tuning
* ⚡ Auto acceleration
* 🔄 Frequency readback
* 🟢 RX / 🔴 TX status
* 📡 Remote status
* 🔊 Volume
* 🔇 Speaker mute
* 🔌 CI-V communication

---

# 📻 Amateur Radio Bands

| Band  | Frequency         |
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

### Full VFO

**1.6000 MHz → 30.0000 MHz**

---

# 🎚️ Operating Modes

| Mode | Description            |
| ---- | ---------------------- |
| USB  | Upper Side Band        |
| LSB  | Lower Side Band        |
| AM   | Amplitude Modulation   |
| AFS  | AFS                    |
| CW   | Continuous Wave        |
| FSK  | Frequency Shift Keying |

---

# 🖱️ VFO Tuning

Mouse-wheel tuning supports:

* **100 Hz**
* **1 kHz**
* **10 kHz**
* **100 kHz**
* **1 MHz**

### MANUAL

Select the tuning step manually.

### AUTO ACCELERATION

The tuning speed increases automatically while tuning.

Press **ESC** to stop active wheel tuning.

---

# 📡 Radio Control

The controller communicates with the IC-M710 through the ICOM CI-V serial interface.

Supported functions include:

* Frequency setting
* Frequency readback
* VFO tuning
* Mode control
* RX / TX status
* Remote status
* Volume
* Speaker mute
* RIT
* RF Level
* S-Meter
* Serial communication

---

# 🔌 Communication Settings

## Default

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

## Baud Rates

```text
1200
2400
4800
9600
19200
```

---

# 🖥️ COM Port Monitor

The COM monitor allows the CI-V communication to be observed.

```text
┌──────────────┐
│  PC / VFO    │
│  Controller  │
└──────┬───────┘
       │
       │ CI-V
       ▼
┌──────────────┐
│  ICOM IC-M710│
└──────────────┘
```

Useful for checking:

* Commands
* Radio responses
* Serial activity
* Interface problems
* Communication status

---

# 🎯 RIT

**RIT — Receive Incremental Tuning**

Allows fine receive-frequency adjustment without changing the main transmit frequency.

Available in **v1.0.7**.

---

# 📊 RF Level

RF Level control is available from the controller in **v1.0.7**.

---

# 📶 S-Meter

The real-time S-Meter was introduced in **v1.0.6**.

```text
S0 ─ S1 ─ S2 ─ S3 ─ S4 ─ S5 ─ S6 ─ S7 ─ S8
```

The S-Meter operates while connected and receiving and stops during TX.

---

# 🟢 RX / 🔴 TX

```text
🟢 RX  = Receive
🔴 TX  = Transmit
```

The controller displays the current radio operating state.

---

# 🔊 Audio

Available audio-related controls include:

* 🔊 Volume
* 🔇 Speaker MUTE / UNMUTE

---

# 🚀 Quick Start

### 1. Connect

```text
Windows PC
     │
     ▼
USB / Serial Interface
     │
     ▼
ICOM IC-M710
```

### 2. Find the COM Port

Open:

**Windows Device Manager → Ports (COM & LPT)**

### 3. Start the Controller

Run the downloaded `.exe`.

### 4. Configure

Select:

* COM Port
* Baud Rate
* Controller ID
* Radio ID

### 5. Connect

Press:

**CONNECT**

### 6. Test

Check:

* Frequency
* Mode
* RX / TX
* Remote
* S-Meter
* RIT
* RF Level

---

# ⚙️ Default Application Settings

| Setting       | Default     |
| ------------- | ----------- |
| Frequency     | 14.2000 MHz |
| Mode          | USB         |
| VFO Range     | FULL        |
| COM Port      | COM1        |
| Baud Rate     | 4800        |
| Controller ID | 90          |
| Radio ID      | 01          |
| Wheel Mode    | MANUAL      |
| Wheel Step    | 100 Hz      |
| Auto Maximum  | 1 MHz       |
| TRX State     | RX          |
| Remote        | OFF         |

---

# 💻 System Requirements

### Operating System

* Windows 10
* Windows 11

### Hardware

* ICOM IC-M710
* Compatible CI-V interface
* Available COM port

### Software

No Python installation is required for the compiled Windows application.

---

# 🔧 Hardware Interface

```text
┌───────────────┐
│  Windows PC   │
└───────┬───────┘
        │ USB
        ▼
┌───────────────┐
│ USB / Serial  │
│   Interface   │
└───────┬───────┘
        │ CI-V
        ▼
┌───────────────┐
│   ICOM IC-M710│
└───────────────┘
```

⚠️ Verify the IC-M710 connector, pinout, signal levels and interface circuitry before connecting hardware.

---

# 🆔 Radio ID

Default controller setting:

```text
Radio ID = 01
```

The radio's configured ID must match the controller.

---

# 🔀 REMT-ID / REMT-IF

### REMT-ID

Radio identification.

```text
REMT-ID = 01
```

### REMT-IF

Remote-control interface selection.

These are separate radio settings.

---

# 🛠️ Troubleshooting

## Cannot Connect

Check:

* Radio power
* COM port
* Baud rate
* Radio ID
* Controller ID
* CI-V interface
* Cable
* Other programs using the COM port

## Frequency Does Not Change

Check the CI-V connection, COM settings and Radio ID.

## S-Meter Does Not Update

Check that:

* Radio is connected
* Controller shows RX
* CI-V communication is working
* Radio ID is correct

## COM Monitor Is Empty

Check the COM port, USB/serial interface, cable and driver.

---

# 📋 Version History

## v1.0.7 — Communication & Control

* 🔌 COM / Communication page
* 🖥️ COM Port Monitor
* 🎯 RIT
* 📊 RF Level
* 🔄 Communication improvements

## v1.0.6 — S-Meter

* 📶 Real-time S-Meter
* S0–S8 indication
* Automatic polling
* RX/TX handling

## v1.0.5 — Core Controller

* 🎛️ VFO
* 📻 Bands
* 🎚️ Modes
* 🖱️ Mouse-wheel tuning
* ⚡ Acceleration
* 🔊 Audio
* 🔌 CI-V

---

# 📦 Files

Current repository contains:

```text
ICOM_M710_VFO_Controller.exe
ICOM_M710_VFO_Controller_1.0.6.exe
README.md
screenshot-v1.0.6.png
screenshot.png
```

---

# 🔐 SHA-256

## v1.0.6

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

## v1.0.5

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

Verify on Windows:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.6.exe -Algorithm SHA256
```

---

# 📥 Downloads

### 🆕 v1.0.7

**[⬇️ Download Latest Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)**

### v1.0.6

**[⬇️ Download ICOM_M710_VFO_Controller_1.0.6.exe](https://github.com/4s6ggs/icom-icm710-vfo/releases)**

### v1.0.5

**[⬇️ Download Previous Release](https://github.com/4s6ggs/icom-icm710-vfo/releases)**

---

# 👨‍💻 Developer

## 4S6GGS

**ICOM IC-M710 VFO Controller**

---

# ⚠️ Disclaimer

This is an independent software project for controlling the ICOM IC-M710 through its serial / CI-V interface.

ICOM and IC-M710 are trademarks of their respective owner.

Use the software at your own risk. Verify the correct CI-V configuration, connector wiring, interface circuitry and radio settings before operation.

---

# 🔗 Project

**[GitHub Repository](https://github.com/4s6ggs/icom-icm710-vfo)**

**[Latest Releases](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest)**

---

# 📻 ICOM IC-M710 VFO Controller

### **4S6GGS • v1.0.7**

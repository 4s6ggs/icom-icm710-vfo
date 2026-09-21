# 📻 ICOM IC-M710 VFO Controller

### Windows VFO & Remote-Control Application

**Developer:** 4S6GGS
**Current Version:** **v1.0.7**
**Platform:** Windows 10 / Windows 11

---

## 📸 Screenshots

### 🆕 v1.0.7 — Main Controller

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.6.png)

### 🆕 v1.0.7 — Controller Interface

![ICOM IC-M710 VFO Controller v1.0.7](screenshot.png)

> The two existing repository screenshots are displayed here as the current **v1.0.7** interface screenshots.

---

# 📡 Overview

The **ICOM IC-M710 VFO Controller** is a Windows desktop application for controlling the ICOM IC-M710 through a compatible serial / CI-V remote-control interface.

The application provides a graphical interface for:

* 🎛️ Frequency control
* 📻 VFO tuning
* 📡 Amateur-band selection
* 🎚️ Operating modes
* 📶 S-Meter
* 🔊 Audio control
* 🎯 RIT
* 📊 RF Level
* 🔌 COM-port configuration
* 🖥️ COM-port monitoring
* 🟢 RX / 🔴 TX status
* 📡 Remote status

> ⚠️ The radio, interface, connector wiring and electrical levels must be correctly configured before use.

---

# ✨ Features

| Feature             | Description                     |
| ------------------- | ------------------------------- |
| 🎛️ Full VFO        | 1.6000–30.0000 MHz              |
| 📻 Band Selection   | Quick amateur-band access       |
| 🖱️ Mouse Wheel     | VFO tuning                      |
| ⚡ Auto Acceleration | Automatic tuning-speed increase |
| 🎚️ Modes           | USB, LSB, AM, AFS, CW, FSK      |
| 📶 S-Meter          | Real-time S0–S8                 |
| 🎯 RIT              | Receive incremental tuning      |
| 📊 RF Level         | RF level control                |
| 🔌 COM Page         | Communication configuration     |
| 🖥️ COM Monitor     | Serial communication monitoring |
| 🔊 Audio            | Volume and speaker mute         |
| 🔄 Readback         | Radio synchronization           |

---

# 🆕 v1.0.7

## 🔌 Communication & Control

**v1.0.7** focuses on communication and additional radio controls.

### Added

* 🔌 Dedicated COM / Communication page
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

**v1.0.6** introduced real-time signal-strength monitoring.

### Added

* 📶 Real-time S-Meter
* S0–S8 indication
* Automatic polling
* RX/TX-aware polling
* S0 reset after disconnect

---

# 🎛️ v1.0.5

## Core VFO Controller

**v1.0.5** established the main controller functions.

### Added

* 🎛️ Frequency control
* 📻 Band selection
* 🎚️ Mode selection
* 🖱️ Mouse-wheel tuning
* ⚡ Automatic acceleration
* 🔄 Frequency readback
* 🟢 RX / 🔴 TX status
* 📡 Remote status
* 🔊 Volume
* 🔇 Speaker mute
* 🔌 CI-V communication

---

# 🎛️ VFO Control

## Full VFO

```text
1.6000 MHz ───────────────────────────── 30.0000 MHz
```

### Tuning Steps

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

### Manual Mode

Select the required tuning step manually.

### Auto Acceleration

The tuning speed automatically increases while the mouse wheel is being used.

Press **ESC** to stop active wheel tuning.

---

# 📻 Amateur Radio Bands

| Band  | Frequency Range   |
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

### Full VFO Range

**1.6000 MHz → 30.0000 MHz**

---

# 🎚️ Operating Modes

```text
USB
LSB
AM
AFS
CW
FSK
```

---

# 📡 Radio Control

The application communicates with the IC-M710 using the ICOM CI-V serial interface.

Supported controls include:

* Frequency setting
* Frequency readback
* VFO tuning
* Operating-mode control
* RX / TX status
* Remote status
* Volume
* Speaker mute
* RIT
* RF Level
* S-Meter
* Serial communication monitoring

---

# 🔌 Communication

## Default Settings

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

The COM Monitor allows serial communication to be observed during operation.

```text
┌──────────────┐
│   Controller │
└──────┬───────┘
       │
       │ CI-V
       ▼
┌──────────────┐
│   IC-M710    │
└──────────────┘
```

Useful for checking:

* Commands
* Radio responses
* Serial activity
* Communication problems
* Interface operation

---

# 🎯 RIT Control

**RIT — Receive Incremental Tuning**

RIT provides fine receive-frequency adjustment without changing the main transmit frequency.

Available in **v1.0.7**.

---

# 📊 RF Level

RF Level control is available from the main controller in **v1.0.7**.

---

# 📶 S-Meter

The S-Meter provides real-time signal-strength information.

```text
S0 ─ S1 ─ S2 ─ S3 ─ S4 ─ S5 ─ S6 ─ S7 ─ S8
```

### v1.0.6

* Automatic polling
* RX-only operation
* Stops during TX
* S0 after disconnect

---

# 🟢 RX / 🔴 TX

```text
🟢 RX  = Receive
🔴 TX  = Transmit
```

The controller displays the current radio operating state.

---

# 🔊 Audio Controls

The controller provides:

* 🔊 Volume control
* 🔇 Speaker MUTE / UNMUTE
* 🔄 Radio status synchronization

---

# 🖥️ System Requirements

### Operating System

* Windows 10
* Windows 11

### Hardware

* ICOM IC-M710
* Compatible CI-V serial interface
* Available Windows COM port

### Software

The compiled Windows application does **not** require Python to be installed.

---

# 🚀 Quick Start

### 1. Connect the Radio

```text
Windows PC
     │
     ▼
USB / Serial Interface
     │
     ▼
ICOM IC-M710
```

### 2. Check Windows COM Port

Open:

```text
Device Manager
    ↓
Ports (COM & LPT)
```

### 3. Start the Controller

Run the released Windows executable.

### 4. Select

```text
COM Port
Baud Rate
Controller ID
Radio ID
```

### 5. Press

```text
CONNECT
```

### 6. Test

Check:

```text
Frequency
Mode
RX / TX
Remote
S-Meter
RIT
RF Level
```

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

# 🔧 Hardware Interface

A suitable interface is required between the Windows computer and the IC-M710.

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
│   IC-M710     │
└───────────────┘
```

> ⚠️ Do not assume a generic USB-to-UART adapter can be connected directly to the radio. Verify the radio connector, pinout, signal levels and interface circuitry.

---

# 🔧 CP2102

A CP2102 module may be used as the USB-to-serial portion of a suitable interface.

The CP2102 itself does **not** define the correct IC-M710 radio-side electrical interface.

> ⚠️ Verify the complete interface circuit before connecting it to the radio.

---

# 🆔 Radio ID

The radio ID must match the controller configuration.

Example:

```text
Radio ID = 01
```

Controller default:

```text
Radio ID = 01
```

---

# 🔀 REMT-ID / REMT-IF

These are different radio settings.

### REMT-ID

Identifies the radio.

```text
REMT-ID = 01
```

### REMT-IF

Selects the remote-control interface.

```text
REMT-IF = configured interface
```

> **REMT-ID is not the same as REMT-IF.**

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
* Another application using the COM port

---

## Frequency Does Not Change

Check:

* CI-V connection
* Radio ID
* Baud rate
* COM port
* COM Monitor

---

## S-Meter Does Not Update

Check:

* Radio is connected
* Radio is in RX
* CI-V communication
* Radio ID

S-Meter polling stops during TX.

---

## COM Monitor Has No Activity

Check:

* COM port
* USB/serial interface
* Cable
* Driver
* Connection
* Whether another program has opened the COM port

---

# 📦 Releases

| Version    | Main Change                          |
| ---------- | ------------------------------------ |
| **v1.0.7** | COM page, COM Monitor, RIT, RF Level |
| **v1.0.6** | Real-time S-Meter                    |
| **v1.0.5** | Core VFO Controller                  |

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

Verify a Windows executable with:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.6.exe -Algorithm SHA256
```

---

# 📁 Repository Files

Current repository structure:

```text
icom-icm710-vfo/
│
├── ICOM_M710_VFO_Controller.exe
├── ICOM_M710_VFO_Controller_1.0.6.exe
├── README.md
├── screenshot-v1.0.6.png
└── screenshot.png
```

---

# ⚠️ Disclaimer

This is an independent software project for controlling the ICOM IC-M710 through its serial / CI-V interface.

ICOM and IC-M710 are trademarks of their respective owner.

Use the software at your own risk. Verify the correct CI-V configuration, connector wiring, interface circuitry and radio settings before operation.

The developer is not responsible for damage resulting from incorrect configuration, wiring, serial-interface settings or operation of connected equipment.

---

# 👨‍💻 Developer

**4S6GGS**

### ICOM IC-M710 VFO Controller

**Current Version: v1.0.7**

---

# 🔗 Project

[GitHub Repository](https://github.com/4s6ggs/icom-icm710-vfo?utm_source=chatgpt.com)

[GitHub Releases](https://github.com/4s6ggs/icom-icm710-vfo/releases?utm_source=chatgpt.com)

---

## 📻 ICOM IC-M710 VFO Controller

### **4S6GGS • v1.0.7**

# ICOM IC-M710 VFO Controller

**Version 1.0.7**
**Developed by 4S6GGS**

A Windows desktop VFO controller for the **ICOM IC-M710** marine HF transceiver using the radio's **CI-V serial control interface**.

Designed for amateur-radio and SWL use, the controller provides frequency tuning, operating-mode selection, radio-status monitoring, S-Meter display, RIT control, and serial communication monitoring from a simple Windows interface.

---

## 📸 Screenshot

![ICOM IC-M710 VFO Controller v1.0.7](screenshot-v1.0.7.png)

---

## 🚀 Latest Release — v1.0.7

**Current release: v1.0.7**

[Download ICOM IC-M710 VFO Controller v1.0.7](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7?utm_source=chatgpt.com)

### v1.0.7 Changes

* Added a dedicated **COM Port Setup** page.
* Added **COM Monitor** to the COM Port Setup page.
* Added **RIT Control** to the Main page.
* Improved COM-port configuration and monitoring.
* Improved the radio-control workflow.

### v1.0.7 Executable

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

### SHA-256

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

### Verify the Download

PowerShell:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.7.exe -Algorithm SHA256
```

The calculated hash should match:

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

---

## 📖 User Guide

The complete beginner-friendly operating and installation guide is available here:

[**Read the Complete User Guide**](docs/USER_GUIDE.md)

The guide covers:

* IC-M710 connection
* CI-V communication
* Radio ID configuration
* COM-port setup
* COM Monitor
* Frequency control
* Amateur-band selection
* Operating modes
* Mouse-wheel tuning
* Auto acceleration
* RIT
* RX/TX status
* Remote status
* Volume and speaker mute
* S-Meter
* Troubleshooting
* DIY CP2102 USB interface information
* Clone/remote-control cable construction
* SHA-256 verification

---

# ✨ Features

## Main VFO Control

* Frequency range: **1.6000–30.0000 MHz**
* Direct frequency entry
* Frequency readback from the radio
* Full VFO mode
* Amateur-band quick selection
* Mouse-wheel frequency tuning
* Manual tuning steps:

  * 100 Hz
  * 1 kHz
  * 10 kHz
  * 100 kHz
  * 1 MHz
* Automatic tuning acceleration
* ESC key to stop tuning activity

## Operating Modes

Supported modes:

* USB
* LSB
* AM
* AFS
* CW
* FSK

## Radio Status

The controller displays:

* RX / TX state
* Remote status
* Current frequency
* Current operating mode
* S-Meter signal level

## RIT Control

Version 1.0.7 adds **RIT Control** directly to the Main page for receiver incremental tuning.

## S-Meter

Version 1.0.6 introduced real-time S-Meter monitoring.

The S-Meter:

* Displays **S0–S8**
* Updates approximately every **300 ms** while connected and receiving
* Uses the IC-M710 `SIGM` / `ALY` response
* Stops polling during TX
* Resets to S0 when disconnected

Signal-level range:

```text
S0 → S8
```

CI-V command used:

```text
PICOA,90,<RADIO_ID>,SIGM,
```

---

# 📡 Amateur Band Quick Selection

| Band  |   Frequency Range | Default Start |
| ----- | ----------------: | ------------: |
| 160 m |   1.800–2.000 MHz |     1.800 MHz |
| 80 m  |   3.500–4.000 MHz |     3.500 MHz |
| 60 m  |   5.250–5.450 MHz |     5.250 MHz |
| 40 m  |   7.000–7.300 MHz |     7.000 MHz |
| 30 m  | 10.100–10.150 MHz |    10.100 MHz |
| 20 m  | 14.000–14.350 MHz |    14.000 MHz |
| 17 m  | 18.068–18.168 MHz |    18.068 MHz |
| 15 m  | 21.000–21.450 MHz |    21.000 MHz |
| 12 m  | 24.890–24.990 MHz |    24.890 MHz |
| 10 m  | 28.000–29.700 MHz |    28.000 MHz |

> **Note:** Frequency ranges are provided as controller quick-selection ranges. Always observe the applicable operating privileges, band plans, and regulations for your location.

---

# 🔌 CI-V Serial Control

The controller communicates with the IC-M710 through its CI-V serial interface.

### Default Serial Configuration

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

The **Controller ID** and **Radio ID** are separate values.

```text
Controller ID = 90
Radio ID      = 01
```

The Radio ID must correspond to the IC-M710 configuration.

---

# ⚙️ Default Settings

When the application starts, the default configuration is:

| Setting       | Default            |
| ------------- | ------------------ |
| Frequency     | 14.2000 MHz        |
| Mode          | USB                |
| VFO Range     | FULL               |
| VFO Range     | 1.6000–30.0000 MHz |
| COM Port      | COM1               |
| Baud Rate     | 4800               |
| Controller ID | 90                 |
| Radio ID      | 01                 |
| Wheel Mode    | MANUAL             |
| Wheel Step    | 100 Hz             |
| Auto Maximum  | 1 MHz              |
| TRX State     | RX                 |
| Remote        | OFF                |

---

# 🖥️ System Requirements

### Operating System

* Windows 10
* Windows 11

### Radio

* ICOM IC-M710

### Interface

A compatible CI-V serial interface is required.

The interface may be:

* A suitable commercial CI-V interface
* A compatible USB-to-serial interface
* A properly constructed DIY interface

### Python

**Python is not required** to run the released EXE.

The public release provides the compiled Windows executable. Python source code is not included in the public release.

---

# 🔧 DIY CP2102 Interface

Users who want to build their own USB serial radio interface can use a CP2102-based USB interface as a starting point.

A useful general reference is:

[DIY Universal Radio Clone Cable Using CP2102 USB Interface — Instructables](https://www.instructables.com/DIY-Universal-Radio-Clone-Cable-Using-CP2102-USB-I?utm_source=chatgpt.com)

The project demonstrates a CP2102 USB interface with TX/RX isolation and a common radio clone bus.

**Important:** This is provided as a general DIY USB-radio-interface reference. It is **not claimed to be a direct IC-M710 connection circuit**.

Before connecting any DIY interface to an IC-M710:

1. Verify the IC-M710 connector pinout.
2. Verify the electrical interface requirements.
3. Verify signal polarity and voltage levels.
4. Confirm the correct CI-V/remote-control interface configuration.
5. Check all wiring before powering the radio.

Do not connect a CP2102 module directly to the IC-M710 connector unless the required interface circuitry and electrical compatibility have been verified.

For complete construction information and troubleshooting, see:

[**DIY CP2102 / Clone Cable Guide**](docs/USER_GUIDE.md)

---

# 📻 Finding the IC-M710 Radio ID

The IC-M710 Radio ID can be checked from the radio's setup mode.

### Procedure

1. Turn the IC-M710 **OFF**.
2. Press and hold **FUNC + 1**.
3. Turn the radio **ON** while continuing to hold the controls as required.
4. The radio enters its setup mode.
5. Use the **GROUP selector / left knob** to navigate the setup items.
6. Locate the remote-control settings.
7. The display will show the remote ID information, for example:

```text
REMT -- ID 01
```

The value after `ID` is the radio's **Radio ID**.

Example:

```text
REMT -- ID 01
```

means:

```text
Radio ID = 01
```

The `REMT -- IF` item refers to the remote-control interface selection and is **not the Radio ID**.

For detailed instructions and interface information, see the [**User Guide**](docs/USER_GUIDE.md).

---

# 📡 COM Port Setup

Version 1.0.7 provides a separate **COM Port Setup** page.

It allows the operator to configure:

* Windows COM port
* Baud rate
* Controller ID
* Radio ID

The page also includes the **COM Monitor**.

This makes it easier to check serial communication between the computer and IC-M710 before using the main VFO controls.

---

# 🔍 COM Monitor

The COM Monitor provides visibility into serial communication.

It can be useful for checking:

* Commands sent by the controller
* Responses received from the radio
* Communication timing
* Incorrect COM-port selection
* Incorrect baud rate
* Radio-ID configuration problems

If the radio does not respond correctly, the COM Monitor can help determine whether communication is actually taking place.

---

# 🎛️ Mouse-Wheel Tuning

The frequency display supports mouse-wheel tuning.

### Manual Steps

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

The selected step determines how much the frequency changes for each wheel movement.

### Auto Acceleration

The controller can automatically increase the tuning step while the mouse wheel is being rotated continuously.

The available acceleration range is configurable from the selected starting step up to the selected maximum step.

The default maximum acceleration is:

```text
1 MHz
```

### Reset

Use **RESET** to return the wheel-tuning state to its initial configuration.

Press **ESC** to stop active wheel tuning.

---

# 🔊 Audio Controls

The controller provides:

* Volume control
* Speaker mute

These controls allow basic audio adjustment from the computer interface.

---

# 📦 Releases

## v1.0.7

**Current release**

![v1.0.7](screenshot-v1.0.7.png)

Changes:

* Separate COM Port Setup page
* COM Monitor
* RIT Control on Main page
* Improved COM-port configuration
* Improved COM monitoring
* Improved radio-control workflow

[View v1.0.7 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7?utm_source=chatgpt.com)

---

## v1.0.6

![v1.0.6](screenshot-v1.0.6.png)

### v1.0.6 Changes

* Added real-time S-Meter display.
* Added IC-M710 signal-level polling.
* Improved radio-status monitoring.

### v1.0.6 Executable

```text
ICOM_M710_VFO_Controller_1.0.6.exe
```

### SHA-256

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

[View v1.0.6 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.6?utm_source=chatgpt.com)

---

## v1.0.5

![v1.0.5](screenshot.png)

### v1.0.5

This was the earlier public release of the ICOM IC-M710 VFO Controller.

### v1.0.5 Executable

```text
ICOM_M710_VFO_Controller.exe
```

### SHA-256

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

[View v1.0.5 Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.5?utm_source=chatgpt.com)

---

# 🛠️ Troubleshooting

## Radio Does Not Connect

Check:

1. The correct COM port is selected.
2. The USB interface is connected.
3. The selected baud rate matches the radio.
4. The Radio ID is correct.
5. The Controller ID is correct.
6. The radio is configured for the appropriate remote-control interface.
7. The CI-V wiring is correct.
8. Another application is not already using the COM port.

---

## No Frequency Readback

Check:

* COM port
* Baud rate
* Radio ID
* Controller ID
* CI-V wiring
* Radio remote-control settings

Use **COM Monitor** to determine whether commands and responses are being exchanged.

---

## Wrong Radio ID

Check the IC-M710 setup menu:

```text
REMT -- ID
```

For example:

```text
REMT -- ID 01
```

Set the controller's Radio ID to the same value.

---

## COM Port Is Missing

Open **Windows Device Manager** and check:

```text
Ports (COM & LPT)
```

Reconnect the USB interface and check whether a COM port appears.

If using a CP2102-based interface, install the appropriate USB-to-UART driver if Windows does not automatically provide one.

---

## Radio Responds Incorrectly

Immediately stop communication and check:

* Wiring
* Pinout
* Signal levels
* Baud rate
* Radio ID
* Controller ID
* Remote-interface configuration

Do not continue operating a DIY interface until the electrical connections have been verified.

---

# 🔄 Communication Flow

The basic communication sequence is:

```text
Windows PC
    │
    │ USB
    ▼
USB / Serial Interface
    │
    │ Serial / CI-V
    ▼
ICOM IC-M710
    │
    │ CI-V Response
    ▼
USB / Serial Interface
    │
    ▼
Windows PC
    │
    ▼
ICOM IC-M710 VFO Controller
```

The application sends control commands and processes responses from the radio.

---

# 📁 Repository Structure

The public repository is organized approximately as follows:

```text
icom-icm710-vfo/
│
├── README.md
├── screenshot.png
├── screenshot-v1.0.6.png
├── screenshot-v1.0.7.png
│
└── docs/
    └── USER_GUIDE.md
```

The compiled application is distributed through the GitHub Releases page.

---

# 🔐 SHA-256 Verification

SHA-256 hashes are provided for published executables so that users can verify the downloaded file.

Example PowerShell command:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.7.exe -Algorithm SHA256
```

Compare the result with the SHA-256 value published for the corresponding release.

---

# 📥 Downloads

The latest executable is available from the GitHub Releases page.

[Download the Latest Release](https://github.com/4s6ggs/icom-icm710-vfo/releases/latest?utm_source=chatgpt.com)

All published releases:

[View All Releases](https://github.com/4s6ggs/icom-icm710-vfo/releases?utm_source=chatgpt.com)

---

# 💻 Source Code

The public release provides the compiled Windows executable.

**Python source code is not included in the public GitHub release.**

The repository is intended to provide the controller application, documentation, release information, and supporting project material.

---

# ⚠️ Safety and Regulatory Information

This software is intended to control an ICOM IC-M710 through a compatible serial/CI-V interface.

Users are responsible for:

* Correct electrical connections
* Correct radio configuration
* Compliance with applicable radio regulations
* Compliance with local amateur-radio licensing requirements
* Observing applicable band plans and operating restrictions

Do not transmit on frequencies or services for which you are not authorized.

When experimenting with DIY interfaces, verify the circuit and connector pinout before connecting equipment.

Incorrect wiring or voltage levels may damage the radio, computer, USB interface, or other equipment.

---

# ❓ FAQ

### Does this program require Python?

No.

The released Windows EXE does not require Python to be installed.

### Does this program work without an IC-M710?

The application is designed specifically for the ICOM IC-M710. Radio communication features require a compatible IC-M710 and serial interface.

### What is the default Radio ID?

The default configuration is:

```text
01
```

Always confirm the actual Radio ID configured in your radio.

### What is the Controller ID?

The controller uses:

```text
90
```

as its default Controller ID.

### What baud rates are supported?

```text
1200
2400
4800
9600
19200
```

### Can I use a DIY USB interface?

Yes, provided the interface is electrically compatible with the IC-M710 and the correct connector/interface circuitry is used.

See the [**User Guide**](docs/USER_GUIDE.md) for DIY interface information.

### Is the CP2102 directly compatible with the IC-M710?

Do not assume that it is.

A CP2102 is a USB-to-UART bridge. The required IC-M710 interface circuitry, connector wiring, signal levels, and configuration must be verified before connection.

---

# 📜 License

Please refer to the repository for the applicable project licensing information.

---

# 👤 Project Information

**Project:** ICOM IC-M710 VFO Controller
**Developer:** 4S6GGS
**Current Version:** 1.0.7
**Platform:** Windows
**Radio:** ICOM IC-M710

[GitHub Repository — 4s6ggs/icom-icm710-vfo](https://github.com/4s6ggs/icom-icm710-vfo?utm_source=chatgpt.com)

---

# ⚠️ Disclaimer

This software is provided for use with the ICOM IC-M710 and compatible interfaces.

The software developer is not responsible for damage resulting from:

* Incorrect wiring
* Incorrect interface construction
* Incorrect configuration
* Improper use
* Operation outside applicable regulations

Users are responsible for verifying their hardware connections and operating the radio safely and legally.

---

**ICOM IC-M710 VFO Controller — 4S6GGS**

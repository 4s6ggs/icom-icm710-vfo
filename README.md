# icom-icm710-vfo
ICOM-IC-M710-VFO-Controller
# ICOM IC-M710 VFO Controller

**Python / Tkinter / Serial CI-V Controller for ICOM IC-M710**

A desktop VFO controller for the **ICOM IC-M710** HF marine transceiver, providing computer-based frequency control, operating-mode selection, VFO tuning, radio status monitoring, volume control, mute control, and serial communication through the radio's CI-V interface.

**Developer:** 4S6GGS
**Application:** ICOM IC-M710 VFO Controller
**Version:** 1.0.5
**Repository:** https://github.com/4s6ggs/icom-icm710-vfo

---

## Features

### VFO Frequency Control

* Full VFO coverage from **1.6000 MHz to 30.0000 MHz**
* Direct frequency entry
* Frequency SET control
* Fast mouse-wheel tuning
* Selectable tuning steps:

  * 100 Hz
  * 1 kHz
  * 10 kHz
  * 100 kHz
  * 1 MHz
* Manual tuning mode
* Automatic acceleration mode
* Configurable automatic acceleration start and maximum step
* Wheel-speed reset

### Amateur Radio Band Selection

Quick-access buttons for:

| Band  | Frequency Range     |
| ----- | ------------------- |
| 160 m | 1.800 – 2.000 MHz   |
| 80 m  | 3.500 – 4.000 MHz   |
| 60 m  | 5.250 – 5.450 MHz   |
| 40 m  | 7.000 – 7.300 MHz   |
| 30 m  | 10.100 – 10.150 MHz |
| 20 m  | 14.000 – 14.350 MHz |
| 17 m  | 18.068 – 18.168 MHz |
| 15 m  | 21.000 – 21.450 MHz |
| 12 m  | 24.890 – 24.990 MHz |
| 10 m  | 28.000 – 29.700 MHz |

A **FULL VFO** mode is also available for the complete 1.600–30.000 MHz range.

---

## Operating Modes

The controller provides mode selection for:

* USB
* LSB
* AM
* AFS
* CW
* FSK

The selected mode is displayed in the main controller interface.

---

## Radio Control

The controller provides:

* RX / TX control
* Speaker mute control
* Speaker enable / disable
* Volume control
* Remote control
* Radio synchronization
* Frequency readback
* Radio status monitoring

---

## Serial Communication

Default communication settings:

| Setting       | Default |
| ------------- | ------- |
| COM Port      | COM1    |
| Baud Rate     | 4800    |
| Controller ID | 90      |
| Radio ID      | 01      |

Supported baud rates:

* 1200
* 2400
* 4800
* 9600
* 19200

The COM port can be selected directly from the application.

---

## Requirements

### Operating System

The application is primarily designed for:

* Windows 10
* Windows 11

### Python

Python 3.x is required when running the source code directly.

### Python Packages

Install the required package with:

```bash
python -m pip install pyserial
```

Tkinter is normally included with the standard Windows Python installation.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/4s6ggs/icom-icm710-vfo.git
```

Enter the project directory:

```bash
cd icom-icm710-vfo
```

Install the dependency:

```bash
python -m pip install pyserial
```

Run the controller:

```bash
python ICOM_M710_VFO_Controller.py
```

Replace the filename above if your Python source file has a different name.

---

## Serial Connection

Connect the computer to the ICOM IC-M710 using the appropriate serial interface.

Before connecting:

1. Connect the radio interface to the computer.
2. Power on the IC-M710.
3. Select the correct COM port.
4. Select the radio's baud rate.
5. Confirm the Radio ID.
6. Press **CONNECT**.

The controller will then communicate with the radio through the serial interface.

> **Important:** The actual hardware interface and CI-V wiring must be appropriate for the IC-M710 and your particular installation. Verify the radio manual and interface hardware before connecting equipment.

---

## User Interface

The application provides a single control interface containing:

* Radio identification
* COM port selection
* Baud-rate selection
* Radio ID
* Connection status
* Full VFO control
* Amateur-band selection
* Operating-mode selection
* Frequency display
* Frequency SET control
* Mouse-wheel tuning
* Automatic tuning acceleration
* RX/TX control
* MUTE control
* Volume control
* Communication log
* Radio status information
* About / Contact information

---

## Mouse Wheel Tuning

The mouse wheel can be used for rapid VFO adjustment.

Available steps:

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

The controller also supports automatic acceleration.

When **AUTO ACCELERATION** is enabled, continued wheel movement can increase the tuning step up to the configured maximum.

Press **ESC** to stop active wheel tuning.

---

## Application Information

**Application:** ICOM IC-M710 VFO Controller

**Callsign:** 4S6GGS

**Version:** 1.0.5

**Developer:** 4S6GGS

### Contact

Email:

```text
4S5GS.gayan@gmail.com
```

### YouTube

YouTube channel:

https://www.youtube.com/@4S6GGS

---

## Project Structure

A typical project structure is:

```text
icom-icm710-vfo/
│
├── ICOM_M710_VFO_Controller.py
├── README.md
├── requirements.txt
└── LICENSE
```

Additional files may be included for releases, documentation, icons, or executable builds.

---

## Building a Windows EXE

The application can be packaged as a Windows executable using PyInstaller.

Install PyInstaller:

```bash
python -m pip install pyinstaller
```

Example build command:

```bash
pyinstaller --onefile --windowed ICOM_M710_VFO_Controller.py
```

The executable will normally be created inside:

```text
dist\
```

For an application icon, use:

```bash
pyinstaller --onefile --windowed --icon=icon.ico ICOM_M710_VFO_Controller.py
```

---

## Version History

### Version 1.0.0

Initial release featuring:

* ICOM IC-M710 serial control
* Full VFO frequency control
* Amateur-band quick selection
* Operating-mode selection
* Mouse-wheel VFO tuning
* Automatic tuning acceleration
* RX/TX control
* Volume control
* Mute control
* Serial communication monitoring
* Radio synchronization
* About / Contact information

---

## Disclaimer

This is an independent software project for controlling an ICOM IC-M710 through a compatible computer/radio interface.

**ICOM** and **IC-M710** are trademarks of their respective owners. This project is not presented as an official ICOM product unless explicitly stated otherwise.

Always verify the correct radio configuration, interface hardware, serial settings, and operating limits before connecting the controller to a transceiver.

---

## License

If you have not selected a license yet, you can choose an appropriate open-source license for the project.

For example, the MIT License can be used if you want to permit modification and redistribution of the software subject to its terms.

---

## Project

**ICOM IC-M710 VFO Controller**

Developed by **4S6GGS**

GitHub:

https://github.com/4s6ggs/icom-icm710-vfo

YouTube:

https://www.youtube.com/@4S6GGS

Email:

[4S5GS.gayan@gmail.com](mailto:4S5GS.gayan@gmail.com)

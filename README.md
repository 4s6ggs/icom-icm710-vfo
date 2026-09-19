# ICOM IC-M710 VFO Controller

**Windows desktop controller for the ICOM IC-M710**

**Developer:** 4S6GGS
**Application:** ICOM IC-M710 VFO Controller
**Version:** 1.0.5

---

## 📻 Download

### Windows EXE

**[Download ICOM_M710_VFO_Controller.exe](./ICOM_M710_VFO_Controller.exe)**

No Python installation is required to run the Windows EXE.

---

## Features

* Full VFO control
* Frequency range: **1.6000 – 30.0000 MHz**
* Direct frequency entry
* Frequency SET control
* Mouse-wheel VFO tuning
* 100 Hz / 1 kHz / 10 kHz / 100 kHz / 1 MHz tuning steps
* Automatic tuning acceleration
* Amateur-band quick selection
* USB / LSB / AM / AFS / CW / FSK modes
* RX / TX status
* Volume control
* MUTE control
* Remote control
* Radio synchronization
* Frequency readback
* Radio status monitoring
* Serial communication log

---

## Amateur Radio Bands

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

---

## Serial Communication

Default settings:

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

---

## How to Use

1. Connect the IC-M710 to the computer using a compatible serial/CI-V interface.
2. Turn on the radio.
3. Run `ICOM_M710_VFO_Controller.exe`.
4. Select the correct COM port.
5. Select the appropriate baud rate.
6. Confirm the Radio ID.
7. Press **CONNECT**.
8. Use the VFO controls to control the radio.

---

## Mouse-Wheel Tuning

The mouse wheel provides fast VFO adjustment.

Available steps:

* 100 Hz
* 1 kHz
* 10 kHz
* 100 kHz
* 1 MHz

The controller also supports **AUTO ACCELERATION**.

Press **ESC** to stop active wheel tuning.

---

## System Requirements

* Windows 10
* Windows 11
* Compatible serial/CI-V radio interface

The distributed EXE does **not** require Python to be installed.

---

## Important

The actual serial/CI-V interface and wiring must be suitable for your IC-M710 and installation.

Verify the radio manual, interface hardware, serial settings, and operating configuration before connecting the controller to the radio.

---

## Developer

**4S6GGS**

ICOM IC-M710 VFO Controller

GitHub:
https://github.com/4s6ggs/icom-icm710-vfo

YouTube:
https://www.youtube.com/@4S6GGS

Email:
[4S5GS.gayan@gmail.com](mailto:4S5GS.gayan@gmail.com)

---

## Disclaimer

This is an independent software project for controlling an ICOM IC-M710 through a compatible computer/radio interface.

ICOM and IC-M710 are trademarks of their respective owners. This project is not an official ICOM product unless explicitly stated otherwise.

---

## License

See the `LICENSE` file included in this repository.

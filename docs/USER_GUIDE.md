# ICOM IC-M710 VFO Controller

## User Guide

**Version:** 1.0.7
**Developer:** 4S6GGS
**Radio:** ICOM IC-M710
**Platform:** Windows 10 / Windows 11

---

## 1. Overview

The **ICOM IC-M710 VFO Controller** is a Windows application for remote control of the ICOM IC-M710 through its CI-V serial interface.

The controller provides a graphical interface for:

* Frequency control
* Full VFO operation
* Amateur-band selection
* Operating-mode selection
* Frequency readback
* RX/TX status
* Remote status
* Volume control
* Speaker mute
* RIT control
* Real-time S-Meter
* Mouse-wheel tuning
* Manual tuning
* Automatic tuning acceleration
* COM-port configuration
* Serial communication monitoring

The application communicates with the IC-M710 using a compatible serial/CI-V interface.

> **Important:** This software is designed for use with compatible IC-M710 hardware and interfaces. Always verify your radio configuration and wiring before connecting external equipment.

---

# 2. Latest Release — v1.0.7

## Download

The latest release is:

**ICOM IC-M710 VFO Controller v1.0.7**

GitHub Releases:

https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

Executable:

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

No Python installation is required to run the compiled Windows executable.

---

## v1.0.7 Screenshot

![ICOM IC-M710 VFO Controller v1.0.7](../screenshot-v1.0.7.png)

---

## v1.0.7 Changes

Version 1.0.7 introduces improvements to the configuration and operating workflow.

### Separate COM Port Setup Page

Serial communication settings are now organized on a dedicated **COM Port Setup** page.

This makes it easier to configure:

* COM port
* Baud rate
* Controller ID
* Radio ID
* Serial connection

### COM Monitor

A **COM Monitor** has been added to the COM Port Setup page.

The monitor helps the operator observe communication between the controller and the radio.

This is useful when:

* Testing a new cable
* Checking the COM port
* Troubleshooting communication
* Confirming that commands are being transmitted
* Checking radio responses

### RIT Control

**RIT Control** has been added to the Main page.

The operator can adjust receive incremental tuning without leaving the main operating screen.

### Communication Improvements

The serial communication workflow has been improved for more reliable operation and easier troubleshooting.

### Radio Control Workflow

The interface has been reorganized to separate communication configuration from normal radio operation.

---

# 3. v1.0.6

## v1.0.6 Screenshot

![ICOM IC-M710 VFO Controller v1.0.6](../screenshot-v1.0.6.png)

---

## v1.0.6 Features

Version 1.0.6 introduced the **real-time S-Meter** and related monitoring functionality.

### Real-Time S-Meter

The controller displays the IC-M710 received signal level from:

```text
S0
```

through:

```text
S8
```

The signal level is updated while the controller is connected and the radio is receiving.

The controller polls the radio approximately every **300 ms**.

The S-Meter communication uses the IC-M710 `SIGM` command and processes the corresponding `ALY` response.

The polling process:

* Runs while connected.
* Runs during RX.
* Stops during TX.
* Resets to S0 when disconnected.

The signal-level range used by the application is:

```text
0 – 8
```

The corresponding CI-V command format used by the controller is:

```text
PICOA,90,<RADIO_ID>,SIGM,
```

---

# 4. v1.0.5

## v1.0.5 Screenshot

![ICOM IC-M710 VFO Controller v1.0.5](../screenshot.png)

---

## v1.0.5 Features

The v1.0.5 release provides the original core VFO-control functionality, including:

* Frequency control
* Full VFO range
* Amateur-band quick selection
* Operating-mode selection
* Mouse-wheel tuning
* Manual tuning
* Automatic acceleration
* Frequency readback
* RX/TX indication
* Remote status
* Volume control
* Speaker mute
* CI-V serial communication

---

# 5. System Requirements

## Computer

* Windows 10 or Windows 11
* Available USB port or serial COM port
* Compatible serial/CI-V interface
* Sufficient permissions to access the selected COM port

## Radio

* ICOM IC-M710
* Correctly configured remote-control interface
* Compatible CI-V communication connection

## Software

The compiled EXE does not require Python.

```text
Python installation: Not required
```

---

# 6. Before You Begin

Before starting the application, make sure:

1. The IC-M710 is powered on.
2. The radio-side interface is correctly connected.
3. The USB/serial interface is connected to the computer.
4. Windows detects the interface.
5. The correct COM port is known.
6. The radio's remote ID is known.
7. The baud rate is known or set to the required value.
8. The radio's remote interface configuration is correct.

If you are building your own interface, read the DIY cable section before connecting anything to the radio.

---

# 7. Connecting the IC-M710

The controller requires a suitable serial interface between the Windows PC and the IC-M710.

A typical arrangement is:

```text
Windows PC
    │
    │ USB
    ▼
USB / Serial Interface
    │
    │ Serial / CI-V
    ▼
IC-M710 Remote Interface
    │
    ▼
ICOM IC-M710
```

The exact electrical interface depends on the hardware being used.

> **Do not connect a generic USB-to-UART module directly to an IC-M710 connector unless the electrical interface and pinout have been verified.**

---

# 8. DIY USB Clone / Remote-Control Cable

A low-cost interface can be built using a **CP2102 USB-to-UART module** together with suitable radio-side interface circuitry.

A useful general reference is:

**DIY Universal Radio Clone Cable Using CP2102 USB Interface**

https://www.instructables.com/DIY-Universal-Radio-Clone-Cable-Using-CP2102-USB-I

This project demonstrates a CP2102-based universal radio cable using TX/RX isolation and a common radio-side connection.

> **Important:** The Instructables project is a general-purpose radio clone-cable reference. It is **not an IC-M710 wiring diagram**. The IC-M710 connector, pinout, electrical interface, and remote-interface configuration must be verified separately.

---


# 9. IC-M710 Remote Interface

The IC-M710 provides remote-control functionality through its designated interface.

Depending on the configuration, the relevant interface may be associated with the radio's **REMOTE/DSC** connection.

Before constructing the cable:

1. Identify the correct IC-M710 connector.
2. Verify the connector pinout.
3. Verify the signal names.
4. Verify the electrical interface.
5. Verify the `REMT-IF` setting.
6. Verify the `REMT-ID`.

Do not rely on an unverified Internet pinout.

---

# 10. IC-M710 `REMT-IF` Setting

The IC-M710 has a Set Mode item named:

```text
REMT-IF
```

This controls the remote-control interface selection.

To enter Set Mode:

1. Turn the IC-M710 **OFF**.
2. Press and hold:

```text
FUNC + 1
```

3. While holding the buttons, turn the radio **ON**.
4. The radio enters Set Mode.
5. Use the **GROUP selector** to navigate through the settings.
6. Locate:

```text
REMT-IF
```

The available selection depends on the radio configuration and interface being used.

For example, an IC-M710 configuration may show an interface selection associated with the D-sub/REMOTE connection.

> Select the option that corresponds to the physical interface actually being used. Do not select an option only because its name appears similar to your cable.

---

# 11. How to Find the IC-M710 Radio ID

The **Radio ID** is required by the VFO Controller.

To find it:

### Step 1

Turn the IC-M710 **OFF**.

### Step 2

Press and hold:

```text
FUNC + 1
```

### Step 3

Turn the radio **ON** while continuing to hold the buttons.

### Step 4

The radio enters Set Mode.

### Step 5

Use the **left GROUP selector/knob** to move through the setup items.

### Step 6

Find:

```text
REMT-ID
```

You may see:

```text
REMT -- ID 01
```

The number is the radio's remote ID.

For example:

```text
REMT-ID = 01
```

Enter the same value in the controller:

```text
Radio ID: 01
```

The normal ID range is:

```text
01 – 99
```

The default value is normally:

```text
01
```

---

# 12. `REMT-ID` vs `REMT-IF`

These two settings are different.

### `REMT-ID`

Identifies the radio.

Example:

```text
REMT-ID = 01
```

Enter this value as:

```text
Radio ID = 01
```

### `REMT-IF`

Selects the remote-control interface.

It is **not** the Radio ID.

For example, when navigating Set Mode you may see:

```text
REMT-ID
```

and:

```text
REMT-IF
```

Use `REMT-ID` to determine the radio address.

Use `REMT-IF` to select the appropriate physical remote-control interface.

---

# 13. Windows COM Port

After connecting the USB interface:

1. Open **Device Manager**.
2. Expand:

```text
Ports (COM & LPT)
```

3. Locate the USB/serial interface.

For example:

```text
CP210x USB to UART Bridge (COM4)
```

In this example:

```text
COM4
```

is the COM port to select in the controller.

---

# 14. CP2102 USB Driver

Windows may automatically install a driver for the CP2102.

If Windows does not recognize the device, install the appropriate **Silicon Labs CP210x USB-to-UART driver** for your operating system.

After successful installation, the device should appear under:

```text
Device Manager
└── Ports (COM & LPT)
```

---

# 15. Building the DIY Cable

For a first build, construct and test the cable in stages.

## Stage 1 — Test the CP2102

Connect:

```text
PC
 │
 USB
 ▼
CP2102
```

Confirm that Windows detects it.

---

## Stage 2 — Identify the COM Port

Open Device Manager and record the COM number.

Example:

```text
CP210x USB to UART Bridge
COM4
```

---

## Stage 3 — Verify the CP2102 Signals

Identify:

```text
TXD
RXD
GND
```

on your actual CP2102 module.

Do not rely only on the physical position of the pins.

---

## Stage 4 — Build the Radio-Side Interface

Construct the interface circuitry according to the verified IC-M710 electrical requirements.

The generic structure is:

```text
CP2102
   │
   ▼
Interface Circuit
   │
   ▼
IC-M710 Connector
```

---

## Stage 5 — Check the Cable

Before connecting the cable to the radio, use a multimeter to check:

* Continuity
* Ground/reference connection
* TX/RX routing
* Connector pin assignment
* Accidental shorts

---

## Stage 6 — Configure the Radio

Verify:

```text
REMT-ID
REMT-IF
```

---

## Stage 7 — Connect to the Radio

Only after the cable has been checked should it be connected to the IC-M710.

---

# 20. DIY Cable Wiring Concept

The general signal path is:

```text
Computer
   │
   │ USB
   ▼
CP2102
   │
   ├── TX
   │
   ├── RX
   │
   └── GND
   │
   ▼
Radio Interface Circuit
   │
   ▼
IC-M710 Remote Interface
```

For conventional UART signal routing:

```text
CP2102 TX → Interface RX
CP2102 RX ← Interface TX
```

The exact radio-side wiring must be determined from the verified IC-M710 interface documentation.

---

# 21. Cable Enclosure

For a permanent cable, place the CP2102 and interface circuitry inside a small enclosure.

Example:

```text
┌─────────────────────────────────┐
│       USB RADIO INTERFACE        │
│                                 │
│ USB                              │
│  │                              │
│  ▼                              │
│ ┌───────────────┐               │
│ │    CP2102     │               │
│ └───────┬───────┘               │
│         │                       │
│ ┌───────▼────────┐              │
│ │ Radio Interface │             │
│ │    Circuit      │             │
│ └───────┬────────┘              │
│         │                       │
└─────────┼───────────────────────┘
          │
          ▼
      IC-M710
```

Use:

* Strain relief
* Insulated connections
* Heat-shrink tubing
* Secure solder joints
* Suitable shielding where appropriate

---

# 22. Cable Labeling

Clearly label the finished cable.

For example:

```text
ICOM IC-M710
USB REMOTE CONTROL
CP2102
```

You may also label the ends:

```text
PC / USB
```

and:

```text
IC-M710 REMOTE
```

---

# 23. First Test After Building the Cable

Do not begin by testing transmit functions.

First verify communication.

### 1. Turn on the IC-M710

Allow the radio to start normally.

### 2. Start the controller

Run:

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

### 3. Open COM Port Setup

Select the detected COM port.

### 4. Set the baud rate

Use:

```text
4800
```

unless your radio/interface configuration requires another supported value.

### 5. Enter the Radio ID

For example:

```text
Radio ID: 01
```

### 6. Enter the Controller ID

Default:

```text
Controller ID: 90
```

### 7. Check COM Monitor

Observe serial communication.

### 8. Connect

Press:

```text
CONNECT
```

### 9. Test frequency readback

Confirm that the controller can communicate with the radio.

### 10. Test additional functions

Test:

* Frequency
* Mode
* Volume
* RIT
* S-Meter
* Remote status

---

# 24. COM Port Setup

Version 1.0.7 provides a separate **COM Port Setup** page.

The page contains the communication configuration.

Typical settings are:

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

---

# 25. COM Monitor

The COM Monitor is available on the COM Port Setup page.

It is useful when troubleshooting communication.

Use it to check whether:

* Commands are being sent.
* The radio is responding.
* The selected COM port is active.
* The configured IDs are being used.
* Communication is occurring after CONNECT.

The COM Monitor is particularly useful when testing a DIY cable.

---

# 26. Main Page

The Main page provides the normal radio-control functions.

The main operating area includes:

* Frequency
* VFO range
* Amateur bands
* Operating mode
* Mouse-wheel control
* RIT
* RX/TX status
* Remote status
* Volume
* Speaker mute
* S-Meter

---

# 27. Frequency Display

The frequency is displayed in MHz.

Example:

```text
14.2000 MHz
```

The controller uses a four-decimal MHz display.

---

# 28. Entering a Frequency

To enter a frequency manually:

1. Click the frequency entry field.
2. Enter the desired frequency.
3. Press **SET**.

Example:

```text
14.2000
```

The controller sends the corresponding frequency command to the radio.

---

# 29. Full VFO

The controller provides a full VFO operating range:

```text
1.6000 MHz – 30.0000 MHz
```

The Full VFO button is shown as:

```text
FULL VFO
1.6 MHz → 30 MHz
```

When selected, the frequency can be controlled throughout the configured VFO range.

---

# 30. Amateur-Band Quick Selection

The controller provides quick access to the following amateur bands.

| Band  |             Range | Default Start |
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

Selecting a band changes the VFO range and moves the frequency to the configured starting frequency.

> **Note:** These are the controller's configured operating ranges. Always observe the regulations and band allocations applicable to your location and operating service.

---

# 31. Operating Modes

The controller provides:

```text
USB
LSB
AM
AFS
CW
FSK
```

Select the required mode from the Main page.

The selected mode is sent to the IC-M710.

---

# 32. Mouse-Wheel Tuning

The mouse wheel can be used to tune the VFO.

Available manual tuning steps are:

|     Step | Display |
| -------: | ------- |
|  0.1 kHz | 100 Hz  |
|    1 kHz | 1 kHz   |
|   10 kHz | 10 kHz  |
|  100 kHz | 100 kHz |
| 1000 kHz | 1 MHz   |

The default step is:

```text
100 Hz
```

---

# 33. Manual Tuning

In **MANUAL** mode, the selected wheel step remains fixed.

Example:

```text
100 Hz
```

Each wheel movement changes the frequency by the selected amount.

This is useful when precise frequency control is required.

---

# 34. Auto Acceleration

The controller also provides:

```text
AUTO ACCELERATION
```

Auto acceleration allows the tuning step to increase while the operator continues to rotate the mouse wheel.

The available acceleration range uses:

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

The operator can configure the maximum acceleration level.

---

# 35. Reset Wheel Speed

The **RESET** function returns the tuning speed to the configured starting level.

This is useful after using automatic acceleration.

---

# 36. ESC / Stop Wheel

Press:

```text
ESC
```

to stop active mouse-wheel tuning.

This provides a quick way to stop continued tuning activity.

---

# 37. RIT Control

Version 1.0.7 adds **RIT Control** to the Main page.

RIT means:

```text
Receive Incremental Tuning
```

RIT allows the receive frequency to be adjusted independently for fine receive correction.

Use RIT when a received station is slightly offset from the desired receive frequency.

The RIT controls are located on the Main page in v1.0.7.

---

# 38. RX / TX Status

The controller displays the current transceiver state:

```text
RX
```

or:

```text
TX
```

RX is displayed using the receive indication.

TX is displayed using the transmit indication.

The S-Meter polling process is stopped while the radio is transmitting.

---

# 39. Remote Status

The controller displays the remote-control state.

Example:

```text
REMOTE OFF
```

The status helps indicate the current remote-control condition.

---

# 40. Volume Control

The controller provides a volume control for the IC-M710.

Use the volume control to adjust the radio audio level remotely.

---

# 41. Speaker Mute

The controller provides a speaker mute function.

Mute can be used when the operator wants to temporarily silence the radio speaker while maintaining the control connection.

---

# 42. S-Meter

The S-Meter was introduced in **v1.0.6**.

It displays:

```text
S0 – S8
```

The controller requests the signal level approximately every:

```text
300 ms
```

while:

* The controller is connected.
* The radio is receiving.

S-Meter polling stops during TX.

When disconnected, the displayed signal level resets to:

```text
S0
```

---

# 43. Typical Startup Procedure

For normal operation:

### Step 1

Connect the IC-M710 interface to the computer.

### Step 2

Turn on the IC-M710.

### Step 3

Start:

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

### Step 4

Open:

```text
COM Port Setup
```

### Step 5

Press:

```text
REFRESH
```

### Step 6

Select the correct COM port.

### Step 7

Set the baud rate.

Default:

```text
4800
```

### Step 8

Enter the Radio ID.

Default:

```text
01
```

### Step 9

Confirm the Controller ID.

Default:

```text
90
```

### Step 10

Check the COM Monitor.

### Step 11

Press:

```text
CONNECT
```

### Step 12

Return to the Main page.

### Step 13

Confirm:

* Frequency
* Mode
* RX/TX
* Remote status
* S-Meter

### Step 14

Test frequency control.

---

# 44. Default Settings

The controller starts with the following default values.

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
| S-Meter       | S0                 |

---

# 45. Troubleshooting

## Controller does not start

Check:

* Windows version.
* EXE file integrity.
* Windows security warnings.
* File permissions.
* Whether the EXE was downloaded completely.

---

## COM port is not shown

Check:

1. USB cable.
2. USB interface.
3. Windows Device Manager.
4. CP210x driver.
5. Whether another application is using the COM port.

Press **REFRESH** after connecting the interface.

---

## CONNECT does not work

Check:

```text
COM Port
Baud Rate
Controller ID
Radio ID
REMT-ID
REMT-IF
Cable
```

---

## COM Monitor shows no activity

Check:

* Correct COM port.
* Correct USB interface.
* Cable connection.
* Whether another application has opened the COM port.
* Controller connection status.

---

## COM Monitor shows transmitted data but no response

The PC-side connection may be functioning while the radio-side connection is not.

Check:

* IC-M710 connector.
* Radio-side interface.
* TX/RX routing.
* Ground/reference.
* `REMT-IF`.
* `REMT-ID`.
* Baud rate.
* Radio power.

---

## Frequency does not change

Check:

* Radio connection.
* COM port.
* Radio ID.
* Controller ID.
* VFO range.
* Frequency value.
* COM Monitor activity.

---

## Frequency readback does not work

Check whether the radio is responding to the controller.

If commands appear in COM Monitor but no response is received, inspect the radio-side interface.

---

## S-Meter remains at S0

Check:

* Controller connection.
* Radio receive state.
* Serial communication.
* COM Monitor.
* Radio response.

Remember that S-Meter polling stops during TX.

---

## RIT does not respond

Check:

* Controller connection.
* Radio communication.
* COM Monitor.
* Current radio operating state.

---

# 46. DIY Cable Troubleshooting

## CP2102 is not detected

Possible causes:

* Faulty USB cable.
* Missing driver.
* Faulty CP2102 module.
* USB port problem.
* Incorrect module wiring.

---

## CP2102 is detected but radio does not respond

Check:

```text
COM Port
Baud Rate
Radio ID
Controller ID
REMT-IF
REMT-ID
TX/RX routing
Ground/reference
Radio connector
Radio-side interface
```

---

## Radio behaves unexpectedly

Disconnect the interface and stop testing.

Recheck:

* Connector pinout.
* Electrical interface.
* Power connections.
* TX/RX connections.
* Ground/reference.
* Interface circuitry.

Do not continue using an interface with uncertain wiring.

---

# 47. DIY Cable First-Test Checklist

Before connecting a newly built cable:

```text
☐ CP2102 detected by Windows
☐ USB driver installed
☐ COM port identified
☐ TXD identified
☐ RXD identified
☐ GND identified
☐ Radio connector verified
☐ IC-M710 pinout verified
☐ Radio-side interface verified
☐ Cable continuity checked
☐ No accidental shorts
☐ Ground/reference checked
☐ REMT-IF checked
☐ REMT-ID checked
☐ Radio ID entered
☐ Baud rate configured
☐ Controller ID configured
☐ COM Monitor ready
```

---

# 48. Communication Flow

The controller communicates with the IC-M710 through the serial interface.

A simplified communication path is:

```text
VFO Controller
      │
      ▼
Windows COM Port
      │
      ▼
USB / Serial Interface
      │
      ▼
Radio-Side Interface
      │
      ▼
IC-M710
      │
      ▼
Radio Response
      │
      ▼
VFO Controller
```

The COM Monitor can be used to observe this communication during troubleshooting.

---

# 49. Release History

## v1.0.7

* Added separate COM Port Setup page.
* Added COM Monitor to COM Port Setup.
* Added RIT Control to Main page.
* Improved COM-port configuration.
* Improved communication monitoring.
* Improved radio-control workflow.

## v1.0.6

* Added real-time S-Meter.
* Added periodic signal-level polling.
* Added RX/TX-aware S-Meter polling.
* Added S0 reset on disconnect.

## v1.0.5

* Core VFO control.
* Full VFO operation.
* Amateur-band quick selection.
* Operating-mode control.
* Mouse-wheel tuning.
* Auto acceleration.
* Frequency readback.
* RX/TX indication.
* Remote status.
* Volume.
* Speaker mute.
* CI-V serial communication.

---

# 50. Downloads

Official GitHub releases:

Latest:

https://github.com/4s6ggs/icom-icm710-vfo/releases/latest

v1.0.7:

https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.7

v1.0.6:

https://github.com/4s6ggs/icom-icm710-vfo/releases/tag/v1.0.6

All releases:

https://github.com/4s6ggs/icom-icm710-vfo/releases

---

# 51. SHA-256 Verification

SHA-256 checksums are provided to allow verification of downloaded executable files.

## v1.0.7

File:

```text
ICOM_M710_VFO_Controller_1.0.7.exe
```

SHA-256:

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

### PowerShell

Open PowerShell in the directory containing the EXE and run:

```powershell
Get-FileHash .\ICOM_M710_VFO_Controller_1.0.7.exe -Algorithm SHA256
```

Compare the result with:

```text
85e167451da74dc6a0ab8c68471e32b842706fe0b8516f771bec5275ed98b8b1
```

---

## v1.0.6

SHA-256:

```text
2956fceac0918cfa544eafabefab704a66dc9cc44892e3ac388f59fa62ac584d
```

---

## v1.0.5

SHA-256:

```text
60d02d21b5468971dfd9acc787fdb89184801a780a25e24daa7bb770353b08d7
```

---

# 52. Source Code

The public release is distributed as a compiled Windows executable.

The Python source code is **not included in the public GitHub release**.

The GitHub repository contains the project documentation and release information.

Repository:

https://github.com/4s6ggs/icom-icm710-vfo

---

# 53. Operating the Radio Responsibly

The controller is a remote-control tool.

The operator remains responsible for:

* Correct radio configuration.
* Correct frequency selection.
* Correct operating mode.
* Legal operation.
* Transmit authorization.
* Compliance with applicable amateur-radio regulations.
* Compliance with any applicable maritime, commercial, or other radio-service requirements.

Always verify the regulations applicable to your location and operating service before transmitting.

---

# 54. Hardware Safety

Before connecting a DIY interface:

* Verify the connector pinout.
* Verify the electrical interface.
* Check for shorts.
* Check TX/RX routing.
* Check the signal reference.
* Confirm the `REMT-IF` setting.
* Confirm the `REMT-ID`.
* Use appropriate isolation/interface circuitry where required.

Never assume that a CP2102 UART output can be connected directly to an unknown radio connector.

---

# 55. FAQ

## Do I need Python?

No.

The compiled Windows EXE does not require Python.

---

## Can I use a CP2102?

A CP2102 can be used as the USB-to-UART portion of a suitable interface.

The required radio-side electrical interface must be implemented correctly.

---

## Can I connect the CP2102 directly to the IC-M710?

Do not assume that it can.

Verify the IC-M710 interface requirements and use the appropriate interface circuitry.

---

## Where can I find the Radio ID?

Enter IC-M710 Set Mode by:

```text
Radio OFF
   ↓
Hold FUNC + 1
   ↓
Power ON
   ↓
Set Mode
   ↓
GROUP selector
   ↓
REMT-ID
```

For example:

```text
REMT-ID 01
```

Then enter:

```text
Radio ID = 01
```

in the controller.

---

## What is the difference between Radio ID and Controller ID?

**Radio ID** identifies the IC-M710.

**Controller ID** identifies the controller address used by the communication system.

They are separate settings.

Default values:

```text
Radio ID       = 01
Controller ID  = 90
```

---

## What baud rates are supported?

The controller provides:

```text
1200
2400
4800
9600
19200
```

The default is:

```text
4800
```

---

## What frequency range does the controller support?

The configured Full VFO range is:

```text
1.6000 MHz – 30.0000 MHz
```

---

## What tuning steps are available?

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

---

## Does the controller have an S-Meter?

Yes.

The real-time S-Meter was introduced in **v1.0.6**.

---

## Does v1.0.7 have RIT?

Yes.

RIT Control was added to the Main page in **v1.0.7**.

---

## Does v1.0.7 have a COM Monitor?

Yes.

The COM Monitor is available on the **COM Port Setup** page.

---

# 56. Project Information

**Project:** ICOM IC-M710 VFO Controller

**Developer:** 4S6GGS

**Current Version:** 1.0.7

**GitHub:**

https://github.com/4s6ggs/icom-icm710-vfo

---

# 57. Disclaimer

This software is provided as a radio-control application for the ICOM IC-M710.

The developer is not responsible for:

* Incorrect hardware wiring.
* Damage caused by incorrect interface construction.
* Incorrect radio configuration.
* Incorrect frequency selection.
* Unauthorized transmissions.
* Regulatory violations.
* Damage resulting from use of unsuitable hardware.
* Damage resulting from incorrect electrical connections.

Users building their own interface should verify all electrical connections before connecting the interface to the radio.

The CP2102 cable reference linked in this guide is provided for educational and construction-reference purposes. The circuit should not be assumed to be electrically compatible with the IC-M710 without independent verification.

---

# 58. Final Quick Reference

## Radio

```text
Radio                  ICOM IC-M710
Remote ID              01
```

## Controller

```text
Controller ID          90
```

## Serial

```text
Default COM            COM1
Default Baud           4800
Supported Baud         1200 / 2400 / 4800 / 9600 / 19200
```

## VFO

```text
Default Frequency      14.2000 MHz
Full VFO               1.6000–30.0000 MHz
Default Mode           USB
```

## Tuning

```text
100 Hz
1 kHz
10 kHz
100 kHz
1 MHz
```

## S-Meter

```text
S0 – S8
~300 ms polling
RX only
```

## v1.0.7

```text
COM Port Setup
COM Monitor
RIT Control
Communication improvements
```

---

## 59. Recommended First-Time Setup

For a new user, the simplest sequence is:

```text
1. Install/connect the USB interface
        ↓
2. Confirm Windows COM port
        ↓
3. Configure IC-M710 REMT-IF
        ↓
4. Find IC-M710 REMT-ID
        ↓
5. Start VFO Controller
        ↓
6. Open COM Port Setup
        ↓
7. Select COM port
        ↓
8. Select 4800 baud
        ↓
9. Enter Radio ID
        ↓
10. Confirm Controller ID 90
        ↓
11. Check COM Monitor
        ↓
12. CONNECT
        ↓
13. Verify frequency readback
        ↓
14. Test frequency control
        ↓
15. Test mode / volume / RIT
        ↓
16. Check S-Meter
```

Once communication has been confirmed, the controller is ready for normal VFO operation.

---

**ICOM IC-M710 VFO Controller — 4S6GGS**

**Version 1.0.7**

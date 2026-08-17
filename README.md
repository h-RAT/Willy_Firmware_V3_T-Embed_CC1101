<h1 align="center"> <code>Willy Firmware V3</code> - Flipper Zero alternative for LILYGO T-Embed CC1101</h1><a id="introduction"></a>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_CC1101/main/Image/Logo.png">
</p>

<h2 align="center">
  <a href="#introduction">Introduction</a> | <a href="#features">Features</a> | <a href="#fromwilly">V2 → V3</a> | <a href="#contact">Contact</a> | <a href="#disclaimer">Disclaimer</a>
</h2>

**Willy Firmware V3** is a feature-rich firmware developed specifically for the **LILYGO T-Embed CC1101** and **T-Embed CC1101 Plus**.

Inspired by the Flipper Zero ecosystem, Willy Firmware brings **Sub-GHz, Infrared, NFC, Wi-Fi, Bluetooth/BLE and nRF24** functionality together in a single ESP32-S3 device.

V3 has been redesigned around the T-Embed platform with a focus on **stability, usability, hardware integration and standalone operation**.

<p align="center">
  <a href="https://discord.gg/VqsUsPQSmP"><img src="https://discordapp.com/api/guilds/1169681522715000873/widget.png?style=banner2" alt="Discord Banner 3"/></a>
</p>

<h4 align="center">Website: https://willy-firmware.com/</h4>

-----

<h1 align="center">What makes Willy Firmware special?</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/IMG_20260814_215202.jpg" width="50%" alt="Willy">
</p>

<br>

Willy Firmware V3 was rebuilt specifically for the LILYGO T-Embed CC1101 platform, taking advantage of its integrated hardware while keeping the philosophy of the previous Willy Firmware generations.

- **All-in-one:** Sub-GHz, Infrared, NFC, Wi-Fi, Bluetooth/BLE and nRF24 functionality.
- **T-Embed optimized:** Designed specifically around the ESP32-S3 based T-Embed CC1101.
- **T-Embed CC1101 Plus support:** Supports the additional nRF24 2.4 GHz radio available on the Plus model.
- **Flipper Zero file compatibility:** Uses Flipper Zero-compatible Sub-GHz and Infrared file formats, allowing compatible files to be saved, loaded, exchanged and reused between devices.
- **SD Card support:** Captured signals and compatible files can be stored and accessed directly from the device.
- **Actively developed:** New applications, protocols, improvements and fixes are regularly added.

---

# Supported Hardware<a id="supported-hardware"></a>

| Device | Support | CC1101 | nRF24 |
| --- | :---: | :---: | :---: |
| LILYGO T-Embed CC1101 | ✅ | ✅ | — |
| LILYGO T-Embed CC1101 Plus | ✅ | ✅ | ✅ |

Both versions use the integrated CC1101 for Sub-GHz functionality.

The **T-Embed CC1101 Plus** additionally includes an nRF24 2.4 GHz radio, which is supported by Willy Firmware V3.

Willy Firmware V3 is designed specifically for the LILYGO T-Embed CC1101 and T-Embed CC1101 Plus. It is not intended as a direct replacement firmware for other ESP32 boards.

---

<p align="center">
   <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Home.png" width="500" alt="Willy">
</p>

-----

<h1 align="center">Features</h1><a id="features"></a>

<h3 align="center">
  <a href="#subghz">📡 Sub-GHz</a> |
  <a href="#infrared">💡 Infrared</a> |
  <a href="#bluetooth">🟦 Bluetooth / BLE</a> |
  <a href="#wifi">📶 Wi-Fi</a> |
  <a href="#nfc">📱 NFC</a> |
  <a href="#nrf24">📡 nRF24</a> |
  <a href="#settings">⚙️ Settings</a>
</h3>

<br>

### 📡 Sub-GHz<a id="subghz"></a>

<p align="center">
  <a href="#read-raw">Read RAW</a> •
  <a href="#read">Read</a> •
  <a href="#transmit">Transmit</a> •
  <a href="#tesla">Tesla</a> •
  <a href="#scanner">Scanner</a> •
  <a href="#bruteforce">Bruteforce</a> •
  <a href="#debruijn">DeBruijn</a> •
  <a href="#jukebox">Jukebox</a> •
  <a href="#jammer">Jammer</a> •
  <a href="#rolljam">Rolljam</a> •
  <a href="#rollback">Rollback</a> •
  <a href="#jam_mode">Rolljam/back Jammer</a> •
  <a href="#pocsag_read">Pocsag Read</a> •
  <a href="#pocsag_send">Pocsag Send</a>
</p>

Willy Firmware uses the integrated **CC1101** for Sub-GHz reception, decoding, transmission and signal analysis.

The firmware supports both known protocols and RAW signals, allowing signals to be received, analyzed, saved and reused directly from the device.

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz1.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz2.png" width="49%">
</p>

-----

- Read RAW:<a id="read-raw"></a><br>

**Read RAW** captures Sub-GHz signals directly as RAW pulse data.

This allows signals using unknown or unsupported protocols to be captured without requiring a decoder.

Captured signals can be inspected, retransmitted or saved to the SD card for later use.

### RAW capture

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW_Settings.png" width="49%">
</p>

### Captured RAW signal

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW_Signal.png" width="700">
</p>

-----

- Read:<a id="read"></a><br>

**Read** receives and decodes Sub-GHz signals using known protocols.

When a compatible signal is received, Willy Firmware decodes its information and stores it temporarily in memory.

Up to **50 signals** can be kept in memory. From there, signals can be inspected, retransmitted or saved to the SD card for later use.

### Read interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Settings.png" width="49%">
</p>

### Received signal

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal2.png" width="49%">
</p>

### Signal list

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_List.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_List2.png" width="49%">
</p>

### Signal generator

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_Generator.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_Generator2.png" width="49%">
</p>

### Supported decoders

<details>
<summary><b>Show supported Sub-GHz decoders</b></summary>

<br>

- Allstar Firefly
- Alutech AT-4N
- Ansonic
- BETT
- Beninca ARC
- CAME
- CAME Atomo
- CAME TWEE
- Cham_Code
- Clemsa
- Ditec GOL4
- Doitrand
- Dooya
- Elplast
- Faac SLH
- Feron
- GangQi
- GateTX
- Hay21
- Hollarm
- Holtek
- Holtek_HT12X
- Honeywell
- Honeywell Sec
- Hormann HSM
- Intertechno_V3
- Jarolift
- KeeLoq
- KeyFinder
- KingGates Stylo4k
- Legrand
- Linear
- LinearDelta3
- Magellan
- Marantec
- Marantec24
- Mastercode
- MegaCode
- Nero Radio
- Nero Sketch
- Nice FLO
- Nice FloR-S
- Nord ICE
- Phoenix_V2
- Power Smart
- Princeton
- Revers_RB2
- Roger
- SMC5326
- Security+ 1.0
- Security+ 2.0
- Somfy Keytis
- Somfy Telis
- Star Line
- Treadmill37

</details>

### Supported vehicle decoders

<details>
<summary><b>Show supported vehicle decoders</b></summary>

<br>

- Chrysler
- Fiat SPA
- Ford V0
- Ford V1
- Ford V2
- Kia/HYU V0
- Kia/HYU V1
- Kia/HYU V2
- Kia/HYU V3
- Kia/HYU V4
- Kia/HYU V5
- Kia/HYU V6
- Kia V7
- Land Rover V0
- Mazda V0
- MazdaSiemens
- Mitsubishi V0
- PSA
- Porsche AG
- Renault V0
- Subaru
- Suzuki
- Star Line
- VAG

</details>

-----

- Transmit:<a id="transmit"></a><br>

**Transmit** generates Sub-GHz signals using supported protocols and user-defined values.

Signals can be configured directly from the device, transmitted immediately or saved to the SD card for later use.

### Transmit interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit_Signal_Editor.png" width="49%">
</p>

### Generated signal

<p align="center">

  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit_Keyboard.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit_Signal.png" width="49%">
  
</p>

<br>

### Supported protocols

<details>
<summary><b>Show supported transmission protocols</b></summary>

<br>

- Allstar Firefly
- Alutech AT-4N
- Ansonic
- BETT
- Beninca ARC
- CAME
- CAME Atomo
- CAME TWEE
- Cham_Code
- Clemsa
- Ditec GOL4
- Doitrand
- Dooya
- Elplast
- Faac SLH
- Feron
- GangQi
- GateTX
- Hay21
- Hollarm
- Holtek
- Holtek_HT12X
- Honeywell
- Honeywell Sec
- Hormann HSM
- Intertechno_V3
- Jarolift
- KeeLoq
- KeyFinder
- KingGates Stylo4k
- Legrand
- Linear
- LinearDelta3
- Magellan
- Marantec
- Marantec24
- Mastercode
- MegaCode
- Nero Radio
- Nero Sketch
- Nice FLO
- Nice FloR-S
- Nord ICE
- Phoenix_V2
- Power Smart
- Princeton
- Revers_RB2
- Roger
- SMC5326
- Security+ 1.0
- Security+ 2.0
- Somfy Keytis
- Somfy Telis
- Treadmill37

</details>

<br>

-----

## Tesla<a id="tesla"></a><br>

**Tesla** generates and transmits the known signal used to open the charging port door on compatible Tesla vehicles.

The appropriate frequency can be selected directly from the interface depending on the target region.

### Supported regions

- **EU** - 433.92 MHz
- **US** - 315.00 MHz

### Tesla interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Tesla.png" width="700">
</p>

-----

## Scanner<a id="scanner"></a><br>

**Scanner** analyzes signal strength (RSSI) across the frequencies available in the Sub-GHz frequency configuration.

When a signal exceeds the configured RSSI threshold, Willy Firmware identifies and displays the frequency with the strongest detected signal.

The detected frequency can then be applied directly to the general Sub-GHz settings.

### Scanner interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Scanner.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Scanner_Settings.png" width="49%">
</p>

### Frequency detected

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Scanner_Result.png" width="700">
</p>

-----

## Bruteforce<a id="bruteforce"></a><br>

**Bruteforce** generates Sub-GHz signals using supported fixed-code protocols while automatically iterating through possible code values.

A single signal can be transmitted using the currently selected value, or the complete sequence can be started to automatically increment the value after each transmission.

The current signal can also be saved to the SD card for later use.

Several parameters can be configured directly from the interface, including:

- Delay between transmissions
- Increment step
- Current code value

The increment step can be adjusted to move through the code range at different intervals, such as **1, 5, 10 or 30 values per step**.

### Bruteforce interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Bruteforce.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Bruteforce_Settings.png" width="49%">
</p>

<br>

### Supported protocols

<details>
<summary><b>Show supported bruteforce protocols</b></summary>

<br>

- Ansonic 12bit - 433.07 MHz
- Ansonic 12bit - 433.92 MHz
- Ansonic 12bit - 434.07 MHz
- CAME 12bit - 303.87 MHz
- CAME 12bit - 307.80 MHz
- CAME 12bit - 315.00 MHz
- CAME 12bit - 330.00 MHz
- CAME 12bit - 433.92 MHz
- CAME 12bit - 868.35 MHz
- Chamberlain 7bit - 300.00 MHz
- Chamberlain 7bit - 315.00 MHz
- Chamberlain 7bit - 390.00 MHz
- Chamberlain 8bit - 300.00 MHz
- Chamberlain 8bit - 315.00 MHz
- Chamberlain 8bit - 390.00 MHz
- Chamberlain 9bit - 300.00 MHz
- Chamberlain 9bit - 315.00 MHz
- Chamberlain 9bit - 318.00 MHz
- Chamberlain 9bit - 390.00 MHz
- Chamberlain 9bit - 433.92 MHz
- HT12X AM 12bit - 315.00 MHz
- HT12X AM 12bit - 433.92 MHz
- HT12X AM 12bit - 868.35 MHz
- HT12X AM 12bit - 915.00 MHz
- HT12X FM 12bit - 433.92 MHz
- Linear 10bit - 300.00 MHz
- Linear 10bit - 310.00 MHz
- LinearDelta3 8bit - 310.00 MHz
- Nice FLO 12bit - 433.92 MHz
- Nice FLO 12bit - 868.35 MHz
- PT2260 24bit - 315.00 MHz
- PT2260 24bit - 330.00 MHz
- PT2260 24bit - 390.00 MHz
- PT2260 24bit - 433.92 MHz
- PT2262 24bit - 315.00 MHz
- PT2262 24bit - 418.00 MHz
- PT2262 24bit - 430.00 MHz
- PT2262 24bit - 430.50 MHz
- PT2262 24bit - 433.92 MHz
- SMC5326 25bit - 330.00 MHz
- SMC5326 25bit - 433.92 MHz
- UNILARM 25bit - 330.00 MHz
- UNILARM 25bit - 433.92 MHz

</details>

<br>

-----

## DeBruijn<a id="debruijn"></a><br>

**DeBruijn** generates and transmits De Bruijn sequences based on supported fixed-code Sub-GHz protocols.

Instead of transmitting individual values one by one, the generated sequence combines possible code combinations into a compact transmission sequence for the selected protocol.

The protocol and operating frequency can be selected directly from the interface.

### DeBruijn interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/DeBruijn.png" width="700">
</p>

<br>

### Supported protocols

<details>
<summary><b>Show supported DeBruijn protocols</b></summary>

<br>

- Linear Multicode | 300.00 MHz
- Linear Multicode | 310.00 MHz
- Linear Multicode | 390.00 MHz
- Linear Multicode | 433.92 MHz
- Stanley Multicode | 300.00 MHz
- Stanley Multicode | 310.00 MHz
- Stanley Multicode | 390.00 MHz
- Stanley Multicode | 433.92 MHz
- Charmberlain | 300.00 MHz
- Charmberlain | 310.00 MHz
- Charmberlain | 390.00 MHz
- Charmberlain | 433.92 MHz
- Linear MooreMatic | 300.00 MHz
- Linear MooreMatic | 310.00 MHz
- Linear MooreMatic | 390.00 MHz
- Linear MooreMatic | 433.92 MHz

</details>

<br>

-----

## Jukebox<a id="jukebox"></a><br>

**Jukebox** provides a collection of known Sub-GHz remote-control commands used by compatible jukebox systems.

A command can be selected directly from the interface and transmitted using its predefined signal.

Available commands include playback controls, volume controls, queue management and other supported remote functions.

### Jukebox interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Jukebox.png" width="700">
</p>

<br>

### Supported commands

<details>
<summary><b>Show supported Jukebox commands</b></summary>

<br>

- Free Credit | 433.92 MHz
- Pause Song | 433.92 MHz
- Skip Song | 433.92 MHz
- Volume UP | 433.92 MHz
- Volume DOWN | 433.92 MHz
- Power OFF | 433.92 MHz
- Lock Queue | 433.92 MHz

</details>

<br>

-----

## Jammer<a id="jammer"></a><br>

**Jammer** is an experimental Sub-GHz interference-testing feature intended for controlled and authorized RF testing environments.

The interface provides different transmission modes, including **Carrier** and **Frame**, allowing the RF output behavior to be selected directly from the settings.

> [!CAUTION]
> Radio-frequency interference may disrupt nearby wireless devices and communications. Use this feature only in controlled environments where you are authorized to perform RF testing, and always comply with applicable local regulations.

### Jammer interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Jammer_Config.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Jammer_Settings.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Jammer.png" width="700">
</p>

<br>

-----

## Rolljam<a id="rolljam"></a><br>

**Rolljam** is an experimental proof-of-concept designed to demonstrate rolling-code capture and synchronization behavior in a controlled testing environment.

The application can collect between **2 and 5 received signals** during a test session and can communicate with a second Willy Firmware device over Wi-Fi to coordinate the testing workflow.

Once the capture session is complete, the collected signals are displayed in a dedicated signal list where they can be inspected and saved to the SD card for later analysis.

> [!CAUTION]
> This feature is intended exclusively for controlled research and authorized testing of systems you own or have permission to evaluate. Radio-frequency interference and unauthorized use of captured signals may be illegal and may disrupt nearby devices.

### Rolljam interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Rolljam.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Rolljam_Settings.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Rolljam_Signal_List.png" width="700">
</p>

<br>

-----

## Rollback<a id="rollback"></a><br>

**Rollback** is an experimental proof-of-concept for studying rolling-code behavior and signal sequences in controlled environments.

The application can capture and store between **2 and 5 signals** during a test session. It can also communicate with a second Willy Firmware device over Wi-Fi to coordinate the testing workflow.

After capture, the collected signals are displayed in a dedicated list where individual signals can be inspected and saved to the SD card for later analysis.

A **Sequence** mode is also available to replay a set of captured signals consecutively. The delay between sequence entries can be configured directly from the interface.

> [!CAUTION]
> This feature is intended exclusively for controlled research and authorized testing of systems you own or have permission to evaluate. Unauthorized replay of captured radio signals may be illegal or interfere with nearby systems.

### Rollback interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Rollback.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Rollback_Settings.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Rollback_Signal_List.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Rollback_Send_Sequence.png" width="49%">
</p>

<br>

-----

## Rolljam/Rollback Jammer<a id="jam_mode"></a><br>

**Rolljam/Rollback Jammer** is a companion mode designed to work with the experimental **Rolljam** and **Rollback** proof-of-concept applications.

It allows two Willy Firmware devices to communicate over Wi-Fi so that the secondary device can participate in a coordinated RF test session.

The mode can be controlled remotely by the primary Willy device, allowing the companion device to start and stop its configured test state as the Rolljam or Rollback workflow progresses.

> [!CAUTION]
> Jam Mode is intended exclusively for controlled RF research and authorized testing environments. Radio-frequency interference may disrupt nearby wireless devices and communications and may be restricted or prohibited by local regulations.

### Rolljam/Rollback Jammer interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Jammer_Roll.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Jammer_Roll_Start.png" width="49%">
</p>

<br>

-----

## POCSAG Read<a id="pocsag_read"></a><br>

**POCSAG Read** is a dedicated receiver for capturing and decoding POCSAG pager messages transmitted over Sub-GHz frequencies.

The receiver can monitor POCSAG transmissions independently of the destination **RIC** and automatically decode supported baud rates.

Received messages are stored temporarily in a signal list, allowing each transmission to be inspected individually along with its decoded information and message content.

### POCSAG Read interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Pocsag_Read.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Pocsag_Read_Signal_List.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Pocsag_Read_Signal.png" width="700">
</p>

<br>

-----

## POCSAG Send<a id="pocsag_send"></a><br>

**POCSAG Send** generates and transmits configurable POCSAG pager messages for compatible receivers.

The destination **RIC**, message content and baud rate can be configured directly from the device using the integrated keyboard and settings interface.

This allows custom POCSAG messages to be created and transmitted without requiring an external computer.

> [!CAUTION]
> Transmitting paging signals may be regulated and could interfere with active paging systems. Use this feature only with equipment and frequencies you are authorized to test, and always comply with applicable local regulations.

### POCSAG Send interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Pocsag_Send.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Pocsag_Settings.png" width="49%">
</p>

<br>

-----

### 💡 Infrared<a id="infrared"></a>

<p align="center">
  <a href="#infrared_learn">Learn</a> •
  <a href="#infrared_remote">Remote</a> •
  <a href="#infrared_tv_b_gone">TV-B-Gone</a>
</p>

Willy Firmware provides a complete set of **Infrared** tools for receiving, decoding, transmitting and managing IR signals directly from the device.

Infrared signals can be captured from existing remote controls, decoded using supported protocols or stored as RAW timing data when the protocol is unknown.

Captured signals can then be inspected, retransmitted or saved to the SD card for later use.

The Infrared section also includes additional tools such as universal remote-control functions for compatible devices.

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Infrared.png" width="700">
</p>

-----

## Infrared Learn<a id="infrared_learn"></a><br>

**Infrared Learn** receives and analyzes infrared signals from compatible remote controls and devices.

When a supported protocol is detected, Willy Firmware automatically decodes the signal and displays its protocol information and associated values.

Signals using an unknown or unsupported protocol can still be captured and stored as **RAW infrared timing data**, allowing them to be reproduced without requiring a dedicated decoder.

Received signals are temporarily stored in a signal list where they can be individually inspected, retransmitted or saved to the SD card for later use.

Signals saved from **Infrared Learn** use the same Flipper Zero-compatible `.ir` file format, allowing compatible infrared files to be exchanged and reused between Willy Firmware and Flipper Zero.

<details>
<summary><b>Show supported Infrared protocols</b></summary>

<br>

- RAW
- NEC
- NECext
- NEC42
- NEC42ext
- Samsung32
- RC6
- RC5
- RC5X
- SIRC
- SIRC15
- SIRC20
- Kaseikyo
- RCA

</details>

<br>

### Infrared Learn interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Learn.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Learn_Settings.png" width="49%">
</p>

### Received signal

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Learn_Signal.png" width="700">
</p>

### Signal list

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Learn_Signal_List.png" width="700">
</p>

<br>

-----

## Infrared Remote<a id="infrared-remote"></a><br>

**Infrared Remote** provides a collection of customizable infrared remote controls loaded directly from the SD card.

Remote controls are organized into different device categories.

### Infrared Remote interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Remote.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Remote2.png" width="49%">
</p>

Each remote is based on a **Flipper Zero-compatible `.ir` file** stored on the SD card, containing a collection of named infrared commands and their associated signal data.

When a remote is opened, its available commands can be selected and transmitted directly from the device.

Because the remote database is stored on the SD card, additional compatible `.ir` files and commands can be added without modifying or rebuilding the firmware.

### Infrared Send Remote interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Remote_TV.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Remote_Digital_Sign.png" width="49%">
    <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Remote_Projector.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Remote_LED.png" width="49%">
<br>
  ...
</p>

<br>

-----

## Infrared TV-B-Gone<a id="infrared_tv_b_gone"></a><br>

**Infrared TV-B-Gone** is a universal TV power-control feature based on a built-in database of known infrared power signals.

Unlike **Infrared Remote**, the signal database is embedded directly into Willy Firmware and does not require an SD card.

Two regional code databases are available directly from the interface:

- **Region NA** - North America
- **Region EU** - Europe

The application automatically transmits the supported power codes for the selected region, allowing compatible televisions to be controlled without selecting a specific manufacturer or remote profile.

### Infrared TV-B-Gone interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/TV_B_Gone.png" width="700">
</p>


<br>

-----

### 🟦 Bluetooth / BLE<a id="bluetooth"></a>

🚧 Documentation and firmware in progress.

-----

### 📶 Wi-Fi<a id="wifi"></a>

🚧 Documentation and firmware in progress.

-----

### 📱 NFC<a id="nfc"></a>

🚧 Documentation and firmware in progress.

-----

### 📡 nRF24<a id="nrf24"></a>

🚧 Documentation and firmware in progress.

-----

### ⚙️ Settings<a id="settings"></a>

<p align="center">
  <a href="#about">About</a> •
  <a href="#brightness">Brightness</a> •
  <a href="#color">Color</a> •
  <a href="#pin-code">PIN Code</a> •
  <a href="#usb-mode">USB Mode</a> •
  <a href="#shutdown">Shutdown</a> •
  <a href="#reboot">Reboot</a>
</p>

The **Settings** section provides access to device information, interface customization, security options and system controls.

Most configurable preferences are stored directly on the device and automatically restored after reboot.

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Settings.png" width="700">
</p>

-----

## About<a id="about"></a><br>

**About** provides an overview of the device's current hardware and system status.

It displays useful real-time information including **RAM usage, SD card capacity, battery level, battery voltage (mV), current consumption (mA) and device uptime**.

This screen provides a quick way to monitor the device's resources, power status and operating time directly from Willy Firmware.

### About interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/About.png" width="700">
</p>

<br>

-----

## Brightness<a id="brightness"></a><br>

**Brightness** allows the display backlight intensity to be adjusted directly from the device.

The selected brightness level is saved in the device settings and automatically restored after reboot.

### Brightness interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Brightness.png" width="700">
</p>

<br>

-----

## Color<a id="color"></a><br>

**Color** allows the main interface color to be customized directly from the device.

A color can be selected using the integrated color picker, allowing the appearance of Willy Firmware to be personalized according to the user's preference.

The selected color is saved in the device settings and automatically restored after reboot.

### Color interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Color.png" width="700">
</p>

<br>

-----

## PIN Code<a id="pin_code"></a><br>

**PIN Code** provides an optional security lock for Willy Firmware.

When enabled, a custom PIN code can be configured and stored in the device settings. The PIN will then be required to unlock the device after startup.

The integrated on-screen keyboard is used to enter and manage the PIN directly from the device.

### PIN Code interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/PIN_Code.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/PIN_Code_Edit.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/PIN_Code_Locked.png" width="700">
</p>

<br>

-----

## USB Mode<a id="usb-mode"></a><br>

**USB Mode** turns the device into a USB mass storage device, allowing the inserted SD card to be accessed directly from a connected computer.

Once enabled, the SD card appears on the computer as a removable USB drive, making it easy to browse, copy, add or manage files without removing the SD card from the device.

### USB Mode interface

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/USB_Mode.png" width="700">
</p>

<br>

-----

## Shutdown<a id="shutdown"></a><br>

**Shutdown** safely powers off the device directly from Willy Firmware.

Once the device is powered off, it can be turned back on by pressing 3x the **OK button**

<br>

-----

## Reboot<a id="reboot"></a><br>

**Reboot** restarts the device and reloads Willy Firmware.

This can be used to quickly restart the system after changing settings or whenever a fresh firmware initialization is required.

<br>

-----

# Development Status

**Willy Firmware V3 is currently under active development.**

Most core functionality is already implemented and functional, but applications, protocols and documentation may continue to evolve as development progresses.

More screenshots and detailed feature documentation will be added as additional sections of the firmware are finalized.

<br>

<h1 align="center">From Willy Firmware V2 to V3</h1><a id="fromwilly"></a>

**Willy Firmware V3 is the successor to Willy Firmware V2.**

V2 was developed around the **ESP32 T-Display-S3** with external hardware such as the CC1101.

V3 has been redesigned specifically around the **LILYGO T-Embed CC1101 platform**, providing much tighter integration between the firmware and the hardware.

Compared with V2, V3 introduces or improves:

- Native LILYGO T-Embed CC1101 support
- T-Embed CC1101 Plus support
- Integrated NFC support
- nRF24 support on compatible hardware
- Improved graphical interface
- Rotary encoder navigation
- Improved SD card integration
- Expanded Sub-GHz protocol support
- Persistent device and interface settings
- Improved hardware and shared SPI management
- A firmware architecture designed specifically around the T-Embed platform

The previous generation of Willy Firmware remains available here:

**[Willy Firmware V2 – ESP32 Flipper Zero Alternative](https://github.com/h-RAT/Willy_Firmware_V2_ESP32_Flipper_Zero_Alternative)**

-----

<br>

<h1 align="center">Contact</h1><a id="contact"></a>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_CC1101/main/Image/Discord.png" width="100" height="100"> 
  <br>
  <code>h_rat</code>
</p>

<h4 align="center">Website: https://willy-firmware.com/</h4>

<br>

-----

<br>

<h1 align="center">Disclaimer</h1><a id="disclaimer"></a>

Willy Firmware is intended for **educational, research and authorized security-testing purposes**.

Some features interact with radio-frequency, infrared, NFC, Bluetooth and Wi-Fi systems. Users are responsible for ensuring that their use of the firmware complies with applicable laws and regulations.

Do not use Willy Firmware to interfere with, access, test or control systems without authorization.

The developer assumes no responsibility for misuse of the firmware or for damages resulting from its use.

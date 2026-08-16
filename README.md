<h1 align="center"> <code>Willy Firmware V3</code> - Flipper Zero alternative for LILYGO T-Embed CC1101</h1><a id="introduction"></a>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_CC1101/main/Image/Logo.png">
</p>

<h2 align="center">
  <a href="#introduction">Introduction</a> | <a href="#features">Features</a> | <a href="#supported-hardware">Supported Hardware</a> | <a href="#fromwilly">V2 → V3</a> | <a href="#contact">Contact</a> | <a href="#disclaimer">Disclaimer</a>
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
- **Flipper file compatibility:** Compatible Sub-GHz and Infrared files can be saved, loaded and reused.
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

### 📡 Sub-GHz

Willy Firmware uses the integrated **CC1101** for Sub-GHz reception, decoding, transmission and signal analysis.

The firmware supports both known protocols and RAW signals, allowing signals to be received, analyzed, saved and reused directly from the device.

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz1.png" width="49%">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz2.png" width="49%">
</p>

-----

- Read RAW:<br>

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

- Read:<br>

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

- Transmit:<br>

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

## Scanner

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

### 💡 Infrared

🚧 Documentation and firmware in progress.

-----

### 🟦 Bluetooth / BLE

🚧 Documentation and firmware in progress.

-----

### 📶 Wi-Fi

🚧 Documentation and firmware in progress.

-----

### 📱 NFC

🚧 Documentation and firmware in progress.

-----

### 📡 nRF24

🚧 Documentation and firmware in progress.

-----
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

# Development Status

**Willy Firmware V3 is currently under active development.**

Most core functionality is already implemented and functional, but applications, protocols and documentation may continue to evolve as development progresses.

More screenshots and detailed feature documentation will be added as additional sections of the firmware are finalized.

<br>

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

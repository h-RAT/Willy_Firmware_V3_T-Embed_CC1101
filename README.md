<h1 align="center"> <code>Willy Firmware V3</code> - Flipper Zero alternative with T-Embed CC1101</h1><a id="introduction"></a>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_CC1101/main/Image/Logo.png">
</p>

<h2 align="center">
  <a href="#introduction">Introduction</a> | <a href="#features">Features</a> | <a href="#contact">Contact</a> | <a href="#disclaimer">Disclaimer</a>
</h2>

Willy Firmware V3 is a feature-rich firmware developed specifically for the LILYGO T-Embed CC1101 and T-Embed CC1101 Plus. Inspired by the Flipper Zero ecosystem, it brings Sub-GHz, Infrared, NFC, Wi-Fi, Bluetooth/BLE and nRF24 functionality together in a single ESP32-S3 device.

### Supported hardware

- LILYGO T-Embed CC1101
- LILYGO T-Embed CC1101 Plus

The Plus version is fully supported, including its additional nRF24 2.4 GHz radio.

<p align="center">
  <a href="https://discord.gg/VqsUsPQSmP"><img src="https://discordapp.com/api/guilds/1169681522715000873/widget.png?style=banner2" alt="Discord Banner 3"/></a>
</p>

<h4 align="center">Website: https://willy-firmware.com/</h4>

-----

<br>
<h1 align="center">What makes Willy Firmware special?</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/IMG_20260814_215202.jpg" width="500" alt="Willy">
</p>

Willy Firmware V3 was rebuilt specifically for the LILYGO T-Embed CC1101 platform, with a focus on stability, usability and hardware integration.

- **All-in-one:** Sub-GHz, Infrared, NFC, Wi-Fi, Bluetooth/BLE and nRF24.
- **T-Embed optimized:** Designed specifically for the ESP32-S3 based T-Embed CC1101 and CC1101 Plus.
- **Flipper file compatibility:** Read, save and reuse compatible Sub-GHz and Infrared files.
- **Actively developed:** New features, protocol support and improvements are regularly added.
<br>

<p align="center">
   <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Home.png" width="500" alt="Willy">
</p>

<br><br>
- <h4>Feature-rich: We include all common applications (Sub-GHz/Infrared/BLE/WiFi/NFC/NR24) in the firmware as well as new features.</h4>

- <h4>Stable: Many hours have been spent rewriting core parts of the firmware as well as some of its apps to ensure stability.</h4>

<br><br>

-----

<h1 align="center">Features:</h1><a id="features"></a>

### #Sub-GHz

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz1.png" width="500" alt="Willy">
  <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz2.png" width="500" alt="Willy">
</p>


-----

- Read RAW:<br>
Reads and decodes signals in a RAW format.

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW.png" width="500" alt="Willy">
    <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW_Settings.png" width="500" alt="Willy">
    <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW_Signal.png" width="500" alt="Willy">
</p>

From there you can send it or save it on the sd card for later use. 

-----

- Read:<br>
Reads and decodes signals based on known protocols. (You can save 50 signals in the memory)

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read.png" width="500" alt="Willy">
    <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Settings.png" width="500" alt="Willy">
    <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_List.png" width="500" alt="Willy">
        <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal.png" width="500" alt="Willy">
    <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_Generator.png" width="500" alt="Willy">


  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_List2.png" width="500" alt="Willy">
      <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal2.png" width="500" alt="Willy">
      <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_Signal_Generator2.png" width="500" alt="Willy">

</p>

From there you can send it or save it on the sd card for later use. 

<details>
<summary><b>Supported Sub-GHz decoders</b></summary>

- Allstar Firefly
- Alutech AT-4N
- Ansonic
- ...
- Treadmill37

</details>

<br>

```txt
[Supported decoders]
* Allstar Firefly
* Alutech AT-4N
* Ansonic
* BETT
* Beninca ARC
* CAME
* CAME Atomo
* CAME TWEE
* Cham_Code
* Clemsa
* Ditec GOL4
* Doitrand
* Dooya
* Elplast
* Faac SLH
* Feron
* GangQi
* GateTX
* Hay21
* Hollarm
* Holtek
* Holtek_HT12X
* Honeywell
* Honeywell Sec
* Hormann HSM
* Intertechno_V3
* Jarolift
* KeeLoq
* KeyFinder
* KingGates Stylo4k
* Legrand
* Linear
* LinearDelta3
* Magellan
* Marantec
* Marantec24
* Mastercode
* MegaCode
* Nero Radio
* Nero Sketch
* Nice FLO
* Nice FloR-S
* Nord ICE
* Phoenix_V2
* Power Smart
* Princeton
* Revers_RB2
* Roger
* SMC5326
* Security+ 1.0
* Security+ 2.0
* Somfy Keytis
* Somfy Telis
* Star Line
* Treadmill37

[Supported vehicle decoders]

* Chrysler
* FIAT SPA
* FORD V0
* Ford V1
* Ford V2
* KIA/HYU V0
* KIA/HYU V1
* KIA/HYU V2
* KIA/HYU V3/V4
* KIA/HYU V5
* KIA/HYU V6
* Kia V7
* Land Rover V0
* MARELLI
* Mazda V0
* MazdaSiemens
* Mitsubishi V0
* PSA GROUP
* PSA OLD
* Porsche AG
* Renault V0
* SUBARU
* SUZUKI
* Star Line
* VAG GROUP
```

-----

- Transmit:<br>
Generates and sends signals based on known protocol and key.

<p align="center">  
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit.png" width="500" alt="Willy">
      <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit_Signal_Editor.png" width="500" alt="Willy">
      <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit_Keyboard.png" width="500" alt="Willy">
      <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Transmit_Signal.png" width="500" alt="Willy">
</p>

From there you can send it or save it on the sd card for later use. 

<br>

```txt
[Supported protocols]

* Allstar Firefly
* Alutech AT-4N
* Ansonic
* BETT
* Beninca ARC
* CAME
* CAME Atomo
* CAME TWEE
* Cham_Code
* Clemsa
* Ditec GOL4
* Doitrand
* Dooya
* Elplast
* Faac SLH
* Feron
* GangQi
* GateTX
* Hay21
* Hollarm
* Holtek
* Holtek_HT12X
* Honeywell
* Honeywell Sec
* Hormann HSM
* Intertechno_V3
* Jarolift
* KeeLoq
* KeyFinder
* KingGates Stylo4k
* Legrand
* Linear
* LinearDelta3
* Magellan
* Marantec
* Marantec24
* Mastercode
* MegaCode
* Nero Radio
* Nero Sketch
* Nice FLO
* Nice FloR-S
* Nord ICE
* Phoenix_V2
* Power Smart
* Princeton
* Revers_RB2
* Roger
* SMC5326
* Security+ 1.0
* Security+ 2.0
* Somfy Keytis
* Somfy Telis
* Treadmill37
```

<br>

-----

- Scanner:<br>
During analysis, the device scans signal strength (RSSI) at all the frequencies available in frequency configuration. 
Then displays the frequency with the highest RSSI value, with signal strength higher than the configured threshold.

<p align="center">  
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Scanner.png" width="500" alt="Willy">
      <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Scanner_Result.png" width="500" alt="Willy">
</p>

From there you can apply the found frequency for the general settings.



-----
Update in progress...

-----

<br>

<h1 align="center">Contact:</h1><a id="contact"></a>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_CC1101/main/Image/Discord.png" width="100" height="100"> 
  <br>
  <code>h_rat</code>
</p>

<h4 align="center">Website: https://willy-firmware.com/</h4>

<br>

-----

<br>

<h1 align="center">Disclaimer:</h1><a id="disclaimer"></a>

Willy Firmware is intended for educational, research and authorized security-testing purposes.

Some features interact with radio-frequency, infrared, NFC, Bluetooth and Wi-Fi systems. Users are responsible for ensuring that their use of the firmware complies with applicable laws and regulations.

Do not use Willy Firmware to interfere with, access, test or control systems without authorization.

The developer assumes no responsibility for misuse of the firmware or for damages resulting from its use.

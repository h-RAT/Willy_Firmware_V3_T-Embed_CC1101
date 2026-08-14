<h1 align="center"> <code>Willy Firmware V3</code> - Flipper Zero alternative with T-Embed CC1101</h1><a id="introduction"></a>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_CC1101/main/Image/Logo.png">
</p>

<h2 align="center">
  <a href="#introduction">Introduction</a> | <a href="#features">Features</a> | <a href="#contact">Contact</a> | <a href="#disclaimer">Disclaimer</a>
</h2>

This firmware is an alternative to Flipper Zero for ESP-32, and is always updated from the original Flipper ideas, making it the most stable alternative.

<p align="center">
  <a href="https://discord.gg/VqsUsPQSmP"><img src="https://discordapp.com/api/guilds/1169681522715000873/widget.png?style=banner2" alt="Discord Banner 3"/></a>
</p>

<h4 align="center">Website: https://willy-firmware.com/</h4>

-----

<br>
<h1 align="center">What makes it special?</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/IMG_20260814_215202.jpg" width="500" alt="Willy">
</p>

We have spent many hours perfecting this code even further, and getting the most out of it.

The goal of this firmware is to be able to benefit from the same functions as the Flipper Zero but on an ESP32, which is cheaper, and easier to obtain in some countries, as well as to regularly bring out amazing updates based on what the community wants, with a real understanding of what is happening. Fixing regularly talked about bugs and expanding capabilities with exciting new features and, most importantly, ensuring the simplest user experience possible.

<br>

<p align="center">
   <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Home.png" width="500" alt="Willy">
</p>

<br><br>
- <h4>Feature-rich: We include all common applications (SubGhz/Infrared/BLE/WiFi/NFC/NR24) in the firmware as well as new features.</h4>

- <h4>Stable: Many hours have been spent rewriting core parts of the firmware as well as some of its apps to ensure stability.</h4>

<br><br>

-----

<h1 align="center">Features:</h1><a id="features"></a>

### #SubGhz

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz1.png" width="500" alt="Willy">
  <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/SubGhz2.png" width="500" alt="Willy">
</p>


-----

- Read RAW:<br>
Reads and decode signals in a raw format, including signals from remotes with unknown protocols.

<p align="center">
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW.png" width="500" alt="Willy">
    <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW_Settings.png" width="500" alt="Willy">
    <br><br> 
  <img src="https://raw.githubusercontent.com/h-RAT/Willy_Firmware_V3_T-Embed_CC1101/refs/heads/main/Image/Read_RAW_Signal.png" width="500" alt="Willy">
</p>

From there you can send it or save it on the sd card for use it later. 

-----

- Read:<br>
Reads and decodes signals based on known protocols. If the protocol is static, Willy decode the signal. (You can save 50 signals in the memory)

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

From there you can send it or save it on the sd card for use it later. 

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


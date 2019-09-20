---
oldwikiname: Grove - LoRa Radio
prodimagename: cover.jpg
surveyurl: 'https://www.research.net/r/F5K3G3F'
bzurl: 'https://www.seeedstudio.com'
title: Grove - LoRa Radio
tags: 'grove_uart, io_3v3, io_5v, plat_duino'
sku: 113060006/113060007
category: Communication
---

# Grove LoRa Radio

![](https://raw.githubusercontent.com/SeeedDocument/Grove_LoRa_Radio/master/img/cover.jpg)

Grove is a very powerful platform developed by Seeed Studio to simplify your IoT projects.We have integrated the grove connector to most boards produced by Seeed to make them become a system. This time, we combined Grove with LoRa to provide an ultra-long-range wireless module for you.

The main functional module in Grove - LoRa Radio 433MHz is RFM98, which is a transceiver features the LoRa long range modem that provides ultra-long range spread spectrum communication and high interference immunity whilst mini-missing current consumption. The heart of Grove - LoRa Radio 433MHz is ATmega168, a widely used chip with very high-performance and low power consumption, especially suitable for this grove module.

There we already integrated a simple wire antenna to receive signal, if the signal is too weak to receive, don’t worry, the MHF connector next to the antenna is for adding a second antenna which has MHF interface to gain more signal.

This is the 433MHz version, which can be used for 433MHz communication. You can also find the version for 868MHz at Grove - LoRa Radio 868MHz.

| Version | Released Date | How to Buy |
| :--- | :--- | :--- |
| Grove - LoRa Radio 433 MHz | Dec 10, 2016 | [![](https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png)](https://www.seeedstudio.com/Grove-LoRa-Radio-433MHz-p-2777.html) |
| Grove - LoRa Radio 868 MHz | Dec 10, 2016 | [![](https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png)](https://www.seeedstudio.com/Grove-LoRa-Radio-868MHz-p-2776.html) |

## Features

* Using RFM95 module based on SX1276 LoRa®
* Working Voltage:5V/3.3V
* ~28mA\(Avg\) @+20dBm continuous transmit
* ~8.4mA\(Avg\)@standby mode
* ~20mA\(Avg\) @receive mode, BW-500kHz
* Working Temperature:-20 – 70℃
* Interface:Grove - UART\(RX,TX,VCC,GND\)
* Simple wire antenna or MHF Connector for external high gain antenna
* Working Frequency:868MHz/433MHz
* +20dBm 100 mW Power Output Capability
* Size:20\*40mm
* Rate:0.3kps~50kps
* Ready-to-go Arduino libraries
* Resered MHF antenna connector

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove_System/)

## Platforms Supported

## Hardware Overview

![](https://raw.githubusercontent.com/SeeedDocument/Grove_LoRa_Radio/master/img/hardware.png)

1. ATMega168 MCU \([datasheet](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/Atmel-2545-8-bit-AVR-Microcontroller-ATmega48-88-168_Datasheet.pdf)\)
2. MHF Connector
3. Wire Antenna
4. RFM95 Module \([datesheet](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/RFM95_96_97_98_DataSheet.pdf)\)
5. Grove Interface

| PIN | NAME | FUNCTION |
| :--- | :--- | :--- |
| 1 | TX | TX of UART |
| 2 | RX | RX of UART |
| 3 | VCC | Power supply, 3.3V or 5V |
| 4 | GND | Connect Ground |

## Application Ideas

* Internet of Things
* Smart Home
* Sensor Hub
* Long distance wireless communication

## Getting Started

After this section, you can make **Grove - LoRa Radio** run with only few steps.

### Preparations

Now we are making a demo for P2P\(point to point\) communication with the Grove - Lora Radio 433MHz, the Grove - LoRa Radio 868MHz is the same way to use.

!!!Tip Grove - LoRa Radio 433MHz can't talk to Grove - LoRa Radio 868MHz.

| Item | Qty | Link |
| :--- | :--- | :--- |
| Seeeduino Lotus | 2 | [GET ONE NOW!](https://www.seeedstudio.com/Seeeduino-Lotus-ATMega328-Board-with-Grove-Interface-p-1942.html) |
| Grove - LoRa Radio 433MHz | 2 | [GET ONE NOW!](https://www.seeedstudio.com/Grove-LoRa-Radio-433MHz-p-2777.html) |
| Micro USB Cable | 2 | [GET ONE NOW!](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html) |

If this is your first time using [Seeeduino Lotus](https://www.seeedstudio.com/Seeeduino-Lotus-ATMega328-Board-with-Grove-Interface-p-1942.html), please refer to [Seeeduino Lotus's wiki](http://www.seeedstudio.com/wiki/Seeeduino_Lotus_v1.0).

Seeeduino Lotus is fully compatible with Arduino which works as simple as Arduino.

If this is your first time using Arduino, Please put hand on [here](http://arduino.cc) to start your Arduino journey.

### Connecting hardware

[Seeeduino Lotus](https://www.seeedstudio.com/Seeeduino-Lotus-ATMega328-Board-with-Grove-Interface-p-1942.html) is a combination of Seeeduino and Base Shield. We can connect the LoRa Radio module to the D5 socket directly as the below picture shows.

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LoRa_Radio/master/img/demo.jpg)

### Download Library

Click to download the library and install it \([How to install an Arduino Library](http://wiki.seeed.cc/How_to_install_Arduino_Library/)\)

[![](https://raw.githubusercontent.com/SeeedDocument/Grove_LoRa_Radio/master/img/library.png)](https://github.com/Seeed-Studio/Grove_LoRa_433MHz_and_915MHz_RF/archive/master.zip)

### Open the example

Open your Arduino IDE, click **File &gt; Examples&gt;Grove\_LoRa\_433MHz\_and\_915MHz\_RF-master** you will get many examples for the module.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_LoRa_Radio/master/img/library_2.png)

| Node | Example Name | Function |
| :--- | :--- | :--- |
| Sender | rf95\_client | Send "Hello World" every 1s |
| Receiver | rf95\_server | Receive data and print it |

Click **Tools&gt;Board** to choose "Seeeduino Lotus" and select respective serial port then click on Upload button to finish the steps.

!!!Tip If you're using Grove - LoRa Radio 868MHz module change the following code.

```c
//rf95.setFrequency(434.0);
rf95.setFrequency(868.0);
```

### Review Results

After upload completed, you can open the serial monitor to see the result.

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LoRa_Radio/master/img/result.jpg)

### Data Rate

The below chart shows the relationships between the band rate signal band width spreding factor and sensitivity.

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_LoRa_Radio/master/img/DateRate.png)

## Resources

* _**Schematics**_
  * [Grove - LoRa Radio 433MHz v1.0 Schematics \(Eagle files\)](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/433_eagle.zip)
  * [Grove - LoRa Radio 433MHz v1.0 Schematics \(PDF files\)](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/433_sch.pdf)
  * [Grove - LoRa Radio 868MHz v1.0 Schematics \(Eagle files\)](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/868_eagle.zip)
  * [Grove - LoRa Radio 868MHz v1.0 Schematics \(PDF files\)](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/868_sch.pdf)
* _**Datasheet**_
  * [RFM95/96/97 Datasheet](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/RFM95_96_97_98_DataSheet.pdf)
  * [Atmega168 Datasheet](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/Atmel-2545-8-bit-AVR-Microcontroller-ATmega48-88-168_Datasheet.pdf)
* _**References**_
  * [LoRa Alliance](https://www.lora-alliance.org/)
* _**Library**_
  * [Grove - LoRa Radio Library and Examples](https://github.com/Seeed-Studio/Grove_LoRa_433MHz_and_915MHz_RF/)
* [_**Download ALL Above**_](https://github.com/SeeedDocument/Grove_LoRa_Radio/blob/master/res/res.zip)


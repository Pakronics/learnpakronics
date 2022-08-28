---
oldwikiname: Grove_-_6-Axis_Accelerometer&Gyroscope
bzprodimageurl: http://statics3.seeedstudio.com/images/product/105020012 3.jpg
prodimagename: Grove-6-Axis_AccelerometerAndGyroscope_product_view_1200_s.jpg
surveyurl: https://www.research.net/r/Grove-6-Axis_AccelerometerAndGyroscope
bzurl: https://seeedstudio.com/Grove-6-Axis-Accelerometer&Gyroscope-p-2606.html
title: Grove - 6-Axis Accelerometer&Gyroscope
tags: plat_duino, plat_pi, plat_bbg, plat_linkit -->
sku: 105020012
category: Sensor
---

# Grove 6 Axis Accelerometer And Gyroscope

![](https://raw.githubusercontent.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/master/img/Grove-6-Axis\_AccelerometerAndGyroscope\_product\_view\_1200\_s.jpg)

Grove - 6-Axis Accelerometer\&Gyroscope is a cost-effective Grove interfaced and integrated sensor combination of 3-axis digital accelerometer and 3-axis digital gyroscope.

With a serious low power consumption digital chip LSM6DS3([datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/master/res/LSM6DS3TR.pdf)) and power supply regulator inside, it features high sensitivity, green tech and low noise interference. It can be configured to different sensitivity levels of acceleration and different angular rate measurement range. Provided with detailed SDK, it can make the prototyping process quicker and easier.

This product can be used for different applications for tilt, motion, and tap sensings, such as robotics, IoT devices and consumer electronic devices.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get\_One\_Now\_Banner.png)](https://www.seeedstudio.com/Grove-6-Axis-Accelerometer\&Gyroscope-p-2606.html)

## Features

* Grove interfaced and cost-effective.
* Digital-output for 6 DOF motion data.
* ±2/±4/±8/±16 g full scale leaner acceleration sensing range for various environment.
* ±125, ±245, ±500, ±1000, ±2000 degree per seconds(dps) for angular rate measurement range make it versatile.
* Detailed SDK for easier programming.
* Regulated power supply for reliable data to be collected.
* Programmed interrupts for different event.
* 8 kB data buffering.

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

## Application ideas

* Robotics
* Consumer-level aircraft
* Computer input devices
* Wearable devices.
* IoT things

## Specifications

For detailed information please refer to [datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/master/res/LSM6DS3TR.pdf).

| Parameter                             | Value                                                                                |
| ------------------------------------- | ------------------------------------------------------------------------------------ |
| Analog supply voltage:                | 5V/3.3V(DC)                                                                          |
| Power consumption:                    | 0.9 mA in combo normal mode and 1.25 mA in combo high-performance mode up to 1.6 kHz |
| Linear acceleration measurement range | ±2/±4/±8/±16 g full scale (typical value)                                            |
| Angular rate measurement range        | ±125, ±245, ±500, ±1000, ±2000 dps(typical value)                                    |
| Linear acceleration sensitivity       | 0.061(FS = ±2), 0.122(FS = ±4), 0.244(FS = ±8), 0.488(FS = ±16) mg/LSB               |
| Angular rate sensitivity              | 4.375(FS = ±125), 8.75(FS = ±245), 17.50(FS = ±500), 35(FS = ±1000), 70(FS = ±2000)  |

### Platforms Supported

Note If no version number is not represented for a specific platform, it means this product support all versions within this platform. But you will need additional corresponding Grove shield board such as Grove - Base Shield v2.

## Hardware Overview

![](https://raw.githubusercontent.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/master/img/Grove-6-Axis\_AccelerometerAndGyroscope\_components\_view\_1200\_s.jpg)

**Grove Port**\
Connect main control board such as Seeeduino board with driver board.

**LSM6DS3**\
Main MCU.

### **Parts list**

| Parts name                              | Quantity |
| --------------------------------------- | -------- |
| Grove - 6-Axis Accelerometer\&Gyroscope | 1PC      |
| Grove wire                              | 1PC      |

## Get started

### **Material required**

* Seeeduino \* 1
* Grove - Base Shield v2

### **Preparations**

Refer to following guides to build an appropriate IDE:

Note We have chosen Seeeduino and it is compatible with Arduino in this case. You can also use Arduino board instead.

[Getting Started on Windows](https://app.gitbook.com/Seeeduino\_v4.2#Getting\_Started\_on\_Windows)

[Getting Started on Mac OS X](https://app.gitbook.com/Seeeduino\_v4.2#Getting\_Started\_on\_Mac\_OS\_X)

### **Hardware connections**

![](https://raw.githubusercontent.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/master/img/Grove-6-Axis\_AccelerometerAndGyroscope\_demo\_connection\_1200\_s.jpg)

Note Plug Grove - 6-Axis Accelerometer\&Gyroscope to I2C interface on Grove - Base shield. Connect power supply with USB cable.

### **A little demo**

Download the [library](https://github.com/Seeed-Studio/Accelerometer\_And\_Gyroscope\_LSM6DS3) for Grove - 6-Axis Accelerometer\&Gyroscope. Refer to \[Guide to use demos downloaded from Seeed's Github]\(/Guide\_to\_use\_demos\_downloaded\_from\_Seeed's\_Github) for quicker flashing your code to main controller board. There are three demo examples in total in sub directory _**examples**_.

## Resources

* **\[Eagle]** [Grove - 6-Axis Accelerometer\&Gyroscopev 1.0](https://github.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/raw/master/res/Grove%20-%206-Axis%20AccelerometerGyroscopev1.0.zip)
* **\[PDF]** [Grove - 6-Axis Accelerometer\&Gyroscopev 1.0 SCH](https://github.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/raw/master/res/Grove%20-%206-Axis%20Accelerometer%26Gyroscope%20v1.0-SCH.zip)
* **\[PDF]** [Grove - 6-Axis Accelerometer\&Gyroscopev 1.0 PCB](https://github.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/raw/master/res/Grove%20-%206-Axis%20Accelerometer%26Gyroscope%20v1.0\_PCB.pdf)
* **\[Library]** [Grove-6-Axis\_AccelerometerAndGyroscope](https://github.com/Seeed-Studio/Accelerometer\_And\_Gyroscope\_LSM6DS3)
* **\[Datasheet]** [Datasheet of LSM6DS3](https://raw.githubusercontent.com/SeeedDocument/Grove-6-Axis\_AccelerometerAndGyroscope/master/res/LSM6DS3TR.pdf)

---
oldwikiname: Grove_-_Digital_Infrared_Temperature_Sensor
bzprodimageurl: http://statics3.seeedstudio.com/images/product/101020077 1.jpg
prodimagename: Grove－Digital_Infrared_Temperature_Sensor_4.jpg)
surveyurl: https://www.research.net/r/Grove-Digital_Infrared_Temperature_Sensor
bzurl: https://seeedstudio.com/Grove-Digital-Infrared-Temperature-Sensor-p-2385.html
title: Grove - Digital Infrared Temperature Sensor
tags: grove_i2c, io_3v3, io_5v, plat_duino, plat_linkit
sku: 101020077
category: Sensor
---

# Grove Digital Infrared Temperature Sensor

| ![](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/img/Grove%EF%BC%8DDigital\_Infrared\_Temperature\_Sensor\_1.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/img/Grove%EF%BC%8DDigital\_Infrared\_Temperature\_Sensor\_2.jpg) |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

The Digital Infrared temperature sensor is a non-contact temperature measurement module which bases on MLX90615.Both the IR sensitive thermopile detector chip and the signal conditioning chip are integrated in the same package.This module communicates with Arduino using SMBus,up to 127 sensors can be read via common 2 wires.Thanks to the module's low noise amplifier, 16-bit ADC and powerful DSP unit, it can achieved a high accuracy of 1℃ over wide temperature rage and a high measurement resolution of 0.02℃.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get\_One\_Now\_Banner.png)](http://www.seeedstudio.com/Grove-Digital-Infrared-Temperature-Sensor-p-2385.html)

## Specifications

|  Item                      |  Min       |  Typical |  Max |  Unit |
| -------------------------- | ---------- | -------- | ---- | ----- |
|  Voltage                   |  2.6       |  3       |  3.4 |  V    |
|  Current                   |            |  1.4     |  1.5 |  mA   |
|  Ambient Temperature Range |  -40 - 85  |  ℃       |      |       |
|  Object Temperature Range  |  -40 - 115 |  ℃       |      |       |
|  Dimension                 |  20x40x9.6 |  mm      |      |       |

## Platforms Supported

## Hardware Overview

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/img/Grove%EF%BC%8DDigital\_Infrared\_Temperature\_Sensor\_4.jpg)

| Pin Number | Name | Type   | Function Description                             |
| ---------- | ---- | ------ | ------------------------------------------------ |
| 1          | GND  | -      | Signal ground                                    |
| 2          | VCC  | in     | Positive Power Supply Input Terminal(3.3V or 5V) |
| 3          | SDA  | in/out | I2C data input/output                            |
| 4          | SCL  | in     | I2C CLK                                          |

## Usage

We will provide an example here to show you how to use this sensor to measure the temperature of the target which is in front of the sensor,and print the result on the serial monitor.

* Connect this module to seeeduino using [Grove - Base Shield](https://app.gitbook.com/Base\_Shield\_V2) port D2.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/img/Digital\_Infrared\_Temperature\_Sensor4.JPG)

### Software Part

1. Download the library and demo code [Digital\_Infrared\_Temperature\_Sensor\_MLX90615](https://github.com/Seeed-Studio/Digital\_Infrared\_Temperature\_Sensor\_MLX90615).
2. Unzip it into the libraries file of Arduino IDE by the path: ..\arduino-1.0.5\libraries.
3.  Open the demo code directly by the path:File -> Examples ->Digital\_Infrared\_Temperature\_Sensor\_MLX90615->MLX90615Soft.

    You can see :

    ![](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/img/MLX90615\_demo\_code.jpg)

    Since the sensor is factory calibrated with the digital SMBus compatible interface enabled,but the library is based on a soft i2c library,so you can use any digital pins on any AVR chip to drive the SDA and SCL lines.We use D2 as the SCL pin and D3 as the SDA pin in this demo code.
4. Upload the code into Arduino.
5.  Start up the Serial Monitor.

    You can see :

    ![](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/img/Digital\_Infrared\_Temperature\_Sensor\_Serial\_Monitor.jpg)

Now, you can measure the temperature with this sensor.Ambient temperature is the MLX90615 package temperature and Object temperature is the object target temperature.According to our experiment,when you place the sensor in the normal indoor temperature,and ensure that there is nothing source of heat in front of the sensor's 1M scope.The Object temperature will approximately equal to Ambient temperature.When measuring the Object temperature,you should ensure the object is as close as possible whit the sensor,but do not touch the surface of the sensor,we recommend the distance is less than 3cm. Wish you have a fun try.

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

## Resources

* [Grove Digital Infrared Temperature Sensor v1.0 eagle file.zip](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/res/Grove\_Digital\_Infrared\_Temperature\_Sensor\_v1.0\_eagle\_file.zip)
* [MLX90615.pdf](https://raw.githubusercontent.com/SeeedDocument/Grove-Digital\_Infrared\_Temperature\_Sensor/master/res/MLX90615.pdf)
* [Demo Code](https://github.com/Seeed-Studio/Digital\_Infrared\_Temperature\_Sensor\_MLX90615)

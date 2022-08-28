---
oldwikiname: Grove_-_Differential_Amplifier_v1.2
bzprodimageurl: https://statics3.seeedstudio.com/images/103020016 1.jpg
prodimagename: Grove-Differential_Amplifier_v1.2.jpg
surveyurl: https://www.research.net/r/Grove-Differential_Amplifier_v1_2
bzurl: https://www.seeedstudio.com/Grove-Differential-Amplifier-p-1284.html
title: Grove - Differential Amplifier v1.2
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit
sku: 103020016
category: Others
---

# Grove Differential Amplifier v1.2

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Differential\_Amplifier\_v1.2/master/img/Grove-Differential\_Amplifier\_v1.2.jpg)

This Grove is designed for precise differential-input amplification. Input the differential signals of your sensor to this module through the male pins, then your Arduino will get a precisely amplified output from the Grove interface. The gain scale factor is selectable. You can get a 35 times or 1085 times amplification via a switch on the board.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get\_One\_Now\_Banner.png)](http://www.seeedstudio.com/Grove-Differential-Amplifier-p-1284.html)

## Features

* High amplifying precision
* Selectable scale factor
* Can be conveniently read by Arduino

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

## Applications

* Data acquisition
* Battery operated systems
* Pressure and temperature bridge amplifiers
* General purpose instrumentation

## Specifications

|  Item              |  Min       |  Typical |  Max            |  Unit |    |
| ------------------ | ---------- | -------- | --------------- | ----- | -- |
|  Operating Voltage |  2.7       |  5.0     |  5.5            |  VDC  |    |
|  Input Voltage     |  0.1       |  \\\\    |  (Vcc-0.8)/Gain |  mV   |    |
|  Output Voltage    |  0         |  \\\\    |  Vcc-0.80       |  mV   |    |
|  Gain              |  Select 35 |  /       |  35             |  /    |  / |
|  Select 1085       |  /         |  1085    |  /              |       |    |

## Platforms Supported

## Usage

**1. Sensor Choosing**

The amplifier can turn signals in mA scale up to A scale. Before using it, make sure the output range of your sensor is in mA scale. For example, [Weight Sensor](https://app.gitbook.com/Weight\_Sensor-Load\_Cell-0-500g) is one of them.

**2. Connector Reforming**

To pair the weight sensor up with the male pins on the amplifier, female connectors need to be soldered on its wires.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Differential\_Amplifier\_v1.2/master/img/Solder.jpg)

**3. Hardware Hookup**

Connect the weight sensor to the amplifier as the picture depicts below.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Differential\_Amplifier\_v1.2/master/img/Connect5.jpg)

**4. Measurement**

Copy and paste the demo code below to Arduino IDE and upload it.

```
    void setup()
    {
      Serial.begin(9600);
      Serial.println("start");
    }

    void loop()
    {
      int i;
      int value;
      float V,Vo;
      float Sum=0;
      for(i=0;i<10;i++)
      {
        value=analogRead(4);
        V=value*5.00/1023;
        Sum+=V;
        delay(10);
      }
      Vo=Sum/10;
      Serial.print("Output score:");
      Serial.println(Vo);
      delay(1000);
    }
```

You can view the amplified signals via serial monitor. For the value of the input signal, you need to use the multimeter to measure the voltage difference between VIN+ and VIN-.

## Resources

* [v1.2 Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Differential\_Amplifier\_v1.2/master/res/Grove-Differential\_Amplifier\_v1.2\_eagle.zip)
* [v1.2 Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Differential\_Amplifier\_v1.2/master/res/Grove-Differential\_Amplifier\_v1.2.pdf)
* [INA132 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Differential\_Amplifier\_v1.2/master/res/Ina132.pdf)

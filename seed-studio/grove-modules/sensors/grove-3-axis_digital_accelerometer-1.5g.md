---
oldwikiname: Grove_-_3-Axis_Digital_Accelerometer(±1.5g)
bzprodimageurl: 'http://statics3.seeedstudio.com/images/101020039 1.jpg'
prodimagename: 3_aix_acc.jpg
surveyurl: 'https://www.research.net/r/Grove-3-Axis_Digital_Accelerometer-1_5g'
bzurl: 'https://seeedstudio.com/Grove-3-Axis-Digital-Accelerometer(±1.5g)-p-765.html'
title: Grove - 3-Axis Digital Accelerometer(±1.5g)
tags: 'grove_i2c, io_3v3, io_5v, plat_duino, plat_linkit, plat_wio'
sku: 101020039
category: Sensor
---

# Grove 3 Axis Digital Accelerometer 1.5g

| ![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/3_aix_acc.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Grove-3-Axis_v1.3.jpg) |
| :--- | :--- |
|  Grove - 3-Axis Digital Accelerometer v1.2 |  Grove - 3-Axis Digital Accelerometer v1.2b |

3-Axis Digital Accelerometer is the key part in projects like orientation detection, gesture detection and Motion detection. This 3-Axis Digital Accelerometer\(±1.5g\) is based on Freescale's low power consumption module, MMA7660FC. It features up to 10,000g high shock survivability and configurable Samples per Second rate. For generous applications that don't require too large measurement range, this is a great choice because it's durable, energy saving and cost-efficient.

\[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)\]\([http://www.seeedstudio.com/Grove-3-Axis-Digital-Accelerometer\(%C2%B11.5g\)-p-765.html](http://www.seeedstudio.com/Grove-3-Axis-Digital-Accelerometer%28%C2%B11.5g%29-p-765.html)\)

## Specifications

* Working voltage: 3.0 - 5.5V
* Off Mode Current: 0.4μA
* Standby Mode Current: 2μA
* Active Mode Current: 47 μA at 1 ODR
* Test Range: ±1.5g
* Sensitivity: 21LSB/g
* Suli-compatible Library

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove_System/)

## Platforms Supported

Note For more details about Suli-compatible Library, please refer to [Suli](/Suli).

## Demonstration

### With [Arduino](/Arduino)

Here we are going to show you how to get raw data and data measured by "g" from this sensor.

Connect this module to the I2C port of Grove - Base Shield via a Grove cable.

Note If you want to activate the Interrupt function of this module, you need to connect the INT soldering pad we broke out on the board with a pin of Arduino that's capable of Interrupt Service Routine.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Digital_Accelerometer_Sensor_Connector1.5g.jpg)

Install the library we provide in the [Resources](/Grove-3-Axis_Digital_Accelerometer-1.5g#resources) section.

Open the code directly by the path:File -&gt; Example -&gt;DigitalAccelerometer\_MMA7660FC -&gt;MMA7660FC\_Demo.

In this program, acceleration information are sent from the sensor to Seeeduino via I2C bus and then Seeeduino printed them onto the serial monitor. Open the serial monitor to check the result.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Grove-3-Axis_Digital_Accelerometer-1.5g-.jpg)

The outputs of this sensor consist of two parts: raw data and 3-axis acceleration info converted into the unit of gravity, "g".

### With Raspberry Pi

1.You should have got a raspberry pi and a grovepi or grovepi+.

2.You should have completed configuring the development enviroment, otherwise follow [here](/GrovePiPlus).

3.Connection

* Plug the sensor to grovepi socket i2c-x\(1~3\) by using a grove cable.

4.Navigate to the demos' directory:

```text
   cd yourpath/GrovePi/Software/Python/
```

* To see the code

```text
    nano grove_i2c_accelerometer.py   # "Ctrl+x" to exit #
```

```text
    import time
    import grovepi

    # Connect the Grove Accelerometer (+/- 1.5g) to any I2C port eg. I2C-1
    # Can be found at I2C address 0x4c
    # SCL,SDA,VCC,GND

    while True:
        try:
            print grovepi.acc_xyz()
            time.sleep(.5)

        except IOError:
            print "Error"
```

5.Run the demo.

```text
    sudo python grove_i2c_accelerometer.py
```

## Reference

Below are two figures helping you understand the physical meaning of the result.

The first figure is about the direction of each axis: ![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/MMA7660_Direction.jpg)

The second figure gives some examples:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Sensing_Direction_1.jpg)

## Resources

* [Datasheet of MMA7660FC](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/res/MMA7660FC.pdf)
* [Grove - 3-Axis Digital Accelerometer Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/res/Grove-3-Axis_Digital_Accelerometer-1.5g-Eagle_File.zip)
* [github repository for 3-Axis Digital Accelerometer\(±1.5g\)](https://github.com/Seeed-Studio/Accelerometer_MMA7660)


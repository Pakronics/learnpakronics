---
oldwikiname: Grove_-_Water_Sensor
bzprodimageurl: http://statics3.seeedstudio.com/images/101020018 1.jpg
prodimagename: Grove-Water_Sensor.jpg
surveyurl: https://www.research.net/r/Grove-Water_Sensor
bzurl: https://seeedstudio.com/Grove-Water-Sensor-p-748.html
title: Grove - Water Sensor
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
sku: 101020018
category: Sensor
---

# Grove Water Sensor

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Sensor/master/img/Grove-Water\_Sensor.jpg)

The Water Sensor module is part of the Grove system. It indicates whether the sensor is dry, damp or completely immersed in water by measuring conductivity. The sensor traces have a weak pull-up resistor of 1 MΩ. The resistor will pull the sensor trace value high until a drop of water shorts the sensor trace to the grounded trace. Believe it or not this circuit will work with the digital I/O pins of your Arduino or you can use it with the analog pins to detect the amount of water induced contact between the grounded and sensor traces.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get\_One\_Now\_Banner.png)](https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html)

### Features

* Grove compatible interface
* Low power consumption
* 2.0cm x 2.0cm Grove module
* High sensitivity

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

### Applications Ideas

* Rainfall detecting
* Liquid leakage
* Tank overflow detector

Caution This device is for educational and hobby applications only. It is not intended to be used in applications where its malfunction could result in damage to property or human safety.

### Specifications

|  Item                                    |  Min  |  Typical |  Max  |  Unit |
| ---------------------------------------- | ----- | -------- | ----- | ----- |
|  Working Voltage                         |  4.75 |  5.0     |  5.25 |  V    |
|  Current                                 |  <20  |  mA      |       |       |
|  Working Temperature                     |  10   |  -       |  30   |  ℃    |
|  Working Humidity (without condensation) |  10   |  -       |  90   |  %    |

### Platforms Supported

### Getting Started

#### With [Arduino](https://app.gitbook.com/Arduino)

Connect the module to the Basic board using any of the digital pin. You can gain the value of the signal pin. When there is water on the bare conducting wires, the value is LOW. Otherwise, it will be HIGH.

The following sketch demonstrates a simple application of using the Water sensor to control the buzzer. As the picture on the below indicates, the Water sensor is connected to digital port 8 of the **Grove - Base Shield** and the Buzzer is connected to digital port 12. When there is water on the bare conducting wires, the SIG pin output a LOW voltage. Then the Buzzer sounds. The hardware installation is as follows:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Sensor/master/img/Water\_Buzzer.jpg)

* Then connect Arduino to PC by using a USB cable.
* Copy and paste code below to a new Arduino sketch.

```c
/*macro definition of water sensor and the buzzer*/
#define WATER_SENSOR 8
#define BUZZER 12

void setup()
{
    pins_init();
}
void loop()
{
    if(isExposedToWater())
    soundAlarm();
}

void pins_init()
{
    pinMode(WATER_SENSOR, INPUT);
    pinMode(BUZZER, OUTPUT);
}

/************************************************************************/
/*Function: When the sensor is exposed to the water, the buzzer sounds  */
/*          for 2 seconds.                                              */
/************************************************************************/
void soundAlarm()
{
    for(uint8_t i = 0;i < 20;i ++)
    {
        digitalWrite(BUZZER, HIGH);
        delay(50);
        digitalWrite(BUZZER, LOW);
        delay(50);
    }
}

/************************************************************************/
/*Function: Determine whether the sensor is exposed to the water        */
/*Parameter:-void                                                       */
/*Return:   -boolean,if it is exposed to the water,it will return true. */
/************************************************************************/
boolean isExposedToWater()
{
    if(digitalRead(WATER_SENSOR) == LOW)
    return true;
    else return false;
}
```

* Upload the code.
* The buzzer sounds when the sensor is damp or completely immersed in water. Have a try!

#### With Raspberry Pi

1.You should have a raspberry pi and a grovepi or grovepi+.

2.You should have completed configuring the development enviroment, otherwise follow [here](https://app.gitbook.com/GrovePiPlus).

3.Connection

* Plug the sensor to grovepi socket D2 by using a grove cable.

4.Navigate to the demos' directory:

```
cd yourpath/GrovePi/Software/Python/
```

*   To see the code

    ```
    nano grove_water_sensor.py   # "Ctrl+x" to exit #
    ```

    \`\`\`

    import time

    import grovepi

## Connect the Grove Water Sensor to digital port D2

## SIG,NC,VCC,GND

water\_sensor = 2

grovepi.pinMode(water\_sensor,"INPUT")

while True: try: print grovepi.digitalRead(water\_sensor) time.sleep(.5)

```
except IOError:
    print "Error"
```

```
5.Run the demo.
```

sudo python grove\_water\_sensor.py

\`\`\`

### Resources

* [Water Sensor Eagle Files](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Sensor/master/res/Water\_sensor.zip)
* [Demo code for Water Sensor](https://github.com/Seeed-Studio/Grove\_Water\_Sensor)

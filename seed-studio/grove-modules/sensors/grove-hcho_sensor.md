---
oldwikiname: Grove_-_HCHO_Sensor
bzprodimageurl: 'http://statics3.seeedstudio.com/images/product/grove HCHO.jpg'
prodimagename: HCHO_Sensor_01.jpg
surveyurl: 'https://www.research.net/r/Grove-HCHO_Sensor'
bzurl: 'https://seeedstudio.com/Grove-HCHO-Sensor-p-1593.html'
title: Grove - HCHO Sensor
tags: 'grove_analog, io_5v, plat_duino, plat_linkit'
sku: 101020001
category: Sensor
---

# Grove HCHO Sensor

![](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/img/HCHO_Sensor_01.jpg)

The Grove - HCHO Sensor is a semiconductor VOC gas sensor. Its design is based on WSP2110 whose conductivity changes with the concentration of VOC gas in air. Through the circuit, the conductivity can be converted to output signal that corresponding to the gas concentration. This sensor can detect the gas whose concentration is up to 1ppm. It’s suitable for detecting formaldehyde, benzene, toluene and other volatile components. This product can be used to detect harmful gas in the home environment. Therefore, it’s a good assistant for you to improve indoor environment quality of life.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/depot/grove-hcho-sensor-p-1593.html)

Warning The sensor value only reflects the approximated trend of gas concentration in a permissible error range, it DOES NOT represent the exact gas concentration. The detection of certain components in the air usually requires a more precise and costly instrument, which cannot be done with a single gas sensor. If your project is aimed at obtaining the gas concentration at a very precise level, then we do not recommend this gas sensor.

## Specifications

* Operating Voltage: 5.0V ± 0.3V
* Target Gases: HCHO, Benzene,Toluene,Alcohol
* Concentration Range: 1~50 ppm
* Sensor Resistance Value\(Rs\): 10KΩ-100KΩ\(in 10ppm HCHO\)
* Sensitivity: Rs\(in air\)/Rs\(10ppm HCHO\)≥5

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove_System/)

## Platforms Supported

## Getting Started

The Grove - HCHO Sensor can be used to detect VOCs, such as HCHO,toluene, benzene, alcohol. Here we take HCHO for an example to demonstrate how to use this sensor.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/img/HCHO_Hardware_Connection.jpg)

```text
// demo of Grove - HCHO Sensor

#define Vc 4.95

void setup()
{
    Serial.begin(9600);
}

void loop()
{
    int sensorValue=analogRead(A0);
    float R0=(1023.0/sensorValue)-1;
    Serial.print("R0 = ");
    Serial.println(R0);
    delay(500);
}
```

After uploading the code, open the serial monitor to get the R0 under normal condition\(outdoor is the best\).

Adjust the resistance of R1\(the blue potentiometer\) with a small screwer to make the number of R0 in the range of 10-100 and record that number\(my R0 number here is 34.28\).

![](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/img/R0.png)

Type your number of R0 in `#define R0 ***`, then uploading the code. Remember not to screw R1 anymore, unless you decide to detect R0 again.

```text
// demo of Grove - HCHO Sensor
#include <math.h>
#define Vc 4.95
//the number of R0 you detected just now
#define R0 34.28

void setup()
{
    Serial.begin(9600);
}

void loop()
{
    int sensorValue=analogRead(A0);
    double Rs=(1023.0/sensorValue)-1;
    Serial.print("Rs = ");
    Serial.println(Rs);
    double ppm=pow(10.0,((log10(Rs/R0)-0.0827)/(-0.4807)));
    Serial.print("HCHO ppm = ");
    Serial.println(ppm);
    delay(1000);
}
```

Then move the sensor into the office, and read the HCHO ppm value:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/img/Rs.png)

From the Typical Sensitivity Curve we could know that the detection range is 1-50ppm.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/img/Sensitivity_Characteristic.jpg)

To detect other VOC gas, you could calculate Rs/R0, then refer to the sensitivity characteristic diagram and find the gas concentration. Or use the following python script to fit the typical sensitivity curve and calculate the value of a and b:

`ppm = 10 ^ ((log10(Rs/R0) + a) / b)`

```text
# coding=utf-8
# calculate a and b of HCHO
import numpy as np
import matplotlib.pyplot as plt

#get the measure data from the Typical Sensitivity Curve
x = np.array([1, 5, 10, 20, 40])
y = np.array([1.21, 0.56, 0.4, 0.3, 0.21])

plt.subplot(221)
plt.loglog(x,y,lw=2)
#plt.ylim(0,1.5)  
plt.xlabel('log(x)')  
plt.ylabel('log(y)')  
plt.show()
```

## Resources

* [Grove - HCHO Sensor Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/res/Grove-HCHO_Sensor_Eagle_File.zip)
* [Grove - HCHO Sensor Schematic in PDF](https://github.com/SeeedDocument/Grove-HCHO_Sensor/raw/master/res/Grove%20-%20HCHO%20Sensor.pdf)
* [WSP2110 Datasheet \(Chinese\)](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/res/WSP2110.pdf)
* [WSP2110 Datasheet \(English\)](https://raw.githubusercontent.com/SeeedDocument/Grove-HCHO_Sensor/master/res/Wsp2110-1-.pdf)


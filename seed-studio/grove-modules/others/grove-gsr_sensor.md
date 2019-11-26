---
oldwikiname: Grove_-_GSR_Sensor
bzprodimageurl: 'http://statics3.seeedstudio.com/images/101020052 1.jpg'
prodimagename: GSR.jpg
surveyurl: 'https://www.research.net/r/Grove-GSR_Sensor'
bzurl: 'https://seeedstudio.com/Grove-GSR-sensor-p-1614.html'
title: Grove - GSR Sensor
tags: 'grove_analog, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg'
sku: 101020052
category: Sensor
---

# Grove GSR Sensor

![](https://raw.githubusercontent.com/SeeedDocument/Grove-GSR_Sensor/master/img/GSR.jpg)

GSR stands for galvanic skin response, is a method of measuring the electrical conductance of the skin. Strong emotion can cause stimulus to your sympathetic nervous system, resulting more sweat being secreted by the sweat glands. Grove - GSR allows you to spot such strong emotions by simple attaching two electrodes to two fingers on one hand. It is an interesting to create emotion related projects like sleep quality monitor.

!!!Warning Grove-GSR Sensor measures the resistance of the people, NOT Conductivity!

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-GSR-sensor-p-1614.html)

## Version

| Product Version | Changes | Released Date |
| :--- | :--- | :--- |
| Grove - GSR\_Sensor V1.0 | Initial | June 19, 2013 |
| Grove - GSR\_Sensor V1.2 | Add C3 100nf between M324PW-TSSOP14 and GND | July 31, 2014 |

## Specification

| Parameter | Value/Range |
| :--- | :--- |
| Operating voltage | 3.3V/5V |
| Sensitivity | Adjustable via a potentiometer |
| Input Signal | Resistance, NOT Conductivity |
| Output Signal | Voltage, analog reading |
| Finger contact material | Nickel |

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove_System/)

## Platforms Supported

## Getting Started

### Hardware

* Step 1. We need to prepare the below stuffs:

| Seeeduino V4.2 | Base Shield | Grove - GSR |
| :--- | :--- | :--- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/img/Grove-GSR_s.jpg) |
| [Get ONE Now](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html) | [Get ONE Now](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html) | [Get ONE Now](https://www.seeedstudio.com/Grove-GSR-sensor-p-1614.html) |

* Step 2. Connect the Grove-GSR to **A0** on Base Shield.
* Step 3. Plug the base Shield into Seeeduino-V4.2.
* Step 4. Connect Seeeduino-V4.2 to PC by using a USB cable.

![](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/img/Hardware_connection.jpg)

!!!Note If we don't have a Base Shield, don't worry, the sensor can be connected to your Arduino directly. Please follow below tables to connect with Arduino.

| Seeeduino | Grove-GSR Sensor |
| :--- | :--- |
| GND | Black |
| 5V | Red |
| NC | White |
| A0 | Yellow |

### Software

* Step 1. Copy the code into Arduino IDE and upload.

```text
const int GSR=A0;
int sensorValue=0;
int gsr_average=0;

void setup(){
  Serial.begin(9600);
}

void loop(){
  long sum=0;
  for(int i=0;i<10;i++)           //Average the 10 measurements to remove the glitch
      {
      sensorValue=analogRead(GSR);
      sum += sensorValue;
      delay(5);
      }
   gsr_average = sum/10;
   Serial.println(gsr_average);
}
```

* Step 2. Do not Wear the GSR sensor.
* Step 3. Click the Tools-&gt; Serial Plotter from Arduino IDE
* Step 4. Use the screw driver to adjust resistor until the serial output as 512.
* Step 5. Wear the GSR sensor.
* Step 6. We will see the below graph. Please deep breath and see the trends.  

![](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/img/Grove-GSR_Result.png)

**Human Resistance** = \(\(1024+2_Serial\_Port\_Reading\)_10000\)/\(512-Serial\_Port\_Reading\), unit is ohm, Serial\_Port\_Reading is the value display on Serial Port\(between 0~1023\)

## FAQ

Please click [here](http://support.seeedstudio.com/knowledgebase/articles/1827199-grove-gsr-sensor-sku-101020052) to see all Grove - GSR sensor FAQs.

## Tech Support

Please do not hesitate to contact **techsupport@seeed.cc** if you require further information.

## Resources

* **\[PDF\]** [Download Wiki PDF](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/res/Grove-GSR_Sensor_WiKi.pdf)
* **\[PDF\]** [Grove-GSR v1.0 Sch](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/res/Grove%20-%20GSR%20v1.0%20SCH.pdf)
* **\[PDF\]** [Grove-GSR v1.0 PCB](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/res/Grove%20-%20GSR%20v1.0%20PCB.pdf)
* **\[PDF\]** [Grove-GSR v1.2 Sch](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/res/Grove%20-%20GSR_v1.2_SCH.pdf)
* **\[PDF\]** [Grove-GSR v1.2 PCB](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/res/Grove%20-%20GSR_v1.2_PCB.pdf)
* **\[Eagle\]** [Grove - GSR v1.0 Eagle File](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/res/Grove-GSR_Eagle_File_V1.0.zip)
* **\[Eagle\]** [Grove - GSR v1.2 Eagle File](https://github.com/SeeedDocument/Grove-GSR_Sensor/raw/master/res/Grove-GSR_Eagle_File_V1.2.zip)
* **\[Datasheet\]** [LM324 datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-GSR_Sensor/master/res/Lm324.pdf)


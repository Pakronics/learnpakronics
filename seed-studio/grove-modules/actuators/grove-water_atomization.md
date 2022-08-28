---
oldwikiname: Grove_-_Water_Atomization
bzprodimageurl: http://statics3.seeedstudio.com/images/product/101020090 4.jpg
prodimagename: Water_Atomization_product_1200.jpg
surveyurl: https://www.research.net/r/Grove-Water_Atomization
bzurl: https://seeedstudio.com/Grove-Water-Atomization-v1.0-p-2542.html
title: Grove - Water Atomization
tags: grove_digital, io_5v, plat_duino
sku: 101020090
category: Actuator
---

# Grove Water Atomization

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Atomization/master/img/Water\_Atomization\_product\_1200.jpg)

Grove - Water Atomization is a fine Grove module for you to develop an atomizer or an atomizer module in your applications easily. With a few simple steps, you can prototype an atomizer. It has grove interface which make it easily applied to plenty of applications. A humidifier is a basic application it can be built with, you can develop more advanced and interesting objects with digital scent technology and any other situation in which atomization is required.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get\_One\_Now\_Banner.png)](http://www.seeedstudio.com/depot/Grove-Water-Atomization-v10-p-2542.html)

## Features

* Heated with ultrasound.
* Easy to prototype a new application.
* Well applied to vast applications.
* For various interesting, smart and fashionable applications.

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

## Application ideas

* Humidifier.
* Scent emitter in different situations.
* For smart-house applications.
* For smart objects on consumer electronic products.

## Specifications

| Parameter            | Value          |
| -------------------- | -------------- |
| Operating Voltage    | 5.0V(DC)       |
| Ripple(at Max power) | ≤100 mV        |
| Max power            | 2W             |
| Peak output voltage  | 65±5V          |
| Operating frequency  | 105±5kHz       |
| Chips                | ETA1617, NE555 |

## Platforms Supported

## Hardware Overview

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Atomization/master/img/Water\_Atomization\_hardware\_overview\_1200.jpg)

**Grove interface**\
Connect main control board such as Seeeduino board with driver board.

**Transducer interface**\
Connect ultrasonic transducer to with driver board.

**Grove wire**\
Connect main control board with driver board.

### **Parts list**

| Parts name                  | Quantity |
| --------------------------- | -------- |
| Driver board                | 1PC      |
| Grove wire                  | 1PC      |
| Ultrasonic transducer plate | 1PC      |

## Get started

### **Material required**

Seeeduino v4.2 x 1

Grove - Base shield v2 x 1

Grove - Wire x 1

### **Preparations**

Refer to following guides to build an appropriate IDE:

Note We have chosen Seeeduino in this case.

[Getting Started on Windows](https://app.gitbook.com/Seeeduino\_v4.2#Getting\_Started\_on\_Windows)

[Getting Started on Mac OS X](https://app.gitbook.com/Seeeduino\_v4.2#Getting\_Started\_on\_Mac\_OS\_X)

### **Hardware connections**

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Atomization/master/img/Water\_Atomization\_hardware\_connection.jpg)

### **A little demo**

Note We also need a Grove - Touch Sensor in this demo and also connect it to A5(Use as digital pin).

1.Copy code below to Arduino IDE editor.

```
/*
  Demo code for grove  atomization.
  Touch to start atomizing.
  Last modified by he
  by xiaohe
*/

// the setup function runs once when you press reset or power the board
void setup() {
    // initialize digital pin 13 as an output.
    pinMode(A5, OUTPUT);// Set A5 as OUTPUT
    pinMode(5, INPUT); // Use digital pin 5 as output port
}

// the loop function runs over and over again forever
void loop() {
    int D2Sig = digitalRead(5);// read pin 5 signal
    if (D2Sig == 1)
    {
        /* code */
        digitalWrite(A5, HIGH);   // atomize
        delay(10000);              // wait for 10 seconds
        digitalWrite(A5, LOW);    // atomization stopped

    }
}
```

2.Place some tissue into a trimmed paper cup filled with water, put ultrasonic transducer onto tissue.

Note The bottom side is the side with hollow which is supposed to face downside. Let bottom of transducer plate sink into the water and keep top side above water. The function of tissue is lead water to the transducer and keep upper side of transducer above water.

3.Upload code to main control board.

4.Now if you touch Grove touch sensor, you can see vapor produced.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Atomization/master/img/Water\_Atomization\_hardware\_connection.jpg)

Caution Do not touch transducer interface pins directly because peak output voltage of Drier board can be 65V.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Atomization/master/img/High\_voltage\_warning\_600.jpg)

Caution The inductor L2 (marked in red rectangle above) will be heated. So do not touch it directly.

## Resources

* [Schematic files in Eagle](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Atomization/master/res/Schematic\_file\_in\_Eagle.zip)
* [Schematic files in PDF](https://raw.githubusercontent.com/SeeedDocument/Grove-Water\_Atomization/master/res/Schematic\_file\_in\_PDF.zip)

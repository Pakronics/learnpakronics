---
oldwikiname: Grove_-_Recorder_v2.0
bzprodimageurl: https://statics3.seeedstudio.com/product/Grove Recorder_01.jpg
prodimagename: Grove-Recorder_V2.0.jpg
surveyurl: https://www.research.net/r/Grove-Recorder_v2_0
bzurl: https://www.seeedstudio.com/Grove-Recorder-p-1825.html
title: Grove - Recorder v2.0
tags: grove_digital, io_3v3, io_5v, plat_duino
sku: 103020018
category: Others
---

# Grove Recorder v2.0

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Recorder\_v2.0/master/img/Grove-Recorder\_V2.0.jpg)

Grove - CRecorder v2.0 is a upgraded recorder with enriched features. It can record 8-20 seconds\[1] audio with high-quality and natural voice. In addition, it also gets sound volume control and playback functions. With MCU such as [Seeeduino](https://app.gitbook.com/Seeeduino\_v4.2) or Arduino board, you can prototype various applications quickly with user-friendly interfaces.

\[1] Recording time could be customized(if you require) by replacing different resistor the solution to do this will be described in later sections.

## Version Tracker

| Product revision | Release date | Support status     | Notes                                                                                                                            |
| ---------------- | ------------ | ------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| V1.0             | Apr 2014     | Supported          | -                                                                                                                                |
| V2.0             | Oct 2015     | Mainstream support | <p>Add speaker volume controller.</p><p>Add NS8002 amplifier to enhance power.</p><p> Add Rec pin Switch for switch Rec pin.</p> |

## Features

* Easy-to-use with sound volume control, record, playback functions and grove interfaces.
* Easy to be programmed for plenty of applications with MCU.
* Automatic power down mode, variable recording and playback duration, non-volatile storage.
* Low power consumption.
* Shipped with a speaker (8Ω/2W).

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

## Application ideas

* Toys.
* Alarm.
* Short-duration-echo required applications.

## Specifications

| Parameter                   | Value                                                                                                                                                           |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Operating voltage           | 3.3\~5.0V(DC)                                                                                                                                                   |
| Ripple(at Max power)        | ≤ 50mV                                                                                                                                                          |
| Recording duration(default) | 12 seconds(MAX value)\[2].                                                                                                                                      |
| Playback duration(default)  | 12 seconds(MAX value).                                                                                                                                          |
| Sample rate                 | 53 kHz                                                                                                                                                          |
| Chip                        | ISD1820PY([Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Recorder\_v2.0/master/res/ISD\_1800\_Specifications.pdf)), NS8002(Volume Amplifier) |

## Platforms Supported

\[2]You can replace the resistor shows as following to change recording duration.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Recorder\_v2.0/master/img/Grove-Recorder\_V2.0\_back\_view\_600.jpg)

_Red rectangle marked area_

Note Playback duration will be same with Recording duration as it changes. Different kinds of resistor will lead different Recording duration as the following table shows.

| ROSC             | Duration | Sampling Frequency | Input Bandwidth |
| ---------------- | -------- | ------------------ | --------------- |
| 80 KΩ            | 8 secs   | 8.0 KHz            | 3.4 KHz         |
| 100 KΩ (default) | 10 secs  | 6.4 KHz            | 2.6 KHz         |
| 120 KΩ           | 12 secs  | 5.3 KHz            | 2.3 KHz         |
| 160 KΩ           | 16 secs  | 4.0 KHz            | 1.7 KHz         |
| 200 KΩ           | 20 secs  | 3.2 KHz            | 1.3 KHz         |

## Hardware Overview

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Recorder\_v2.0/master/img/Grove-Recorder\_Hardware\_View\_wiki\_s.jpg)

**Grove interface**

Connect main control board such as [Seeeduino](https://app.gitbook.com/Seeeduino\_v4.2) board with Grove - Recorder.

**Speaker interface**

Connect Grove - Recorder with speaker.

**Rec shaft**

Start recording.

**Volume control interface**

Control volume for speaker.

**MIC**

Microphone for recording.

**IDS 1820PY**

Microcontroller.

**Running indicator**

Light on while you are recording. Light out as you stop recording or recording time exceeds record duration.

**Rec pin Switch**

You can switch Rec pin ON/OFF, so you can disable or enable MCU controlled recording.

**Grove wire**

Connect main control board with driver board.

**Speaker**

### **Parts list**

| Parts name            | Quantity |
| --------------------- | -------- |
| Grove - Recorder v2.0 | 1 PC     |
| Grove wire            | 1 PC     |
| Speaker               | 1 PC     |

## Get started

### **Materials required**

* [Seeeduino](https://app.gitbook.com/Seeeduino\_v4.2) x 1
* [Grove - Button](https://app.gitbook.com/Grove-Button) x 1
* Grove wire x 1

### **Preparations**

Refer to the following guides to build a appropriate IDE:

Note We have used Seeeduino in this case.

[Getting Started on Windows](https://app.gitbook.com/Seeeduino\_v4.2#Getting\_Started\_on\_Windows)

[Getting Started on Mac OS X](https://app.gitbook.com/Seeeduino\_v4.2#Getting\_Started\_on\_Mac\_OS\_X)

### **Hardware connections**

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Recorder\_v2.0/master/img/Grove-Recorder\_Hardware\_connection\_s.jpg)

* Connect all modules as above figure shows.
  * Grove - Button > **D2**
  * Grove - Recorder > **D7**

### **Software Work**

Test code as below, copy to your Arduino IDE, then click Upload(CTRL+U) to upload code to your Arduino.

```
// demo for Grove - Recorder

const int pinButton = 2;
const int pinRec    = 7;


void setup()
{
    pinMode(pinButton, INPUT);
    pinMode(pinRec, OUTPUT);
}

void loop()
{
    if(digitalRead(pinButton))      // button pressed
    {
        digitalWrite(pinRec, HIGH);
        delay(200);
        digitalWrite(pinRec, LOW);
        while(digitalRead(pinButton));  // until button release
    }

    delay(10);
}
```

### Test it

* After connection works and software works finished, press shaft Rec to start recording.
* Then press button on Grove - Button to playback.
* You can also adjust volume with Philip screw driver.

## Resources

* Schematic file in [Eagle](https://raw.githubusercontent.com/SeeedDocument/Grove-Recorder\_v2.0/master/res/Grove-Recorder\_v2.0\_Schematic\_Eagle\_file.zip) format
* Schematic file in [PDF](https://raw.githubusercontent.com/SeeedDocument/Grove-Recorder\_v2.0/master/res/Grove-Recorder\_v2.0\_Schematic\_PDF\_file.zip) format

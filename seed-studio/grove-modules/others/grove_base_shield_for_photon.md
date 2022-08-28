---
title: Grove Base Shield for Photon
category: Others
bzurl: >-
  https://www.seeedstudio.com/Particle-Photon-Base-Shield-p-2598.html?cPath=98_106_57
oldwikiname: Grove Base Shield for Photon
prodimagename: Grove_Base_Shield_for_Photon_product_view_1200_s.jpg
surveyurl: https://www.research.net/r/Grove_Base_Shield_for_Photon
sku: 103020031
---

# Grove Base Shield for Photon

![](https://github.com/SeeedDocument/Grove\_Base\_Shield\_for\_Photon/raw/master/img/Grove\_Base\_Shield\_for\_Photon\_product\_view\_1200\_s.jpg)

**Grove Base Shield for Photon** is an expansion shield board which incorporate [Grove](https://app.gitbook.com/Grove\_System) port on which you can build more powerful and intelligent applications with much richer and cost-effective Grove functional modules. It gets three digital ports, two analog ports, two I2C ports and one UART port. It a kind of plug-and-play board which will accelerate your prototyping process dramatically.

[![](https://github.com/SeeedDocument/Seeed-WiKi/raw/master/docs/images/300px-Get\_One\_Now\_Banner-ragular.png)](https://www.seeedstudio.com/Particle-Photon-Base-Shield-p-2598.html?cPath=98\_106\_57)

## Features

* Grove interfaced
* Connect to massive and low-cost Grove modules
* I2C, UART ports integrated

## Application ideas

* Compact IoT applications such as smart router.

## Specification

|  Grove ports |  3 digital ports 2 analog ports 2 I2C ports 1 UART port. |
| ------------ | -------------------------------------------------------- |
|  Dimensions  |  53 × 53 mm                                              |
|  Weight      |  18g                                                     |

## Hardware Overview

![](https://github.com/SeeedDocument/Grove\_Base\_Shield\_for\_Photon/raw/master/img/Grove\_Base\_Shield\_for\_Photon\_component\_diagram\_annotated\_1200\_s.jpg)

### **Parts list**

| Parts name                    |  Quantity |
| ----------------------------- | --------- |
|  Grove Base Shield for Photon |  1PC      |

## Getting Started

**Note:** In this case we show you a general development environmental.

### Material required

* [Particle Photon](http://www.seeedstudio.com/depot/Particle-Photon-p-2527.html) × 1
* USB cable (type A to micro type-B) × 1
* A PC or Mac
* Grove Base Shield for Photon × 1
* [Grove - Buzzer](http://www.seeedstudio.com/depot/Grove-Buzzer-p-768.html?cPath=38) × 1

### Buzzing

&#x20;1\. Refer to \[here]\(https://docs.particle.io/guide/getting-started/connect/core/) to connect to a device (PC or Mac).

!!!Note 1. We recommend that you choose **node.js v4.2.3 LTS** especially for Windows 10 user. 2. You may need to one more steps after run command **particle setup**, that is, connect you device (PC or Mac) to a wi-fi AP whose name contain **Photon**, especially on Windows 10.

&#x20;2\. Use \[Web IDE]\(https://build.particle.io/) for your project. Login with your account and choose your device (click the 2nd last icon on left column).

!!!Note We recommend you choose [Web IDE](https://build.particle.io/) to compile or flashing your code to Photon which is much quicker than using Particle Dev, if your internet connectivity is not so good.

&#x20;3\. Connect them like following:

![](https://github.com/SeeedDocument/Grove\_Base\_Shield\_for\_Photon/raw/master/img/Grove\_Base\_Shield\_for\_Photon\_demo\_conneciton\_1200\_S.jpg)

&#x20;4\. Now you can copy following code to Web IDE and flash them to Photo by clicking a lighting-like icon (the 1st icon on left column).

!!!Note Copy the code only to the tab named _**filename.ino**_.

```
/*
   Buzzing
   Use digital pin D4
   This example code is in the public domain.
   by xiaohe
  */
int led1 = D4; //set D4 as output

void setup() {
    pinMode(led1, OUTPUT);
}

void loop() {
    // enable buzzing
    digitalWrite(led1, HIGH);

    // We'll leave it on for 1 second...
    delay(1000);

    // Then we'll turn it off...
    digitalWrite(led1, LOW);

    // Wait 1 second...
    delay(1000);

    // And it will repeat!
}
```

## Resources

* [Schematic files](https://github.com/SeeedDocument/Grove\_Base\_Shield\_for\_Photon/raw/master/res/Schematic\_files\_for\_Grove\_Base\_Shield\_for\_Photon.zip)
* [Grove\_System](https://app.gitbook.com/Grove\_System)

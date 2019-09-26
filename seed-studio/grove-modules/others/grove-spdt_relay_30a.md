---
title: Grove - SPDT Relay(30A)
category: Others
bzurl: 'https://www.seeedstudio.com/Grove-SPDT-Relay(30A)-p-1473.html'
oldwikiname: Grove - SPDT Relay(30A)
prodimagename: SPDT_Relay_01.jpg
surveyurl: 'https://www.research.net/r/Grove_SPDT_Relay_30A'
sku: 103020012
---

# Grove SPDT Relay 30A

![](https://github.com/SeeedDocument/Grove-SPDT_Relay_30A/raw/master/img/SPDT_Relay_01.jpg)

The SPDT Relay\(30A\) is a high quality Single Pole Double Throw Relay\(SPDT\).The Relay consists of a coil, 1 common terminal, 1 normally closed terminal, and one normally open terminal. When the coil of the relay is at rest \(not energized\), the common terminal and the normally closed terminal have continuity. When the coil is energized, the common terminal and the normally open terminal have continuity. This relay's coil is rated up to 5V and the contact is rated up to 30A \(@250VAC, 30VDC\).You can use it to control high current devices.

## Feature

* High Switching Current
* SPDT Relay
* Normally closed relay

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove_System/)

## Specification

| Item | Min | Typical | Max | Unit |
| :--- | :--- | :--- | :--- | :--- |
| working Voltage | 4.75 | 5.0 | 5.25 | VDC |
| Current | - | 185 | - | mA |
| Pull-In Voltage\(Max\) | - | 3.75 | - | VDC |
| Operation Time\(Max\) | - | 15 | - | ms |
| Release Time\(Max\) | - | 10 | - | ms |
| Operating Ambient Temperature | -25 | - | 70 | °C |

## Usage

**With Arduino**

Why do we want to use a relay and do we really need to? Anytime you want to switch on/off a device which draws more current or works with a high voltage, you'll need to use a relay. That is to say, the relay is "a high voltage or current switch controlled by low voltage". The coil of an SPDT relay that we most commonly use draws very little current \(the [Grove - Relay](http://wiki.seeed.cc/Grove-Relay/)supports 10A\). Now, with this 30A relay, you can control much more high-current switch devices such as headlights, parking lights, horns, etc.

The SPDT Relay internal structure:

![](https://github.com/SeeedDocument/Grove-SPDT_Relay_30A/raw/master/img/Relay_Struction.jpg)

You may see that the common terminal and the normally closed terminal have continuity When the coil of the relay is at rest.

But when the coil is energized, the common terminal and the normally open terminal will have continuity.

Hardware Installation can refer to the following picture:

![](https://github.com/SeeedDocument/Grove-SPDT_Relay_30A/raw/master/img/SPDT_Relay.jpg)

The coding to control this relay is the same as the [Grove - Relay](http://wiki.seeed.cc/Grove-Relay/)

Good luck to you for controlling your air-condition or washing machine, with Arduino and the Grove - SPDT Relay\(30A\).

**With Raspberry Pi**

1.You should have got a raspberry pi and a grovepi or grovepi+.

2.You should have completed configuring the development enviroment, otherwise follow [here](http://wiki.seeedstudio.com/wiki/GrovePi+#Introducing_the_GrovePi.2B).

3.Connection

* Plug the sensor to grovepi socket D4 by using a grove cable.

4.Navigate to the demos' directory:

```text
   cd yourpath/GrovePi/Software/Python/
```

To see the code

```text
   nano grove_spdt_relay.py   # "Ctrl+x" to exit #
```

```text
import time
import grovepi

# Connect the Grove SPDT Relay to digital port D4
# SIG,NC,VCC,GND
relay = 4

grovepi.pinMode(relay,"OUTPUT")

while True:
    try:
        # switch on for 5 seconds
        grovepi.digitalWrite(relay,1)
        print "on"
        time.sleep(5)

        # switch off for 5 seconds
        grovepi.digitalWrite(relay,0)
        print "off"
        time.sleep(5)

    except KeyboardInterrupt:
        grovepi.digitalWrite(relay,0)
        break
    except IOError:
        print "Error"
```

5.Run the demo.

```text
   sudo python grove_spdt_relay.py
```

## Resource

* \[Grove - SPDT Relay\(30A\) Eagle File\]\([https://github.com/SeeedDocument/Grove-SPDT\_Relay\_30A/raw/master/res/Grove\_-\_SPDT\_Relay\(30A\)\_Eagle\_File.zip](https://github.com/SeeedDocument/Grove-SPDT_Relay_30A/raw/master/res/Grove_-_SPDT_Relay%2830A%29_Eagle_File.zip)\)
* [SLA-05VDC-SL-C Datasheet](https://github.com/SeeedDocument/Grove-SPDT_Relay_30A/raw/master/res/SLA-05VDC-SL-C_Datasheet.pdf)


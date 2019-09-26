---
oldwikiname: Grove_-_Dry-Reed_Relay
bzprodimageurl: 'http://statics3.seeedstudio.com/images/product/DryReed Relay.jpg'
prodimagename: DryReed_Relay_01.jpg
surveyurl: 'https://www.research.net/r/Grove-Dry-Reed_Relay'
bzurl: 'https://seeedstudio.com/Grove-Dry-Reed-Relay-p-1412.html'
title: Grove - Dry-Reed Relay
tags: >-
  grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg,
  plat_wio
sku: 103020014
category: Actuator
---

# Grove Dry Reed Relay

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Dry-Reed_Relay/master/img/DryReed_Relay_01.jpg)

The **Grove-Dry Reed Relay** is a relay module which works through magnetizing the vibration reed via the current in the coils. Compared to electromagnetic relays, the contacts completely sealed is the biggest feature of the Dry-Reed Relay. Besides, it features simplicity in construct, compactness, fast speed and long life, which make it widely applied in many fields such as microelectronic detection, Automatic Control etc.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Dry-Reed-Relay-p-1412.html)

## Features

* Grove Interface
* High Speed
* Good stability
* Long contact life
* Contact fully sealed

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove_System/)

## Specifications

|  Item |  Min |  Typical |  Max |  Unit |
| :--- | :--- | :--- | :--- | :--- |
|  Voltage |  4.8 |  5.0 |  5.2 |  VDC |
|  Coil Resistance |  225 |  250 |  275 |  Ω |
|  Pick-Up Voltage |  3.75 |  VDC |  |  |
|  Switching Current\(Max\) |  0.5 |  A |  |  |
|  Switching Voltage\(Max\) |  120 VAC/60VDC |  - |  |  |
|  Carrying Current\(Max\) |  1.0 |  A |  |  |
|  Operate Time\(Max\) |  1.0 |  mS |  |  |
|  Release Time\(Max\) |  0.5 |  mS |  |  |
|  Mechanical Life\(at no load\) |  1×108 operations |  - |  |  |
|  Ambient Temperature |  -30 |  / |  70 |  ˚C |

## Platforms Supported

## Usage

### With Arduino

The Dry-Reed Relay can support up to 60VDC 1A load. You can use it to control resistance load, **but it is not applicable to inductive load\(such as Motor\)**.

The usage of this Dry-reed relay is quite alike that of common relays.

* Connect electric light to Grove - Dry-Reed Relay and power for electric light.
* Connect Grove - Dry-Reed Relay to port D2 of [Grove - Base Shield](/Base_Shield_V2) and plug it into Arduino/Seeeduino.
* Upload the below code.

```text
    int Relay = 2;

    // the setup routine runs once when you press reset:
    void setup() {                
      // initialize the digital pin as an output.
      pinMode(Relay, OUTPUT);     
    }

    // the loop routine runs over and over again forever:
    void loop() {
      digitalWrite(Relay, HIGH);   //the Relay close(HIGH is the voltage level)
      delay(5000);               // wait for five seconds
      digitalWrite(Relay, LOW);    //the Relay normally open by making the voltage LOW
      delay(5000);               // wait for five seconds
    }
```

* The electric light will light up for seconds ,then off for seconds, repeatedly.For the special applications, you may need to write the code by yourself.

### With Raspberry Pi

1.You should have got a raspberry pi and a grovepi or grovepi+.

2.You should have completed configuring the development enviroment, otherwise follow [here](/GrovePiPlus).

3.Connection

* Plug the sensor to grovepi socket D4 by using a grove cable.

4.Navigate to the demos' directory:

```text
    cd yourpath/GrovePi/Software/Python/
```

* To see the code

  ```text
  nano grove_relay.py   # "Ctrl+x" to exit #
  ```

  ```text
  import time
  import grovepi

  # Connect the Grove Relay to digital port D4
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
    sudo python grove_relay.py
```

## Resources

* [Grove - Dry-Reed Relay Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Dry-Reed_Relay/master/res/Grove-Dry-Reed_Relay_Eagle_File.zip)
* [Dry-Reed Relay Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Dry-Reed_Relay/master/res/Dry-Reed_Relay_Datasheet.pdf)


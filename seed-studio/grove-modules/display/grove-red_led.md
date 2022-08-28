---
title: Grove - Red LED
category: Display
bzurl: https://www.seeedstudio.com/Grove-Red-LED-p-1142.html
oldwikiname: Grove - Red LED
prodimagename: Grove-LED_Photo.jpg
surveyurl: https://www.research.net/r/Grove_Red_LED
sku: 104030005
---

# Grove Red LED

![](https://github.com/SeeedDocument/Grove-Red\_LED/raw/master/img/Grove-LED\_Photo.jpg)

Grove - Red LED is similar to the [Grove - LED](https://app.gitbook.com/Grove-LED) module in that it houses an LED light source. In addition, it also has a potentiometer on-board to manage the power requirements of the LED. The PCB of this module has mounting holes using which it can be mounted on the required surface for your prototype. For example, it can be easily used as a pilot lamp for indicating power or signal presence.

## Features

* Provides an LED light source for your project
* Flexibility to replace Red LED with any other LED, e.g., that of a different color since the LED is 'pinned in' into the LED holder rather than soldered on to the board
* On-board potentiometer guarantees brightness control and interoperability with a higher range of input voltages

## Usage

Follow these steps to build a sample circuit using this module:

1.Connect the LED module to the output side of your circuit (to the right of the power module). On the input side of the circuit, you may use a range of sensor based input modules ([Grove - Light Sensor](https://app.gitbook.com/Grove-Light\_Sensor), [Grove - Sound Sensor](https://app.gitbook.com/Grove-Sound\_Sensor), [Grove - Button](https://app.gitbook.com/Grove-Button) or [Grove - Slide Potentiometer](https://app.gitbook.com/Grove-Slide\_Potentiometer)).

2.Power up the circuit.

3.The LED will turn ON when the input module supplies a trigger:

* If using with a momentary switch like the one on the [Grove - Button](https://app.gitbook.com/Grove-Button) module, simply press the button to turn ON the LED:

![](https://github.com/SeeedDocument/Grove-Red\_LED/raw/master/img/Grove-momentarySwitch-RedLED.jpg)

* If using with a [Grove - Slide Potentiometer](https://app.gitbook.com/Grove-Slide\_Potentiometer), move the slider from the GND position to VCC and see how the brightness of the LED increases as the supplied voltage increases.
* If using with a [Grove - Light Sensor](https://app.gitbook.com/Grove-Light\_Sensor) connected directly to the input side of the circuit, you should see the LED turn ON in bright light and turn OFF in the dark. If you want the LED to turn ON only in the dark, add a [Grove - NOT](https://app.gitbook.com/Grove-NOT) module between the light sensor and the power module.

You can use either the [Grove - USB Power](https://app.gitbook.com/Grove-Mixer\_Pack#2.\_USB\_Power) module or the [Grove - DC Jack Power](https://app.gitbook.com/Grove-DC\_Jack\_Power) module for the Grove circuit when using in standalone mode (without MCU). When used in conjunction with an MCU board such as an [Arduino](https://app.gitbook.com/w/index.php?title=Arduino\&amp;action=edit\&amp;redlink=1) or [Seeeduino](https://app.gitbook.com/Seeeduino) and a [Grove - Base Shield](https://app.gitbook.com/Grove-Base\_Shield), the power is supplied to the circuit through the microcontroller board and there is no need to use any [Grove Power Module](https://app.gitbook.com/GROVE\_System#Power).

### With [Raspberry Pi](https://app.gitbook.com/GrovePiPlus)

Connect the LED to Port D4 and power on the Raspberry Pi, using the Grove wire connector.This is a test to make led blinking.You can connect to GrovePi+ with it as the picture below.

![](https://github.com/SeeedDocument/Grove-Red\_LED/raw/master/img/GrovePiPlus\_red\_led.jpg)

```
# GrovePi LED Blink example

import time
from grovepi import *

# Connect the Grove LED to digital port D4
led = 4

pinMode(led,"OUTPUT")
time.sleep(1)

while True:
    try:
        #Blink the LED
        digitalWrite(led,1)        # Send HIGH to switch on LED
        time.sleep(1)

        digitalWrite(led,0)        # Send LOW to switch off LED
        time.sleep(1)

    except KeyboardInterrupt:    # Turn LED off before stopping
        digitalWrite(led,0)
        break
    except IOError:                # Print "Error" if communication error encountered
        print "Error"
```

#### Run The Program

*   Find the path to the file(According to your own path)

    ```
    cd GrovePi/Software/Python/
    ```
*   Run Program

    ```
    sudo python grove_led_blink.py
    ```

## Availability

This [Grove](https://app.gitbook.com/Grove) module is available as part of the following [Grove Kit Series](https://app.gitbook.com/GROVE\_System#GROVE\_Kit\_Series):

* [Grove Mixer Pack V2](https://app.gitbook.com/GROVE\_MIXER\_PACK\_V2)

The [Grove Mixer Pack](https://app.gitbook.com/Grove-Mixer\_Pack) uses the [Grove - LED](https://app.gitbook.com/Grove-LED) module.

Alternatively, it can be bought stand-alone [here](http://www.seeedstudio.com/depot/Grove-Red-LED-p-1142.html) at the [Seeed Studio Bazaar](http://www.seeedstudio.com/depot/Grove-Red-LED-p-1142.html).

## Resources

* [Grove - Red LED Schematic](https://github.com/SeeedDocument/Grove-Red\_LED/raw/master/res/Grove-LED\_v1.3.pdf)
* Also see [Grove Mixer Pack V2 Resources](https://app.gitbook.com/GROVE\_MIXER\_PACK\_V2#Resources) section for Eagle files for this module
* [Schematic at Easyeda](https://easyeda.com/Seeed/Grove\_Red\_LED-7e3e5eacbdc94abb90c01c55c55bc83a)

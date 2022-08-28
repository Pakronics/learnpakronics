---
title: Grove Base BoosterPack
category: Others
bzurl: https://www.seeedstudio.com/Grove-Base-BoosterPack-p-2177.html
oldwikiname: Grove Base BoosterPack
prodimagename: 110020004%205.jpg
surveyurl: https://www.research.net/r/Grove_Base_BoosterPack
sku: 103020019
---

# Grove Base Booster Pack

![](https://github.com/SeeedDocument/Grove\_Base\_BoosterPack/raw/master/img/110020004%205.jpg)

BoosterPacks are plug-in modules that can stack on top of the various LaunchPad kits to add additional functionality, such as sensors, displays, wireless modules & more. The Grove Base BoosterPack is a welcome addition to the LaunchPad/BoosterPack ecosystem, enabling any LaunchPad to interface with the growing offering of Grove modules from Seeed Studio. The Grove Base BoosterPack offers a convenient and easy way for rapid prototypers to use more than one hundred Grove modules with standardized connectors, including sensors, actuators, displays, lights, motors and more.

![](https://github.com/SeeedDocument/Grove\_Base\_BoosterPack/raw/master/img/Grove\_Web\_idea.jpg)

**What is Grove？**

Grove is a modular, ready-to-use tool set that takes a building block approach to assembling electronics. The Grove system consists of a base shield and a large selection of modules that feature standardized connectors. The base shield allows for easy connection of any microcontroller to interface with the various Grove modules. Each Grove module addresses a unique function & the overall collection of modules expand a wide range of functionality - from a simple push-button to a complex heart rate sensor. Each one comes with clear documentation and demo code to help you get started quickly.

![](https://github.com/SeeedDocument/Grove\_Base\_BoosterPack/raw/master/img/IMG\_GROVE.JPG)

**What is LaunchPad？**

The LaunchPad is a set of Evaluation Kits from Texas Instruments. To introduce new functionality to the LaunchPad evaluation kits, we present the BoosterPack which acts as a plug-in board that fit on top of the LaunchPad baseboards. It offers a convenient and easy way for you to use more than one hundred Grove modules with standardized connectors, including sensors, actuators, displays, lights, motors and so on.

## Features

* Seeedstudio presents the newly launched Grove Base BoosterPack allowing Texas Instruments Launchpad to be connected closed with our Groves Family,further enabling rapid prototype and combinations with a range of Sensors, actuators,displays,lights,motors and etc.
* The Grove Base BoosterPack has thirteen Groves 4-pin standard interfaces ,including five analog, five digital and three serial port, acting as a plug-n-play expansion module on Launchpad based on MSP430 launchpad.It also provides various of tutorials on how to connect with TI MSP430, there are 11 different kinds of projects for reference prototype ,which offers a convenient way to guide your creativity.
* There is a RED LED on the Grove BoosterPack. It will indicate the power supply.

![](https://github.com/SeeedDocument/Grove\_Base\_BoosterPack/raw/master/img/BoosterpackpinMapping.jpg)

## Using the Grove Base BoosterPack

### Using a 40-pin LaunchPad

i.e. MSP-EXP430F5529LP, EK-TM4C123GXL, etc

The BoosterPack was designed in a way to leverage pins in the “inner 20 pins” \[21-40]. The pins are connected as shown below in the table:

Using the table below, developers should be able to read an analog value from a Grove module (i.e. potentiometer/turn knob) that is connected to Grove connector ‘J6’ by using the analogRead(24) API call with Energia.

|  Connector Type |  Grove connector Label |  GND |  VCC  |  SIG1 (connection to the BoosterPack pin) |  SIG0 (connection to the BoosterPack pin) \* |
| --------------- | ---------------------- | ---- | ----- | ----------------------------------------- | -------------------------------------------- |
|  Analog         |  J5                    |  GND |  3.3V |  23 (analog capable pin)                  |  22 (analog capable pin)                     |
|  Analog         |  J6                    |  GND |  3.3V |  25 (analog capable pin)                  |  24 (analog capable pin)                     |
|  Analog         |  J7                    |  GND |  3.3V |  26 (analog capable pin)                  |  25 (analog capable pin)                     |
|  Analog         |  J8                    |  GND |  3.3V |  27 (analog capable pin)                  |  26 (analog capable pin)                     |
|  Analog         |  J9                    |  GND |  3.3V |  28 (analog capable pin)                  |  27 (analog capable pin)                     |
|  I2C            |  J10                   |  GND |  3.3V |  10 (I2C SDA)                             |  9 (I2C SCL)                                 |
|  UART           |  J11                   |  GND |  3.3V |  4 (UART to MCU)                          |  3 (UART from MCU)                           |
|  SPI            |  J12                   |  GND |  3.3V |  14 (SPI MISO)                            |  7 (SPI CLK)                                 |
|  Digital        |  J13                   |  GND |  3.3V |  39 (Digital/PWM pin)                     |  40 (Digital/PWM pin)                        |
|  Digital        |  J14                   |  GND |  3.3V |  38 (Digital/PWM pin)                     |  39 (Digital/PWM pin)                        |
|  Digital        |  J15                   |  GND |  3.3V |  37 (Digital/PWM pin)                     |  38 (Digital/PWM pin)                        |
|  Digital        |  J16                   |  GND |  3.3V |  36 (Digital/PWM pin)                     |  37 (Digital/PWM pin)                        |
|  Digital        |  J17                   |  GND |  3.3V |  35 (Digital/PWM pin)                     |  36 (Digital/PWM pin)                        |

### Using a 20-pin LaunchPad

If you are using a 20-pin LaunchPad, you can use jumpers or jumper wire to make the appropriate connections between a Grove connector & the BoosterPack connector.

Using your specific LaunchPad’s pin out diagram, you can physically/electrically connect the Grove module to the appropriate pin. Pinout diagrams for each LaunchPad are available here: [http://energia.nu/pin-maps/](http://energia.nu/pin-maps/)

With the help of these pin diagrams, you know which pin has the function you need. If you want to use Grove connector J5 for an analog Grove module (i.e. potentiometer knob), you can use the Energia pin maps to identify an analog-capable pin of the BoosterPack connector. Using a jumper of wire, you can connect pin number 22 with the analog-capable pin that is available. For example, if you are using an MSP-EXP430G2 LaunchPad, you can use a jumper or a cable to connect pin 22 with pin 2.

## Supported Products

### Grove List

* [1. Buzzer](https://app.gitbook.com/Grove-Buzzer#With\_TI\_LaunchPad)
* [2. Relay](https://app.gitbook.com/Grove-Relay#With\_TI\_LaunchPad)
* [3. 4-Digital Display ](https://app.gitbook.com/Grove-4-Digit\_Display#With\_TI\_LaunchPad)
* [4. Rotary Angle Sensor ](https://app.gitbook.com/Grove-Rotary\_Angle\_Sensor#With\_TI\_LaunchPad)
* [5. Light Sensor](https://app.gitbook.com/Grove-Light\_Sensor#With\_TI\_LaunchPad)
* [6. Sound Sensor ](https://app.gitbook.com/Grove-Sound\_Sensor#With\_TI\_LaunchPad)
* [7. PIR Motion Sensor ](https://app.gitbook.com/Grove-PIR\_Motion\_Sensor#With\_TI\_LaunchPad)
* [8. Moisture Sensor](https://app.gitbook.com/Grove-Moisture\_Sensor#With\_TI\_LaunchPad)
* [9. Ultrasonic Ranger Sensor](https://app.gitbook.com/Grove-Ultrasonic\_Ranger#With\_TI\_LaunchPad)
* [10. Temperature Humidity Sensor ](https://app.gitbook.com/Grove-Temperature\_and\_Humidity\_Sensor#With\_TI\_LaunchPad)

## Resources

* [Hardware eagle files](https://github.com/SeeedDocument/Grove\_Base\_BoosterPack/raw/master/res/Grove\_Base\_BoosterPack\_v1.0.zip)
* [Grove Starter Kit For LaunchPad User's Manual](https://github.com/SeeedDocument/Grove\_Base\_BoosterPack/raw/master/res/Grove%20Starter%20Kit%20Manual.pdf)

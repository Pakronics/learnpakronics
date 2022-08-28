---
title: GrovePi+
category: Raspberry Pi
bzurl: https://www.seeedstudio.com/GrovePi%2B-p-2241.html
oldwikiname: GrovePi+
prodimagename: GrovePi_Wiki_1.JPG
surveyurl: https://www.research.net/r/GrovePi_plus
sku: 103010002
---

# GrovePi Plus

![](https://github.com/SeeedDocument/GrovePi\_Plus/raw/master/img/110060049%2010\_02.jpg)

[GrovePi](http://www.dexterindustries.com/GrovePi/) is an add-on board that brings [Grove Sensors](https://app.gitbook.com/GROVE\_System) to the [Raspberry Pi](http://www.seeedstudio.com/depot/s/Raspberry%20Pi.html?search\_in\_description=0). As a new version of [GrovePi](http://www.seeedstudio.com/depot/GrovePi-p-1672.html). It adds support for the newly RaspberryPi Model B+ and Model A+. There are three mounting holes can perfect match all version of Raspberry Pi. Camera cable outlet hole. It also improves the voltage level converting sub circuits.

## Features

* 7 digital Ports
* 3 analoge Ports
* 3 I2C ports
* 1 Serial port connect to GrovePi
* 1 Serial port connect to Raspberry Pi
* Grove header Vcc output Voltage: 5Vdc

## Get Started

**Welcome to the Quickstart Guide to the GrovePi+.**

If you want to know more about how it works, you can find all the design files in the designer's [Github Repository](https://github.com/DexterInd/GrovePi).

### Connect the GrovePi to the Raspberry Pi

First, mount your GrovePi on the Raspberry Pi. The GrovePi slides over top of the Raspberry Pi as shown in the picture below.

![](https://github.com/SeeedDocument/GrovePi\_Plus/raw/master/img/GrovePiPlus\_wiki\_3.jpg)

![](https://github.com/SeeedDocument/GrovePi\_Plus/raw/master/img/GrovePi\_Wiki\_1.JPG)

Ensure that the pins are properly aligned when stacking the GrovePi.

### Setup the Software on the Raspberry Pi

Next we will install the software on the Raspberry Pi. There are two options for installation:

* You can use our BrickPi Image.
* Use your own image. If you already have your own flavor of linux running on the Raspberry Pi, you can use our bash script to setup for the GrovePi.

**Using the BrickPi Image**

* Download the Brick Pi Image and install the image on your SD card. [Here is the link to the BrickPi Page with steps to configure the SD card](http://www.dexterindustries.com/BrickPi/getting-started/pi-prep/). You will need a minimum of 4GB SD Card for this installation.
* Clone the Github repository at an appropriate location in Raspbian

```
git clone https://github.com/DexterInd/GrovePi.git
```

* Run the bash script in the Scripts folder to configure the Raspbian. [Here is the tutorial for setting up with the Script.](http://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/)
* Restart your Raspberry Pi.

**Configuring your own image**

* Clone the Github repository at an appropriate location

```
git clone https://github.com/DexterInd/GrovePi.git
```

* Run the bash script in the Scripts folder to configure the Raspbian. [here](http://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) is the tutorial for setting up with the Script.
* Restart the Raspberry Pi and start using the Grove Pi.

### Testing the GrovePi

Once you have your Raspberry Pi configured to work with the GrovePi, it’s time to see it in action.

We have developed three simple projects to illustrate how the GrovePi works.

## Supported Products

### Grove List

* [1. Grove - Button ](https://app.gitbook.com/Grove-Button#With\_Raspberry\_Pi)
* [2. Light Sensor](https://app.gitbook.com/Grove-Light\_Sensor#With\_Raspberry\_Pi)
* [3. Buzzer](https://app.gitbook.com/Grove-Buzzer#With\_Raspberry\_Pi)
* [4. Sound Sensor ](https://app.gitbook.com/Grove-Sound\_Sensor#With\_Raspberry\_Pi)
* [5. Grove - Red LED ](https://app.gitbook.com/Grove-Red\_LED#With\_Raspberry\_Pi)
* [6. Grove - Blue LED ](https://app.gitbook.com/Grove-LED#With\_Raspberry\_Pi)
* [7. Grove - Green LED ](https://app.gitbook.com/Grove-LED#With\_Raspberry\_Pi)
* [8. LCD RGB Backlight ](https://app.gitbook.com/Grove-LCD\_RGB\_Backlight#With\_Raspberry\_Pi)
* [9. Rotary Angle Sensor ](https://app.gitbook.com/Grove-Rotary\_Angle\_Sensor#With\_Raspberry\_Pi)
* [10. Temperature Humidity Sensor ](https://app.gitbook.com/Grove-Temperature\_and\_Humidity\_Sensor#With\_Raspberry\_Pi)
* [11. Ultrasonic Ranger Sensor](https://app.gitbook.com/Grove-Ultrasonic\_Ranger#With\_Raspberry\_Pi)
* [12. Relay](https://app.gitbook.com/Grove-Relay#With\_Raspberry\_Pi)

## Resources

* **\[Eagle]** [GrovePi\_Plus V3.0 eagle file](https://github.com/SeeedDocument/GrovePi\_Plus/raw/master/res/GrovePi%2BEagle%20FIle.zip)
* **\[PDF]** [GrovePi\_Plus V3.0 schematics pdf file](https://github.com/SeeedDocument/GrovePi\_Plus/raw/master/res/GrovePi%2B%20v3.0%20Sch.pdf)
* **\[PDF]** [GrovePi\_Plus V3.0 PCB pdf file](https://github.com/SeeedDocument/GrovePi\_Plus/raw/master/res/GrovePi%2B%20v3.0%20PCB.pdf)
* **\[Document]** [Setting\_Up\_Software\_for\_GrovePi](https://github.com/SeeedDocument/GrovePi\_Plus/raw/master/res/Setting\_Up\_Software\_for\_GrovePi.pdf)

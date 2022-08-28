---
title: Grove Indoor Environment Kit for Edison
category: Others
bzurl: >-
  https://www.seeedstudio.com/Grove-Indoor-Environment-Kit-for-Intel%C2%AE-Edison-p-2427.html
oldwikiname: Grove Indoor Environment Kit for Edison
prodimagename: Grove_Indoor_Environment_Kit_for_Edison_with_case.JPG
surveyurl: https://www.research.net/r/Grove_Indoor_Environment_Kit_for_Edison
sku: 110060064
---

# Grove Indoor Environment Kit for Edison

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Grove\_Indoor\_Environment\_Kit\_for\_Edison\_with\_case.JPG)

Grove Indoor Environment Kit for Edison makes it easy to create complete indoor environment applications with Intel Edison and Arduino Breakout Board. With the Base Shield V2, developer can plug up to 11 different Grove sensors & actuators quickly. We provide cool demo code which will be constantly updated, and it will be very easy to operate these sensors & actuators without any programming experience.

[![](https://github.com/SeeedDocument/Seeed-WiKi/raw/master/docs/images/300px-Get\_One\_Now\_Banner-ragular.png)](https://www.seeedstudio.com/Grove-Indoor-Environment-Kit-for-Intel%C2%AE-Edison-p-2427.html)

## What's included in the kit?

* [Base Shield V2](https://app.gitbook.com/Base\_shield\_v2) x1
* [Grove - Tempture\&Humidity Sensor (High-Accuracy \&Mini)](https://app.gitbook.com/Grove-TemptureAndHumidity\_Sensor-High-Accuracy\_AndMini-v1.0) x1
* [Grove - Moisture sensor](https://app.gitbook.com/Grove-Moisture\_sensor) x1
* [Grove - Light Sensor](https://app.gitbook.com/Grove-Light\_Sensor) x1
* [Grove - UV Sensor](https://app.gitbook.com/Grove-UV\_Sensor) x1
* [Grove - PIR Motion Sensor](https://app.gitbook.com/Grove-PIR\_Motion\_Sensor) x1
* [Grove - Encoder](https://app.gitbook.com/Grove-Encoder) x1
* [Grove - Button](https://app.gitbook.com/Grove-Button) x1
* [Grove - LCD RGB Backlight](https://app.gitbook.com/Grove-LCD\_RGB\_Backlight) x1
* [Grove - Relay](https://app.gitbook.com/Grove-Relay) x1
* [Grove - Servo](https://app.gitbook.com/Grove-Servo) x1
* [Grove - Buzzer](https://app.gitbook.com/Grove-Buzzer) x1
* [9V to Barrel Jack Adapter](http://www.seeedstudio.com/depot/9V-to-Barrel-Jack-Adapter-p-1481.html) x1
* 26AWG Grove Cable x10
* USB Cable x1

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Grove-Indoor-Environment-Kit-for-Edison.jpg)

## Installing Edison Arduino IDE

Refer to Intel Edison offical site: [Edison Getting Started Guide](https://communities.intel.com/docs/DOC-23147)

1.Download the Edison Arduino IDE.(Note: Select your OS.)

2.Navigate to the folder where you downloaded the .zip Edison Arduino IDE

3.Right click on the .7z file,highlight “7-zip”, and select “Extract to “arduino-…”

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/IndoorKit\_Extract\_7z.png)

4.Click through the folder that was created until you see the IDE “arduino.exe” file.Double-click this file and this window should open.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/IndoorKit\_ArduinoIDE.png)

## Install required drivers

1.Download [FTDI drivers](http://www.ftdichip.com/Drivers/CDM/CDM%20v2.10.00%20WHQL%20Certified.exe)

2.Right-click the .exe file you downloaded, which should be called “CDM…” and select “Run as administrator”.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Edison\_FTDI\_Driver.jpg)

3.Click “Extract”.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Edison\_FTDI\_Driver\_Install.jpg)

4.Click “Next”.

5.Click “Finish” when you see this screen.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Edison\_FTDI\_Driver\_Install\_ok.jpg)

6.Download [Intel Edison Drivers](https://communities.intel.com/docs/DOC-23242) to install the required RNDIS, CDC, and DFU drivers.

7.Double-click the .exe file to begin the install.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Intel\_Edison\_Driver.jpg)

## Hardware connection

Using 26AWG Grove Cable making the following connections:

|  Grove Modules                |  Connected to |
| ----------------------------- | ------------- |
|  Temperature\&Humidity Sensor |  I2C          |
|  Moisture Sensor              |  A1           |
|  Light Sensor                 |  A2           |
|  UV Sensor                    |  A3           |
|  PIR Motion Sensor            |  D7           |
|  Encoder                      |  D2           |
|  Button                       |  UART(D1)     |
|  LCD RGB Backlight            |  I2C          |
|  Relay                        |  D5           |
|  Servo                        |  D6           |
|  Buzzer                       |  D4           |

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Edison\_Indoor\_Wire\_Figure.png)

## Running Example

1.Open the web site: [Grove\_Indoor\_Environment\_Demo](https://github.com/Seeed-Studio/Grove\_Indoor\_Environment\_Demo) to download the whole project.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Indoor\_Kit\_Github\_Demo.png)

2.Click **Tools > Serial Port** and select the Com # that the Intel Edison is connected to

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Import\_Indoor\_Kit\_Demo.png)

3.Click Sketch>Import Library…>Add Library and import the library downloaded at **step 1**

4.Click **File>Examples> Grove\_Indoor\_Environment\_Demo** and select the demo Click **upload** icon

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Upload\_Indoor\_Kit\_Demo.png)

5.Open **Serial Monitor**, it will print the sensors’ information:

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Indoor\_Kit\_Serial\_Monitor.png)

6.Rotate the Encoder to check the sensor value on the LCD.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Indoor\_Kit\_Rotate\_Encoder.png)

7.In the **“Send TextBox”**, you can enter the following command to operate the sensors and actuators:

_set \[sensor]\[condition:>, < or =]\[ threshold],\[actuator]=\[action]_

|  Example                         |  Description                                                                                                                                                                                          |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  \_set temp>40, relay=1\_        |  if temperature is higher than 40℃, the relay opens.                                                                                                                                                  |
|  \_set temp>40, sleep=1\_        |  if temperature is >40℃, nothing to do.                                                                                                                                                               |
|  \_set humi>60, buzzer=1\_       |  if humidity is >60%, the buzzer beeps.                                                                                                                                                               |
|  \_set light>600, servo=90\_     |  if light intensity is >600, the servo truns 90°.                                                                                                                                                     |
|  \_set uv>80, relay=0\_          |  if UV intensity is >80, the relay closes.                                                                                                                                                            |
|  \_set pir=1, buzzer=1\_         |  if people detected, the buzzer beeps.                                                                                                                                                                |
|  \_set ms>40, relay=1\_          |  if moisture is >40, the relay opens.                                                                                                                                                                 |
|  \_set ssid=name, psw=password\_ |  set the wifi SSID and Password.you can open a web browser, and go to the IP address displayed on the Serial Monitor or LCD. The default port is 88. he default port is 88. Such as: 192.168.1.101:88 |

Note:

* The command should be ended with ‘/n’, so **“NewLine”** (in the Serial Monitor) should be selected.
* A actuator can only be controlled by a sensor. If A sensor wants to control a actuator(has be controlled by B sensor), B sensor should be set sleep.

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Indoor\_Kit\_command.png)

8.WiFi connection. open the Serial Monitor, and set your ssid and password(as below). Check the local IP on the LCD or Serial Monitor. On a device connected on the same network, open a web browser, and go to the IP address above, you can see the sensor value.

_**Note: When visiting the web server, a port number(88)should be added,such as: 172.20.10.2:88.**_

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Indoor\_Kit\_SSID\_PSW.png)

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Indoor\_Kit\_Local\_IP.png)

![](https://github.com/SeeedDocument/Grove\_Indoor\_Environment\_Kit\_for\_Edison/raw/master/img/Indoor\_Kit\_Web\_Server.png)

## Resource

* [Grove Indoor Environment Kit Source Code](https://github.com/Seeed-Studio/Grove\_Indoor\_Environment\_Demo)
* [Edison Getting Started Guide](https://communities.intel.com/community/makers/edison/getting-started)
* [Intel Edison Software & Documentation](https://communities.intel.com/community/makers/edison/documentation)

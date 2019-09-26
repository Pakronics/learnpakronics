---
title: Grove - PS/2 Adapter
category: Others
bzurl: 'https://www.seeedstudio.com/Grove-PS%262-Adapter-p-966.html'
oldwikiname: Grove - PS/2 Adapter
prodimagename: PS221_sensor.jpg
surveyurl: 'https://www.research.net/r/Grove_PS-2_Adapter'
sku: 103020003
---

# Grove PS 2 Adapter

![](https://github.com/SeeedDocument/Grove-PS_2_Adapter/raw/master/img/PS221_sensor.jpg)

The PS/2 Adapter enables you to connect a PS2 device to the Arduino/Seeeduino mainboards. With the help of PS2Keyboard/PS2MouseNlibrary, you can create the bridge between these PS2 device and Arduino/Seeeduino.

[![](https://github.com/SeeedDocument/Seeed-WiKi/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/Grove-PS%262-Adapter-p-966.html)

## Features

* Standard Grove interface
* Standard PS/2 interface

## Specification

|  Item |  Min |  Typical |  Max |  Unit |
| :--- | :--- | :--- | :--- | :--- |
|  Voltage |  4.75 |  5.0 |  5.25 |  V |
|  Current |  100 |  mA |  |  |
|  Communication Mode |  PS/2 Communication Protocol |  / |  |  |
|  Clock Frequency |  10 |  15 |  33 |  KHZ |

## Application Ideas

* PS/2 mouse and keyboard input

## Usage

The PS/2 connector is a 6-pin Mini-DIN connector used for connecting keyboard and mouse to a PC compatible computer system.The PS/2 designs on keyboard and mouse interfaces are electrically similar and employ the same communication protocol. Today, this connector has been replaced by USB, but as Arduino/Seeeduino, it is also a good choice to use the PS/2 connector as it is more convenient and cheaper when you need a mouse or keyboard.

A PS/2 connector has 6 pins as you can see from the following diagram. Pin 1 and pin 6 are not connected. Pin 3 is for ground, and pin 4 is for power. The other 2 pins are for clock and data.

![](https://github.com/SeeedDocument/Grove-PS_2_Adapter/raw/master/img/MiniDIN-6_Connector.svg.png)

|  Pin |  Name |  Function |  Correspond to the Grove Interface |
| :--- | :--- | :--- | :--- |
|  1 |  +DATA |  Data |  DATA |
|  2 |  NC |  Reserved |  - |
|  3 |  GND |  GND Line |  GND |
|  4 |  Vcc |  +5DCV |  VCC |
|  5 |  +CLK |  Clock frequency |  CLK |
|  6 |  NC |  Reserved |  - |

1.Plug the PS/2 mouse or keyboard to the Grove-PS/2 Adapter, and then connect Grove to the D5/D6 of [Grove - Base Shield](http://www.seeedstudio.com/depot/grove-base-shield-p-754.html?cPath=132_134). You can change the digital port as you like. But, don't forget to change the port number in the definition of the demo code at the same time.

!!!Note Pin 5 is the mouse data pin, pin 6 is the clock pin.

2.Plug the Base Shield into Arduino/Seeeduino and connect Arduino/Seeeduino to PC via a USB cable.

![](https://github.com/SeeedDocument/Grove-PS_2_Adapter/raw/master/img/PS2_sensorss.jpg)

3.Download [PS2 Adapter library](https://github.com/SeeedDocument/Grove-PS_2_Adapter/raw/master/res/PS2_Adapter_Library.zip), Unzip and put them in the libraries file of Arduino IDE by the path: ..\arduino-1.0\libraries.

4.Restart the Arduino IDE, open one of the demo codes, for example ps2\_mouse directly by the path:File -&gt; Example -&gt;PS2\_Adapter-&gt;ps2\_kbd.

```text
/*
 * an Arduino sketch to interface with a ps/2 keyboard.
 * Also uses serial protocol to talk back to the host
 * and report what it finds. Used the ps2 library.
 */

#include &lt;ps2.h&gt;

/*
 * Pin 5 is the ps2 data pin, pin 6 is the clock pin
 * Feel free to use whatever pins are convenient.
 */

PS2 kbd(6, 5);

void kbd_init()
{
    char ack;

    kbd.write(0xff);  // send reset code
    ack = kbd.read();  // byte, kbd does self test
    ack = kbd.read();  // another ack when self test is done
}

void setup()
{
    Serial.begin(9600);
    kbd_init();
}

/*
 * get a keycode from the kbd and report it back to the
 * host via the serial line.
 */
void loop()
{
    unsigned char code;

    for (;;) { /* ever */
    /* read a keycode */
        code = kbd.read();
    /* send the data back up */
        Serial.println(code, HEX);
        // delay(20);  /* twiddle */
    }
}
```

Please click [here](http://www.seeedstudio.com/wiki/Upload_Code) if you do not know how to upload. After uploading the firmware to the MCU,you can check the status via a Serial Monitor\(9600 baudrate\):

![](https://github.com/SeeedDocument/Grove-PS_2_Adapter/raw/master/img/Result.jpg)

X ,Y output value changes correspondingly while the mouse move around.

## Resources

* [Grove - PS/2 Adapter Eagle File](https://github.com/SeeedDocument/Grove-PS_2_Adapter/raw/master/res/Grove-PS2_Adapter_eagle_file.zip)
* [PS2 Adapter Library](https://github.com/SeeedDocument/Grove-PS_2_Adapter/raw/master/res/PS2_Adapter_Library.zip)


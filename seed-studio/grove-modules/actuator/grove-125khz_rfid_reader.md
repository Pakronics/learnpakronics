---
oldwikiname: Grove_-_125KHz_RFID_Reader
bzprodimageurl: http://statics3.seeedstudio.com/images/product/gr125k.jpg
prodimagename: Grove-125KHz_RFID_Reader.jpg
surveyurl: https://www.research.net/r/Grove-125KHz_RFID_Reader
bzurl: https://seeedstudio.com/Grove-125KHz-RFID-Reader-p-1008.html
title: Grove - 125KHz RFID Reader
tags: grove_digital, io_5v, plat_duino, plat_pi
sku: 113020002
category: Communication
---

# Grove 125KHz RFID Reader

![](https://raw.githubusercontent.com/SeeedDocument/Grove-125KHz\_RFID\_Reader/master/img/Grove-125KHz\_RFID\_Reader.jpg)

This Grove-125KHz RFID Reader is a module used to read uem4100 RFID card information with two output formats: Uart and Wiegand. It has a sensitivity with maximum 7cm sensing distance. There is also [the electronic brick version](http://www.seeedstudio.com/depot/electronic-brick-125khz-rfid-card-reader-p-702.html?cPath=52) of this module. It can help you with project like internet of thing and access control system.

And you should use the module below while using RFID reader:

* [RFID tag combo (125khz)](http://www.seeedstudio.com/depot/rfid-tag-combo-125khz-5-pcs-p-700.html?cPath=19\_24)

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get\_One\_Now\_Banner.png)](http://www.seeedstudio.com/depot/grove-125khz-rfid-reader-p-1008.html)

## Specifications

* Voltage: 4.75-5.25V
* Working Frequency: 125 KHz
* Sensing Distance(Max): 70mm
* TTL Output: 9600 baudrate, 8 data bits, 1 stop bit, and no verify bit
* Wiegand Output: 26 bits Wiegand format, 1 even verify bit, 24 data bits, and 1 odd verify bit

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

## Platforms Supported

## Demonstration

Here we show how to read RFID information using the Grove - 125KHz RFID Reader. Connect Grove - 125KHz RFID Reader to UART of Grove - Base Shield.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-125KHz\_RFID\_Reader/master/img/RFID\_reader.jpg)

### Uart Mode (Jumper set to the left two pins)

You would need to select the jumper to "U" to enter this mode, and the setting is: 9600bps, N, 8, 1, TTL output

```c
/*
  link between the computer and the SoftSerial Shield
  at 9600 bps 8-N-1
  Computer is connected to Hardware UART
  SoftSerial Shield is connected to the Software UART:D2&D3
*/

#include <SoftwareSerial.h>

SoftwareSerial SoftSerial(2, 3);
unsigned char buffer[64];       // buffer array for data receive over serial port
int count = 0;                    // counter for buffer array

void setup()
{
    SoftSerial.begin(9600);     // the SoftSerial baud rate
    Serial.begin(9600);         // the Serial port of Arduino baud rate.
}

void loop()
{
    // if date is coming from software serial port ==> data is coming from SoftSerial shield
    if (SoftSerial.available())              
    {
        while(SoftSerial.available())               // reading data into char array
        {
            buffer[count++] = SoftSerial.read();      // writing data into array
            if(count == 64)break;
        }
        Serial.write(buffer, count);     // if no data transmission ends, write buffer to hardware serial port
        clearBufferArray();             // call clearBufferArray function to clear the stored data from the array
        count = 0;                      // set counter of while loop to zero
    }
    if (Serial.available())             // if data is available on hardware serial port ==> data is coming from PC or notebook
    SoftSerial.write(Serial.read());    // write it to the SoftSerial shield
}
void clearBufferArray()                 // function to clear buffer array
{
    // clear all index of array with command NULL
    for (int i=0; i<count; i++)
    {
        buffer[i]=NULL;
    }                  
}
```

Open the Serial Monitor, the card information can be displayed as shown below:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-125KHz\_RFID\_Reader/master/img/Read\_Data\_.jpg)

### Wiegand Mode (Jumper Set to the Right two Pins)

You would need to select the jumper to "W" to enter this mode. The [Wiegand demo code](https://raw.githubusercontent.com/SeeedDocument/Grove-125KHz\_RFID\_Reader/master/res/RFID\_Wiegand\_INT.zip) for Seeeduino is designed to read Wiegand data in interrupt mode.

In Wiegand Mode, output data is formatted with 26bits including 24bits card info and 2 bits parity.

&#x20;bit

&#x20;0

&#x20;1

&#x20;2

&#x20;3

&#x20;4

&#x20;5

&#x20;6

&#x20;7

&#x20;8

&#x20;9

&#x20;10

&#x20;11

&#x20;12

&#x20;13

&#x20;14

&#x20;15

&#x20;16

&#x20;17

&#x20;18

&#x20;19

&#x20;20

&#x20;21

&#x20;22

&#x20;23

&#x20;24

&#x20;25

&#x20;\-

&#x20;PE

&#x20;D

&#x20;P0

&#x20;\-

&#x20;\-

&#x20;E

&#x20;0

&#x20;\-

&#x20;\-

&#x20;\-

&#x20;D2\[7..0]

&#x20;D1\[7..0]

&#x20;D0\[7..0]

&#x20;\-

* PE is even bit, PO is odd bit;
* E is the data bit which was involved in even, O is the data bit which was involved in odd;
* DX\[7..0] is the data bit which correspond to Mifare@ Standard & Light card read only ID;

### How to convert the output to Card Number

Take ID: 0009776930 for example:

* Card Number ID: 0009776930 ------- Decimalism \[Start Bit(00) + Card Number(8 numbers)]
* Output: 0700952F229F ------------- Hex \[\[Start Bit(07h) + Card Number(8 numbers) + Checksum]
* The calculator for decimal and hex numbers is available online.

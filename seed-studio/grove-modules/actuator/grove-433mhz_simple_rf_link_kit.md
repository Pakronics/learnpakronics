---
oldwikiname: Grove_-_433MHz_Simple_RF_Link_Kit
bzprodimageurl: 'http://statics3.seeedstudio.com/images/product/433MHz RF kit.jpg'
prodimagename: 433MHz_Simple_RF.jpg
surveyurl: 'https://www.research.net/r/Grove-433MHz_Simple_RF_Link_Kit'
bzurl: 'https://seeedstudio.com/Grove-433MHz-Simple-RF-link-kit-p-1062.html'
title: Grove - 433MHz Simple RF Link Kit
sku: 113060000
category: Communication
---

# Grove 433MHz Simple RF Link Kit

![](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/img/433MHz_Simple_RF.jpg)

This kit is used for one way wireless communication at a frequency of 433MHz and includes a transmitter module and a receiver module. The twig configuration of this kit allows for around 40 meters of transmitting distance indoors, or around 100 meters outside.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-433MHz-Simple-RF-link-kit-p-1062.html)

## Version Tracker

| Revision | Description | Release |
| :--- | :--- | :--- |
| v0.9b | Initial public release | 03,Oct,2011 |

## Features

* GROVE compatible interface.
* Uses ASK \(Amplitude Shift Keying\) Modulation.
* One way communication.

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove_System/)

## Specifications

### Transmitter Module

|  Item |  Min |  Typical |  Max |  Unit |
| :--- | :--- | :--- | :--- | :--- |
|  Working Voltage |  3.0 |  5.0 |  12.0 |  VDC |
|  Current |  3 |  / |  10 |  mA |
|  Work Mode |  ASK |  / |  |  |
|  Transmit Power\(Max\) |  15 |  mW |  |  |
|  Working Distance |  40 |  / |  100 |  m |

### Receiver Module

| Item | Typical | Unit |
| :--- | :--- | :--- |
| Working Voltage | 5 | VDC |
| Quiescent Current | 5 | mA |
| Receiver Sensitivity | -105 | dBm |
| Operating frequency | 433.92 | MHz |

## Application Ideas

* Remote control
* Remote automation
* Alarm

## Usage

The transmitter and receiver modules both rely on a single wire for communication. Though using the UART supplied by the Arduino platform can work, it is recommended, instead, to use the VirtualWire library which uses Amplitude Shift Keying for modulation which provides better communication.

Both the transmitter and receiver modules require three wires: Vcc, Ground, and signal. Pin 2 of both parts of the kit are not connected.

* Connect the Transmitter module to Digital I/O 2 of the [Grove-Base Shield V2](/Base_Shield_V2) on the Arduino being used for transmission.

Error creating thumbnail: Invalid thumbnail parameters

* Connect the Receiver module to Digital I/O 2 of the [Grove-Base Shield V2](/Base_Shield_V2) on the receiving Arduino.

Error creating thumbnail: Invalid thumbnail parameters

* Download the [VirtualWire library](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/VirtualWire_Library.zip) and unzip it into the libraries file of Arduino IDE by the path: ..\arduino-1.0\libraries. Please reference [here](http://www.pjrc.com/teensy/td_libs_VirtualWire.html).
* Upload the code below for transmitter module:

```text
    #include <VirtualWire.h>

    //Grove - 315(433) RF link kit Demo v1.0
    //by :http://www.seeedstudio.com/
    //connect the sent module to D2 to use  
    #include <VirtualWire.h>

    int RF_TX_PIN = 2;

    void setup()
    {
      vw_set_tx_pin(RF_TX_PIN); // Setup transmit pin
      vw_setup(2000); // Transmission speed in bits per second.
    }

    void loop()
    {
      const char *msg = "hello";
      vw_send((uint8_t *)msg, strlen(msg));  // Send 'hello' every 400ms.
      delay(400);

    }
```

* Upload the code below for receiver module:

```text
    //Grove - 315(433) RF link kit Demo v1.0
    //by :http://www.seeedstudio.com/
    //connect the receive module to D2 to use ..
    #include <VirtualWire.h>

    int RF_RX_PIN = 2;

    void setup()
    {
      Serial.begin(9600);
      Serial.println("setup");
      vw_set_rx_pin(RF_RX_PIN);  // Setup receive pin.
      vw_setup(2000); // Transmission speed in bits per second.
      vw_rx_start(); // Start the PLL receiver.
    }

    void loop()
    {
      uint8_t buf[VW_MAX_MESSAGE_LEN];
      uint8_t buflen = VW_MAX_MESSAGE_LEN;
      if(vw_get_message(buf, &buflen)) // non-blocking I/O
      {
        int i;
        // Message with a good checksum received, dump HEX
        Serial.print("Got: ");
        for(i = 0; i < buflen; ++i)
        {
          Serial.print(buf[i], HEX);
          Serial.print(" ");
          //Serial.print(buf[i]);
        }
        Serial.println("");
      }
    }
```

* Open the serial monitor of receiver module to see the result.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/img/Receive_Data.jpg)

This is just a simple transmitter and receiver instance as a reference.

## Resources

* [VirtualWire Library.zip](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/VirtualWire_Library.zip)
* [433MHz\_demo.zip](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/315MHz_Demo.zip)
* [VirtualWire Documentation](http://www.open.com.au/mikem/arduino/VirtualWire.pdf)
* [TI:LM358PSR](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/1110010P1.pdf)
* [R433A Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-433MHz_Simple_RF_Link_Kit/master/res/ADI;ACTR433A.pdf)


---
oldwikiname: Grove_-_Serial_Bluetooth_v3.0‏‎
bzprodimageurl: http://statics3.seeedstudio.com/images/product/113020008 1.jpg
prodimagename: Grove-Serial_Bluetooth_v3.0.jpg
surveyurl: https://www.research.net/r/Grove-Serial_Bluetooth_v3_0
bzurl: https://seeedstudio.com/Grove-Serial-Bluetooth-v3.0-p-2475.html
title: Grove - Serial Bluetooth v3.0
sku: 113020008
category: Communication
---

# Grove Serial Bluetooth v3.0

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/img/Grove-Serial\_Bluetooth\_v3.0.jpg)

Grove - Serial Bluetooth is an easy to use module compatible with the existing Grove Base Shield, and designed for transparent wireless serial connection setup. The serial port Bluetooth module is fully qualified Bluetooth V2.0+EDR(Enhanced Data Rate) 2Mbps Modulation with complete 2.4GHz radio transceiver and baseband. It uses CSR Bluecore 04-External single chip Bluetooth system with CMOS technology and with AFH(Adaptive Frequency Hopping Feature).It has the smallest footprint of 12.7mm x 27mm. Hope it will simplify your overall design/development cycle.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get\_One\_Now\_Banner.png)](https://www.seeedstudio.com/Grove-Serial-Bluetooth-v3.0-p-2475.html)

## Specifications

* Operating Voltage: 5.0VDC
* Data Rate: 2Mbps
* RF Transmit Power (Max)：+4dBm
* Sensitivity：-80dBm
* Fully Qualified Bluetooth V2.0+EDR 3Mbps Modulation
* Selectable baud rate
* Auto-reconnect in 30 min when disconnected as a result of beyond the range of connection

!!!Tip More details about Grove modules please refer to [Grove System](http://wiki.seeed.cc/Grove\_System/)

## Demonstration

Two Bluethooth modules work as shown below:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/img/Ppt5.JPG)

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/img/Ppt6.JPG)

### Hardware Installation

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/img/Grove\_serial\_bluetooth\_3\_.jpg.png)

### Download Code and Upload

1. You can download the code in github, click [here](https://github.com/Seeed-Studio/Bluetooth\_Shield\_V2\_Demo\_Code/archive/master.zip),then extract it to libraries folder of Arduino.
2. Open Arduino IDE, open File -> Examples -> Bluetooth\_Shield\_V2\_Demo\_Code -> Master\_Button, then you open the code of Master,modify the code as follows:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/img/Grove\_serial\_bluetooth\_4\_.jpg.png)

1. Open Arduino IDE, open File -> Examples -> Bluetooth\_Shield\_V2\_Demo\_Code -> Slave\_led, then you open the code of Slave and modify the code as well like above.
2. Save the modification and click Upload to Upload the code, if you have any problem about how to start Arduino, please click [here](https://app.gitbook.com/Getting\_Started\_with\_Seeeduino) for some help.

### Check The Result

1. After finish Uploading the code to both Master and Slave, reset the two devices meanwhile
2. You can see the led blink, indicate that devices was initializing and connecting.
3. After about servel seconds, led on, indicate that Master and Slave had connected.

Note If the phenomenon is not observed above, try unplugging the power and re-plug in again.

## Reference

### Commands to change default configuration

**1. Set working MODE**

| Command  | Description                                 |
| -------- | ------------------------------------------- |
| AT+ROLES | Set device working mode as client (slave).  |
| AT+ROLEM | Set device working mode as server (master). |

**2.Set BAUDRATE**

|  AT+BAUD6                                                                               |  Set baudrate 38400. Save and Rest. |
| --------------------------------------------------------------------------------------- | ----------------------------------- |
|  Supported baudrate: 4--9600, 5--19200,6--38400,7--57600,8--115200,9--230400,A--460800. |                                     |

**3. Set Device NAME**

| Command        | Description                                    |
| -------------- | ---------------------------------------------- |
| AT+NMAEabcdefg | Set device name as “abcdefg”.Max length is 12. |

**4. Set PINCODE**

| Command    | Description                          |
| ---------- | ------------------------------------ |
| AT+PIN2222 | Set pincode “2222”,Max length is 12. |

**5.Restore all setup value to factory setup**

| Command    | Description                              |
| ---------- | ---------------------------------------- |
| AT+DEFAULT | Restore all setup value to factory setup |

**6. Query module address**

| Command | Description          |
| ------- | -------------------- |
| AT+ADDR | Query module address |

**7. Query Last Connected Device Address**

| Command | Description          |
| ------- | -------------------- |
| AT+RADD | Query module address |

## Resources

* [Serial Bluetooth Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/res/Grove-Serial\_Bluetooth\_eagle\_file.zip)
* [Bluetooth Software Instruction](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/res/Bluetooth\_Software\_Instruction.pdf)
* [Bluetooth - Module Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Serial\_Bluetooth\_v3.0/master/res/Bluetooth\_module.pdf)

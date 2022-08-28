# LED Control Over Bluetooth

## Learning Objectives:

After performing this lab exercise, you will be able to:

* Create Arduino sketch (code) and program Arduino/Genuino 101 board
* Understand the working of Bluetooth Low Energy protocol
* Create a BLE service using Genuino 101 board
* Connect to Genuino 101 board service from PC/mobile BLE app
* Control the LED on/off using PC/mobile app

## Working principle of key components

Before performing this lab experiment, it is important to learn following concepts:

* Arduino/Genuino 101 is a low-power consumption and high-performance version of Arduino board with Bluetooth low-energy (BLE) and 6-axis accelerometer on board. It is compatible with Arduino/Genuino Uno in term of form factor and peripheral list. (For more details, please visit: [https://www.arduino.cc/en/Main/ArduinoBoard101](https://www.arduino.cc/en/Main/ArduinoBoard101)).
* Arduino/Genuino 101 can be easily programmed using Arduino IDE (version 1.6.7 and higher). However, the hardware libraries for Arduino/Genuino 101 board needs to be updated / installed. (Refer appendix for detailed procedure).
* CurieBLE library is used for programming the on-board BLE of Arduino/Genuino 101. Bluetooth 4.0 supports both traditional Bluetooth and the new Bluetooth Low Energy (or BLE). BLE is optimized for lower power consumption at lower data rates. (further details: [https://www.arduino.cc/en/Main/ArduinoBoard101](https://www.arduino.cc/en/Main/ArduinoBoard101)).
* A BLE device can act as peripheral device (or bulletin board) or central device (reader). A bulletin would post data in the form of characteristics of different services. These characteristics from bulletin (or peripheral BLE device) can be read or written by reader (central BLE devices).

![](<../../../.gitbook/assets/ble (2).jpg>)

* The information presented by the peripheral or bulletin is structured as services. Each service is further divided into characteristics. These characteristics are the actual data that is exchanged between peripheral and central devices.
* As demonstrated in this tutorial, a service can be created with a characteristic for controlling the on-board LED at pin 13. A central device (a mobile or PC app) would then be able to read the status of LED and control it (turn it on/off).
* One can use a standard service or define an own custom service. A standard service has 16 bit (or 4 hex characters) Universally Unique Identifier (UUID) whereas a custom UUID has 128 bits ( = 32 hex characters).
* A service can have multiple characteristics. A characteristics value can be up to 20 bytes long.
* A BLE device can be recognized by others using their General Advertising Profile (GAP) which contains a customizable ‘device name’ and list of services it provides.

## Key commands

Before programming the Arduino/Genuino 101, it is important to learn following key commands:

* blePeripheral.setDeviceName

Sets the BLE device name as descriptor for other devices to identifiy

* blePeripheral.setAdvertisedServiceUuid

Set the UUID of the service to be provided

* blePeripheral.addAttribute

Add services or characteristics to the BLE peripheral

* blePeripheral.setEventHandler

Assign callback functions for different BLE peripheral events

* characteristics.setValue

Sets the value of the ‘characteristics’

* characteristics.Value

Gets the value of the ‘characteristics’

* blePeripheral.poll

Polls (looks for) any even related to BLE peripheral

## Check Your Understanding

1. A BLE device can be configured as:
   1. Reader or central device
   2. Bulletin or peripheral device
   3. Both a & b
   4. None of a & b
2. A standard service has UUID of length \_\_\_\_
   1. 16 bytes
   2. 16 bits
   3. 128 bytes
   4. 128 bits
3. A custom service has UUID of length \_\_\_\_
   1. 16 bytes
   2. 16 bits
   3. 128 bytes
   4. 128 bits
4. UUID stands for
   1. Undoubtedly Unique Identifier
   2. Universally Unique Identifier
   3. User-defined Unique Identifier
   4. Unique User Identifier
5. What is NOT part of Genuino 101 board?
   1. Accelerometer
   2. Character LCD
   3. PWM pins
   4. Bluetooth
6. GAP stands for \_\_\_\_
   1. General Advertising Profile
   2. Genuino Arduino Profile
   3. Genuino Access Protocol
   4. Genuino As Peripheral
7.  A characteristic value can have a maximum length of \_\_\_

    1. 8 bytes
    2. 16 bytes
    3. 20 bytes
    4. 4 bytes



The answers to the above questions can be found at [Appendix B](appendices/appendix-b.md).

## Procedure

### Hardware Setup

1. Connect the Arduino/Genuino 101 board with computer using USB cable.

![](<../../../.gitbook/assets/3 (8).png>)

### Arduino IDE / Library Setup

1. Make sure you have Arduino IDE version 1.6.7 or higher and Intel Genuino 101 drivers installed on your computer. For installation of Arduino IDE and drivers, you can follow instructions from [Appendix A](appendices/appendix-a.md).

### Creating Sketch / Program

1. Open the sketch (G101\_Ex-1\_BLE\_LED\_control.ino) on Arduino IDE.

![](<../../../.gitbook/assets/4 (15).png>)

1. From Tools menu, select the right board (i.e., Arduino/Genuino 101) and COM Port it is connected to.

![](<../../../.gitbook/assets/5 (5).png>)

1. Compile (verify) and run (upload) the sketch on Arduino board. In case of any upload error, try pressing the Master Reset Button just at the start of upload process.

![](<../../../.gitbook/assets/6 (4).png>)

1. Open the “serial monitor” of Arduino IDE. It will be used to display the messages when BLE central device (reader – app on mobile or PC) gets connected to, disconnected from Genuino 101 board or the LED is turned on/off using the app.

### BLE App (PC / Mobile) Setup

1. BLE is supported only on Bluetooth 4.0 hardware. Ensure your computer / mobile / tablet hardware supports BLE. You’ll need appropriate BLE app to communicate with Genuino 101 over Bluetooth. We recommend following free apps: LightBlue for Mac and nRF Master Control for mobile (Android / iOS).
2. Open the app and scan for Bluetooth devices. Arduino / Genuino 101 should appear with the name “LED Controller”.

![](<../../../.gitbook/assets/7 (2).png>)

1. Click on “LED Controller” under the list of peripherals to connect to it. Once connected, the services and associated characteristics will be populated in respective tabs.

![](<../../../.gitbook/assets/8 (10).png>)

1. Clicking on “Read” button will show the value of characteristics (led\_char) as “0” and the LED on Arduino / Genuino 101 board will be off.

![](<../../../.gitbook/assets/9 (4).png>) ![](<../../../.gitbook/assets/10 (11).png>)

1. You can turn on the LED by writing “01” as the characteristics value. Verify that LED on the board is lit up. The value will be updated from 0 1, if you read again.

![](<../../../.gitbook/assets/11 (3).png>) ![](<../../../.gitbook/assets/12 (2).png>) ![](<../../../.gitbook/assets/13 (4).png>)

## Additional Exercise

You can extend your learning by trying following programming exercises:

1. Make a system to turn on/off a given digital pin of the Arduino over Bluetooth. One should supply – (1) digital pin to be controlled (2) on / off state
2. Extend the program 1 to read status of all the digital pins (pin 2 – 13) at once. One should also be able to write (turn on/off) all of them at once over Bluetooth.

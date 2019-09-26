---
title: Grove - Recorder
category: Actuator
bzurl: 'https://www.seeedstudio.com/Grove-Recorder-p-1825.html'
oldwikiname: Grove - Recorder
prodimagename: Grove-Recoder.jpg
surveyurl: 'https://www.research.net/r/Grove-Recorder'
sku: 103020018
---

# Grove Recorder

![](https://github.com/SeeedDocument/Grove_Recorder/raw/master/img/Grove-Recoder.jpg)

Grove - Recorder is based on the ISD1820P chip, and can record 8-20 secs of audio. It offers true single-chip voice recording and provides non-volatile storage. The recording time can be varied by changing the sampling resistor \(R6\) on the module's PCB. By default, the resistor on-board has a value of 100KΩ and thus the module offers a default recording time of 10 secs. The audio recording can be directly controlled by the on-board push button or by a micro-controller such as a [Seeeduino](/Seeeduino).

[![](https://github.com/SeeedDocument/Seeed-WiKi/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/Grove-Recorder-p-1825.html)

## Features

* Low power consumption
* Non-volatile storage
* User-friendly operation
* Replace a single resistor to change recording duration and sampling frequency
* Add a resistor to set play cycle mode
* Ships with and connects to an 8Ω/2W mini-speaker \(as shown in the picture\)
* Uses Standard 4-pin [Grove Cables](/GROVE_System#Grove_Cables) to connect to other [Grove](/Grove) modules or a micro-controller such as the [Seeeduino](/Seeeduino).

## Interface Function

![](https://github.com/SeeedDocument/Grove_Recorder/raw/master/img/Recorder_Bottom1.jpg) ![](https://github.com/SeeedDocument/Grove_Recorder/raw/master/img/Recorder_Top1.jpg)

① LED IndicatorModes:Record: Red LED light stays ON from the beginning of the recording duration until the end.Playback: Red LED flashes to signal end of audio playback.② Sampling resistorYou can set the recording duration and sampling rate by change sampling resistor \(R6\) based on the following table:

|  ROSC |  Duration |  Sampling Frequency |  Input Bandwidth |
| :--- | :--- | :--- | :--- |
|  80 KΩ |  8 secs |  8.0 KHz |  3.4 KHz |
|  100 KΩ \(default\) |  10 secs |  6.4 KHz |  2.6 KHz |
|  120 KΩ |  12 secs |  5.3 KHz |  2.3 KHz |
|  160 KΩ |  16 secs |  4.0 KHz |  1.7 KHz |
|  200 KΩ |  20 secs |  3.2 KHz |  1.3 KHz |

③ Playback resistorModes:Cycle: R8 is place 0Ω resistorSingle: R8 is not place resistor④ Play KeyNot used currently⑤ REC Key⑥ Grove Interface⑦ Loudspeaker Interface⑧ REC IC：ISD1820P

## Usage

Follow these steps to build a sample circuit using the **Grove - Recorder** module:

1. Connect the recorder module to the output side of the Grove circuit \(to the right of the power module\). On the input side of the circuit, you may use a [Grove - Button](/Grove-Button) or a [Grove - Slide Potentiometer](/Grove-Slide_Potentiometer) module.
2. Power up the circuit.
3. Press and hold down the REC button on the recorder module and start recording the audio. The on-board red LED will turn ON. Continue to record the audio until the red LED gets turned OFF. The LED getting turned OFF is indicative of the fact that the recording time is now over.
4. To play back the audio segment that has been recorded, press and hold down the [Grove - Button](/Grove-Button). You should now hear the audio segment you recorded being played back. Continue to press and hold down the [Grove - Button](/Grove-Button) until you see the red LED on-board the recorder module flash. The flash indicates that playback of audio is now complete. If instead of a [Grove - Button](/Grove-Button), you are using a [Grove - Slide Potentiometer](/Grove-Slide_Potentiometer), simply move the slider from GND to VCC position to hear the playback at any time.
5. To override the recorded audio, simply repeat step 3 above. The new message will override the old one.

Below is an illustration of a Grove circuit built using the [Grove - USB Power](/Grove-Mixer_Pack#2._USB_Power) power module:

![](https://github.com/SeeedDocument/Grove_Recorder/raw/master/img/REC_Grove-Recoder.JPG)

![](https://github.com/SeeedDocument/Grove_Recorder/raw/master/img/Play_Grove-Recoder.JPG)

If you do not have the Grove - USB Power module, use the [Grove - DC Jack Power](/Grove-DC_Jack_Power) module instead.

## Availability

This [Grove](/Grove) module is available as part of the following [Grove Kit Series](/GROVE_System#GROVE_Kit_Series):

* [Grove Mixer Pack V2](/GROVE_MIXER_PACK_V2)

Alternatively, it can be bought stand-alone at the [Seeed Studio Bazaar](http://www.seeedstudio.com/depot/Grove-Recorder-p-1825.html).

## Resources

* [Grove - Recorder v1.0 Schematics \(Eagle files\)](https://github.com/SeeedDocument/Grove_Recorder/raw/master/res/Grove-Recorder_v1.0.zip)
* [Grove - Recorder v1.0 Schematics \(pdf\)](https://github.com/SeeedDocument/Grove_Recorder/raw/master/res/Grove-Recorder_v1.0.pdf)
* [Datasheet ISD1820P.pdf \(Chinese\)](https://github.com/SeeedDocument/Grove_Recorder/raw/master/res/ISD1820P.pdf)


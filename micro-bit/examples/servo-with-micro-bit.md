# Servo with micro:bit

It's easy to connect up a servo to the micro:bit either using crocodile/alligator leads or a breadboard. A micro-servo such as the [SG90](https://www.pakronics.com.au/products/towerpro-sg90c-360-degree-micro-servo-1-6kg-dfser0043) or Tower hobby servo \(either 180 degree rotation or 360 degree\) can be connected from Pin0, 3V and GND and controlled by sending the signal on Pin0. Usually the wiring colouring is Orange = Signal, Red = 3V, Brown = Ground\(GND\)

[![micro:bit and servo](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/19045498178/original/VqTg1HPErS2Q2-AWpqy0lYvj6LZHptuUfA.png?1562159761)](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/19045498178/original/VqTg1HPErS2Q2-AWpqy0lYvj6LZHptuUfA.png?1562159761)

Whilst these micro-servos are known to work, it's important to note that the specified operating voltage for most servo motors is around +5V and that the micro:bit can only supply a [small amount of power to connected circuits](https://tech.microbit.org/hardware/#power-supply)[ ](https://tech.microbit.org/hardware/#power-supply)[\(3V](https://tech.microbit.org/hardware/#power-supply)[ and 90mA max\).](https://tech.microbit.org/hardware/#power-supply) The most reliable way to use this type of servo is to power the micro:bit via a battery pack and to use fresh batteries, as the battery voltage drops the servo will become less reliable. Battery powering also avoids damaging the micro:bit by letting the servo draw more current than the micro:bit can safely supply.

The optimal method for connecting a servo is to use a separate battery pack to power the servo and use the micro:bit to control it. This way you are only connecting Pin0 and GND from the micro:bit to the servo \(we still need to use GND to share a common ground with other parts of the circuit\).  

The battery pack supplies a higher voltage than the micro:bit. Do not connect the red wire from the battery pack to the micro:bit as you will damage it.

Additional battery packs often come as either 4.5V \(3 batteries\) or 6V \(4 batteries\). The micro:bit will supply 0V or 3V on the PWM pin0, and this has to be above the digital input pin threshold of the servo. If the voltage supplied to the servo is too high, half of that voltage becomes the pin threshold and the 3V from the micro:bit might not be enough to direct the servo.

[![micro:bit, servo and external battery pack](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/19045540191/original/2HzDfQrYbn9CXWhoqXJqLxqyZxQuhlajlw.png?1562226243)](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/19045540191/original/2HzDfQrYbn9CXWhoqXJqLxqyZxQuhlajlw.png?1562226243)

With the extra connections, you may find it easier to use a breadboard and a micro:bit edge connector breakout to make building the circuit easier.

### Programming

Servo motors determine their position by the ratio of on time and off time in an \(approximately\) 20 millsecond \(ms\) pulse. The micro:bit makes use of Pulse Width Modulation[ ](https://learn.sparkfun.com/tutorials/pulse-width-modulation)\(PWM\) as a way to simulate an analogue output on a digital pin. It sends a series of high speed on/off pulses to the servo which sets it’s target position. eg 0, -90, 180 degrees, or in the case of a continuous rotation servo, the speed and direction of rotation.

#### Makecode

To program the micro:bit to control the servo, we will need to send a signal to it on Pin0. [MakeCode has a handy reference for servos that describes the use of the Servo Write Pin block.](https://makecode.microbit.org/reference/pins/servo-write-pin) Note the difference in use for 180 degree rotation and 360 degree / continuous rotation servos.

[![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/19045540862/original/YYn3Y8TWSVqrg7qpEnYtuRQHEtcYPm-vsw.png?1562226930)](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/19045540862/original/YYn3Y8TWSVqrg7qpEnYtuRQHEtcYPm-vsw.png?1562226930)

####  

#### Python

In MicroPython, we need to set our initial PWM period for the pin and then write an analogue value to it

```text

from microbit import * 
# Servo control: 
# 100 = 1 millisecond pulse all right 
# 200 = 2 millisecond pulse all left 
# 150 = 1.5 millisecond pulse center 
pin0.set_analog_period(20)

while True: 
	pin0.write_analog(150)
	sleep(1000)
	pin0.write_analog(100)
	sleep(1000)
	pin0.write_analog(200)
	sleep(1000)
```

There are some mixed standards as to what pulse width causes what specific servo position \(or servo speed and direction\). This data can be found by searching for the datasheet for the model number of the servo eg SG90. 


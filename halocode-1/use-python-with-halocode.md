# Use Python with HaloCode

HaloCode is a MicroPython-based single board computer.  
Python code need to be uploaded to HaloCode to run.

**Start Using Python**

Switch the programming mode from "Blocks" to "Python" to start using Python.

![](../.gitbook/assets/0%20%2825%29.png)

**Note: please make sure that "HaloCode" is currently selected.**

![](../.gitbook/assets/1%20%2810%29.png)

Here's an example code:

import halo

import event

@event.start

def on\_start\(\):

 halo.led.show\_all\(122, 239, 10\)

 time.sleep\(3\)

 halo.led.off\_all\(\)

After programming, click "Upload" to upload the program to HaloCode.

![](../.gitbook/assets/2%20%2810%29.png)

**Convert Blocks to Python Code**

In the Scripts area, click   ![](../.gitbook/assets/3%20%281%29.png)   to covert blocks to Python. The following is an example:

![](../.gitbook/assets/4%20%282%29.png)

**Use HaloCode's LEDs**

**LED Ring**

The ID and position of each of the 12 LEDs are as follows:

![](../.gitbook/assets/5%20%2811%29.png)

**led.show\_all\(r, g, b\)**

Set the color of all the LEDs, mixed by red, green, and blue, each color with a value range 0-255.

halo.led.show\_all\(255, 0, 0\) \# Set all the LEDs to color red

**led.off\_all\(\)**

Turn off all the LEDs.

halo.led.off\_all\(\) \# Turn off all the LEDs

**led.show\_ring\(color\)**

Set the color of all 12 LEDs at the same time. There are ten colors: red, green, blue, yellow, cyan, purple, white, orange, black, and gray.

halo.led.show\_ring\('red orange yellow green cyan blue purple white white white white white'\) \# Set the 12 LEDs to color red, orange, yellow, green, cyan, blue, purple, white, white, white, white, and white respectively

**led.show\_single\(led\_id, r, g, b\)**

Set the color of one specified LED.

halo.led.show\_single\(1, 255, 0, 0\) \# Set the color of the first LED to red

**led.off\_single\(led\_id\)**

Turn off one specified LED.

halo.led.off\_single\(4\) \# Turn off the fourth LED

**led.show\_animation\(name\)**

Show the default LED animation. There are four options: spoondrift, meteor, rainbow, and firefly.

halo.led.show\_animation\('rainbow'\) \# Show the "rainbow" LED animation

**led.ring\_graph\(percentage\)**

Use the status of the LED ring to display percentage.

halo.led.ring\_graph\(60\) \# Use the LED ring to display 60%

**Use the Sensors of HaloCode**

**button.is\_pressed\(\)**

If the button is pressed, return True; otherwise, return False.

print\(halo.button.is\_pressed\(\)\) \# Print True if the button is pressed

**microphone.get\_loudness\(\)**

Get the loudness of the microphone. The range is 0-100.

print\(halo.microphone.get\_loudness\(\)\) \# Output the loudness

**motion\_sensor.is\_shaked\(\)**

Tell whether HaloCode is being shaken. The result is True or False.

print\(halo.motion\_sensor.is\_shaked\(\)\) \# If HaloCode is being shaken, return True

**motion\_sensor.is\_tilted\_left\(\)/motion\_sensor.is\_tilted\_right\(\)**

Tell whether HaloCode is tilted to the right or left. The result is True or False.

print\(halo.motion\_sensor.is\_tilted\_left\(\)\) \# If HaloCode is left-tilted, return True

**motion\_sensor.is\_arrow\_up\(\)/motion\_sensor.is\_arrow\_down\(\)**

Tell whether HaloCode is placed arrow-up or arrow-down. The result is True or False.

print\(halo.motion\_sensor.is\_arrow\_up\(\)\) \# If HaloCode is placed arrow-up, return True

**Gyroscope**

Get the roll, pitch or yaw value of HaloCode's gyroscope

* motion\_sensor.get\_roll\(\)
* motion\_sensor.get\_pitch\(\)
* motion\_sensor.get\_yaw\(\)

Get the gyroscope's rotation value \(in degrees\) around a certain axis.

* motion\_sensor.get\_rotation\(axis\): x, y, or z axis
* motion\_sensor.reset\_rotation\(axis="all"\): reset the rotation angles of the gyro

You can use motion\_sensor.get\_shake\_strength\(\) to get the intensity of the shaking.

print\("The yaw and pitch is:", halo.motion\_sensor.get\_yaw\(\), halo.motion\_sensor.get\_pitch\(\)\) \# output the yaw and pitch value of the gyro

print\("The rotation value is:", halo.motion\_sensor.get\_rotation\(x\), halo.motion\_sensor.get\_rotation\(y\), halo.motion\_sensor.get\_rotation\(z\)\)

halo.motion\_sensor.reset\_roation\(\) \# reset the rotation value.

print\("Shake strength:", halo.motion\_sensor.get\_shake\_strength\(\)\)

**get\_timer\(\)**

Get the timer value in seconds \(since startup or last reset\).

print\(halo.get\_timer\(\)\) \# print the timer value since startup or last reset

**reset\_timer\(\)**

Reset the timer.

halo.reset\_timer\(\)

print\(halo.get\_timer\(\)\) \# prints 0

**HaloCode's Event and Flow Control**

HaloCode supports events \(like when the button is pressed\), and it also supports multi-threading.

If you wish to use event, declare a function and register it to the event. A program can only register no more than 6 event functions.

Example:

def on\_button\_pressed\(\): \# define a function

 print\("The button is pressed!"\)

halo.on\_button\_pressed\(\) \# register it to "when button is pressed" event

**on\_button\_pressed\(\)**

When the button is pressed, run the function.

def on\_button\_pressed\(\):

 print\("The button is pressed!"\)

halo.on\_button\_pressed\(\)

**on\_shaked\(\)**

When HaloCode is being shaken, call the function.

def on\_shaked\(\):

 print\("I'm shaken!"\)

halo.on\_shaked\(\)

**on\_tilted\_left\(\)**

Call the function when HaloCode is tilted to the left.

def on\_tilted\_left\(\):

 print\("I'm left-tilted!"\)

halo.on\_tilted\_left\(\)

**on\_greater\_than\(volume, 'microphone'\)**

When the loudness is over a certain value, call the function.

def on\_greater\_than\(\):

 print\("The loudness is over 50! Too loud!"\)

halo.on\_greater\_than\(50, 'microphone'\)

**on\_received\(message\_name\)**

When the specified message is received, call the function.

def on\_received\(\):

 print\("Game start!"\)

halo.on\_received\("game\_start"\)


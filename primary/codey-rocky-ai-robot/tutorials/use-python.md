# Use Python

Codey is a micropython-based robot.  
Python code need to be uploaded to Codey in order to run.

### Start Using Python <a id="start-using-python"></a>

Start using Python by switching the programming mode from "Blocks" to "Python"

![](http://docs.makeblock.com/codeyrocky/en/tutorials/use-python-1.png)

**Note: please make sure that Codey is currently selected.**

![](http://docs.makeblock.com/codeyrocky/en/tutorials/use-python-2.png)

Here's an example code:

```text
import codey
import rocky
import time
import event

@event.start
def on_start():
    codey.led.show(255,0,0)
    rocky.forward(50,1)
```

After programming, click "Upload" to upload the program to Codey.

### Convert Blocks to Python <a id="convert-blocks-to-python"></a>

In the Scripts area, click   ![](http://docs.makeblock.com/codeyrocky/en/tutorials/use-python-3.png)   to covert blocks to Python. The following is an example:

![](http://docs.makeblock.com/codeyrocky/en/tutorials/use-python-4.png)

### Use the Face Panel <a id="use-the-face-panel"></a>

#### display.show\(text, wait=False\) <a id="displayshowtext-waitfalse"></a>

Show a piece of text on Codey's Face Panel.

```text
codey.display.show("hello world", wait=False)
codey.display.show(3.14, wait=False)
codey.display.show("14:02", wait=False)
```

#### display.show\_image\(image, time\) <a id="displayshowimageimage-time"></a>

Show an image on Codey's face panel. The image displayed needs to be converted to hexadecimal data.

If the duration is any other number than zero, the panel will turn off after the set duration.

```text
codey.display.show_image("00003c7e7e3c000000003c7e7e3c0000", time_s=1)
```

#### display.show\_image\(image, x, y\) <a id="displayshowimageimage-x-y"></a>

Display an image on Codey's face panel at a specific location \(x, y\).

```text
codey.display.show_image("000c18181c0c000000000c1c18180c00", 0, 0)
# Show a smiley face at the upper-left corner
```

#### codey.display.set\_pixel\(x, y, status\) / codey.display.toggle\_pixel\(x, y\) <a id="codeydisplaysetpixelx-y-status--codeydisplaytogglepixelx-y"></a>

* set\_pixel: set the status of the pixel at \(x, y\); set `True` to light up the pixel, or `False` to turn it off
* toggle\_pixel: toggle a pixel at \(x, y\): turn on if it is off, and off if it is on

```text
codey.display.set_pixel(5, 5, True) # light up the pixel at (5, 5)
codey.display.set_pixel(5, 5, False) # turn off the pixel at (5, 5)
codey.display.toggle_pixel(5, 5) # toggle the pixel at (5, 5)
```

#### display.get\_pixel\(x, y\) <a id="displaygetpixelx-y"></a>

Check if the certain pixel of Codey is on or not. If on, return True; otherwise return False

```text
print(codey.display.get_pixel(5, 5))  # print True if the pixel at (5, 5) is on
```

#### display.clear\(\) <a id="displayclear"></a>

Clear all the contents on Codey's face panel.

```text
codey.display.clear() # turn off the face panel
```

### Use the RGB LED on the Codey <a id="use-the-rgb-led-on-the-codey"></a>

#### led.show\(r, g, b, time\) <a id="ledshowr-g-b-time"></a>

Set the color of Codey's LED.

If the duration is a non-zero number, the LED will turn off after specified seconds.

```text
codey.led.show(255, 255, 0, 1) # set the color, turn off after 1 second
codey.led.show(255, 0, 0) # change the color to red
```

#### led\_off\(\) <a id="ledoff"></a>

Turn off Codey's LED.

```text
codey.led_off() # turn off the led light
```

#### led.set\_red\(value\) / led.set\_green\(value\) / led.set\_blue\(value\) <a id="ledsetredvalue--ledsetgreenvalue--ledsetbluevalue"></a>

Set the RGB value of the LED independently. The range of each color value is 0-255.

```text
codey.led.set_red(255)
codey.led.set_green(255)
codey.led.set_blue(255)
```

### Make a Sound <a id="make-a-sound"></a>

#### speaker.play\_melody\(name\) <a id="speakerplaymelodyname"></a>

Play the a sound file.

```text
codey.speaker.play_melody("meow")
codey.speaker.play_melody("meow.wav") # .wav is optional
```

Sound file available：

* `hello.wav` : hello
* `hi.wav` :hi
* `bye.wav` : bye
* `yeah.wav` : yeah
* `wow.wav` : wow
* `laugh.wav` : laugh
* `hum.wav` : hum
* `sad.wav` : sad
* `sigh.wav` : sigh
* `annoyed.wav` : annoyed
* `angry.wav` : angry
* `surprised.wav` : scared
* `yummy.wav` : pettish
* `curious.wav` : curious
* `embarrassed.wav` : embarrassed
* `ready.wav` : ready
* `sprint.wav` : sprint
* `sleepy.wav` : snore
* `meow.wav` : meow
* `start.wav` : start
* `switch.wav` : switch
* `beeps.wav` : beeps
* `buzzing.wav` : buzz
* `exhaust.wav` : air-out
* `explosion.wav` : explosion
* `gotcha.wav` : gotcha
* `hurt.wav` : painful
* `jump.wav` : jump
* `laser.wav` : laser
* `level up.wav` : level-up
* `low energy.wav` : low-energy
* `metal clash.wav` : metal-clash
* `prompt tone.wav` : prompt-tone
* `right.wav` : right
* `wrong.wav` : wrong
* `ring.wav` : ringtone
* `score.wav` : score
* `shot.wav` : shot
* `step_1.wav` : step\_1
* `step_2.wav` : step\_2
* `wake.wav` : activate
* `warning.wav` : warning

#### speaker.play\_note\(note\_number, beats\) <a id="speakerplaynotenotenumber-beats"></a>

Tell Codey to play a musical note for a duration.

The note number is the MIDI number. You may also use note names like "C3" or "D4". Incorrect note name will produce an error in the console.

```text
codey.speaker.play_note(36, 1)
codey.speaker.play_note('c3', 0.25)
```

#### speaker.play\_tone\(frequency, beats\) <a id="speakerplaytonefrequency-beats"></a>

Play a certain frequency of sound for a duration of certain beats.

```text
codey.speaker.play_tone(700, 1)
```

#### speaker.rest\(beats\) <a id="speakerrestbeats"></a>

Pause the sound for a certain number of beats.

```text
codey.speaker.rest(0.25)
```

#### speaker.stop\_sounds\(\) <a id="speakerstopsounds"></a>

Stop all sounds.

```text
codey.speaker.stop_sounds()
```

#### speaker.volume <a id="speakervolume"></a>

Set or read the volume of Codey's speaker.

```text
codey.speaker.volume = (70) # Set the volume of Codey's speaker to 70%
print(codey.speaker.volume) # Get the current volume of Codey's speaker
```

### Use the Sensors of Codey <a id="use-the-sensors-of-codey"></a>

#### button\_a.is\_pressed\(\)/button\_b.is\_pressed\(\)/button\_c.is\_pressed\(\) <a id="buttonaispressedbuttonbispressedbuttoncispressed"></a>

If the specified button is pressed, return True; otherwise, return False.

```text
print(codey.button_a.is_pressed()) # print True if the button A is pressed.
```

#### potentiometer.get\_value\(\) <a id="potentiometergetvalue"></a>

Get the position of the potentiometer knob on Codey's side. The value will be 0-100.

```text
print(codey.potentiometer.get_value()) # Get the position of potentiometer
```

#### sound\_sensor.get\_loudness\(\) <a id="soundsensorgetloudness"></a>

Get the loudness of the sound sensor. The range is 0-100.

```text
print(codey.sound_sensor.get_loudness()) # output the loudness of the sound sensor
```

#### light\_sensor.get\_value\(\) <a id="lightsensorgetvalue"></a>

Get the light intensity detected by the light sensor. The range is 0-100.

```text
print(codey.light_sensor.get_value()) # output the light sensor's value
```

#### motion\_sensor.is\_shaked\(\) <a id="motionsensorisshaked"></a>

Tell whether the Codey is being shaken. The result is True or False.

```text
print(codey.motion_sensor.is_shaked()) # if Codey is being shaken, return True
```

#### motion\_sensor.is\_tilted\_left\(\)/motion\_sensor.is\_tilted\_right\(\)/ motion\_sensor.is\_ears\_up\(\)/motion\_sensor.is\_ears\_down\(\) <a id="motionsensoristiltedleftmotionsensoristiltedrightmotionsensorisearsupmotionsensorisearsdown"></a>

Tell whether Codey is tilted to the right/left, or placed ears-up/ears-down. The result is True or False.

```text
print(codey.motion_sensor.is_tilted_left()) # If Codey is left-tilted, return True
print(codey.motion_sensor.is_ears_up()) # If Codey is placed ears-up, return True
```

#### Gyroscope <a id="gyroscope"></a>

Get the roll, pitch or yaw value of Codey's gyroscope

* motion\_sensor.get\_roll\(\)
* motion\_sensor.get\_pitch\(\)
* motion\_sensor.get\_yaw\(\)

Get the gyroscope's rotation value \(in degrees\) around a certain axis.

* motion\_sensor.get\_rotation\(axis\): x, y, or z axis
* motion\_sensor.reset\_rotation\(axis="all"\): reset the rotation angles of the gyro

You can use motion\_sensor.get\_shake\_strength\(\) to get the intensity of the shaking.

```text
print("The yaw and pitch is:", codey.motion_sensor.get_yaw(), codey.motion_sensor.get_pitch()) # output the yaw and pitch value of the gyro
print("The rotation value is:", codey.motion_sensor.get_rotation(x), codey.motion_sensor.get_rotation(y), codey.motion_sensor.get_rotation(z))
codey.motion_sensor.reset_rotation() # reset the rotation value.
print("Shake strength:", codey.motion_sensor.get_shake_strength())
```

#### get\_timer\(\) <a id="gettimer"></a>

Get the timer value in seconds \(since startup or last reset\)

```text
print(codey.get_timer()) # print the timer value since startup or last reset
```

#### reset\_timer\(\) <a id="resettimer"></a>

Reset the timer.

```text
codey.reset_timer() 
print(codey.get_timer()) # prints 0
```

### Codey's Events and Flow Control <a id="codeys-events-and-flow-control"></a>

Codey supports events \(like when the button is pressed\), and it also supports multi-threading.

If you wish to use event, declare a function and register it to the event. A program can only register no more than 6 event functions.

Example:

```text
def on_button_a_pressed(): # define a function
    print("Button A is pressed!")

codey.on_button_a_pressed() # register it to "when button A is pressed" event
```

#### on\_button\_a\_pressed\(\)/on\_button\_b\_pressed\(\)/on\_button\_c\_pressed\(\) <a id="onbuttonapressedonbuttonbpressedonbuttoncpressed"></a>

When the button is pressed, run the function.

```text
def on_button_b_pressed():
    print("The B button is pressed")

codey.on_button_b_pressed()
```

#### on\_shaked\(\) <a id="onshaked"></a>

When Codey is shaken, call the function.

```text
def on_shaked():
    print("I'm shaken!")

codey.on_shaked()
```

#### on\_tilted\_left\(\) <a id="ontiltedleft"></a>

Call the function when Codey tilts to the left.

```text
def on_tilted_left():
    print("I'm tilted-left!")

codey.on_tilted_left()
```

#### on\_greater\_than\(volume, 'sound\_sensor'\) <a id="ongreaterthanvolume-soundsensor"></a>

When the loudness is over a certain value, call the function.

```text
def on_greater_than():
    print("The volume is over 50! Too loud!")

codey.on_greater_than(50, 'sound_sensor')
```

#### on\_less\_than\(lightness, 'light\_sensor'\) <a id="onlessthanlightness-lightsensor"></a>

When the lightness is under a certain value, call the function.

```text
def on_less_than():
    print("The light is under 30! too dark!")

codey.on_less_than(30, 'light_sensor')
```

#### on\_received\(message\_name\) <a id="onreceivedmessagename"></a>

When a Scratch broadcast is received, trigger the function.

```text
def on_received():
    print("Game start!")

codey.on_received('game_start')
```

#### broadcast\(message\_name\) <a id="broadcastmessagename"></a>

Broadcast a certain message to the Scratch system.

```text
codey.broadcast('game_start')
```

#### stop\_all\_scripts\(\)/stop\_this\_script\(\)/stop\_other\_scripts\(\) <a id="stopallscriptsstopthisscriptstopotherscripts"></a>

Stop all processes, this process, or other processes.

```text
codey.stop_all_scripts() # stop all processes on Codey
```

### Let the Rocky move <a id="let-the-rocky-move"></a>

#### forward\(speed, time\) <a id="forwardspeed-time"></a>

Tell the Rocky to move forward for a certain period of time. If the time is not set, it will keep moving. The speed range is 0-100.

```text
rocky.forward(50, 1) # run forward for 1 seconds at the speed of 50
rocky.forward(100) # run forward forever at the speed of 100
```

#### backward\(speed, time\) <a id="backwardspeed-time"></a>

Tell the Rocky to move backward for a certain period of time. If the time is not set, it will keep moving. The speed range is 0-100.

```text
rocky.backward(50)
rocky.backward(100) # run backward at the max speed of 100
```

#### turn\_right\(speed, time\) <a id="turnrightspeed-time"></a>

Tell the Rocky to turn right for a certain period of time. If the time is not set, it will keep turning. The speed range is 0-100.

```text
rocky.turn_right(50, 1) # turn right at speed 50 for 1 second
rocky.turn_right(100) # turn right at the max speed of 100
```

#### turn\_left\(speed, time\) <a id="turnleftspeed-time"></a>

Tell the Rocky to turn left for a certain period of time. If the time is not set, it will keep turning. The speed range is 0-100.

```text
rocky.turn_left(50, 1) # turn left at speed 50 for 1 second
rocky.turn_left(100) # turn left at the max speed of 100
```

#### turn\_right\_by\_degree\(angle\) <a id="turnrightbydegreeangle"></a>

Make Rocky turn right at a certain angle until done.

```text
rocky.turn_right_by_degree(90) # turn right for 90 degrees until done
```

#### turn\_left\_by\_degree\(angle\) <a id="turnleftbydegreeangle"></a>

Make Rocky turn left at a certain angle until done.

```text
rocky.turn_left_by_degree(90) # turn left for 90 degrees until done
```

#### drive\(left\_speed, right\_speed\) <a id="driveleftspeed-rightspeed"></a>

Set the speed of Codey's two wheels at the same time.

```text
rocky.drive(50, 50) # set the speed of both wheels to 50
```

#### stop\(\) <a id="stop"></a>

Stop the movement of Codey

```text
rocky.stop() # tell Codey to stop moving
```

### Use Rocky's Sensors and Light <a id="use-rockys-sensors-and-light"></a>

#### color\_ir\_sensor.set\_led\_color\(color\) <a id="colorirsensorsetledcolorcolor"></a>

Set the color of Rocky's LED. Color can be one of: "red", "green", "blue", "yellow", "purple", "cyan", "white", "black". Set the color to "black" will turn off Rocky's LED.

```text
rocky.color_ir_sensor.set_led("red")
rocky.color_ir_sensor.set_led("black")
```

#### color\_ir\_sensor.is\_obstacle\_ahead\(\) <a id="colorirsensorisobstacleahead"></a>

Tell if there is obstacle ahead. Return True or False. \(Rocky's sensor array must face forward\)

```text
print(rocky.color_ir_sensor.is_obstacle_ahead())
```

#### color\_ir\_sensor <a id="colorirsensor"></a>

Get the value of the base sensor array.

* color\_ir\_sensor.get\_light\_strength\(\): get the ambient light intensity of the environment; return 0-100
* color\_ir\_sensor.get\_reflected\_light\(\): get the reflection light value of the surface; return 0-100
* color\_ir\_sensor.get\_reflected\_infrared\(\): get the IR reflection value of the surface; return 0-100
* color\_ir\_sensor.get\_greyness\(\): get the greyness of the surface by light sensor; return 0-100
* color\_ir\_sensor.get\_red\(\): get the red value of the surface; return 0-255
* color\_ir\_sensor.get\_green\(\): get the green value of the surface; return 0-255
* color\_ir\_sensor.get\_blue\(\): get the blue value of the surface; return 0-255
* color\_ir\_sensor.is\_color\(color\_str\): Tell whether the color sensor senses the specific color; return True or False. The color\_name could be one of "red", "green", "blue", "yellow", "purple", "cyan", "white", "black".

```text
print("Lightness and Reflection: ", color_ir_sensor.get_light_strength(), color_ir_sensor.get_reflected_light())
print("IR light value: ", color_ir_sensor.get_reflected_infrared())
print("Greyness: ", color_ir_sensor.get_greyness())
print("RGB value: ", color_ir_sensor.get_red(), color_ir_sensor.get_green(), color_ir_sensor.get_blue())
print("On a red surface? ", color_ir_sensor.is_color("red"))
```

### Communicate with Infrared Signals <a id="communicate-with-infrared-signals"></a>

Codey can send and receive infrared signals.

#### ir\_send\(message\) <a id="irsendmessage"></a>

send a piece of string message with Codey's Infrared Emitter. Another Codey can receive this message with its Infrared Receiver.

```text
codey.ir_send("A")
```

#### ir\_receive\(\) <a id="irreceive"></a>

When a piece of message sent with infrared signals is received, return a string value.

```text
codey.show(codey.ir_receive())
```


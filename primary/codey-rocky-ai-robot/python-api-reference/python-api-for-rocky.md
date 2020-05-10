# Python API for Rocky



### `motion` – Rocky Chassis Movement <a id="motion-&#x2013;-rocky-chassis-movement"></a>

**Function**

`rocky.stop()`  
Rocky stops moving.

`rocky.forward(speed, t = None, straight = False)`  
Rocky moves forward, parameters：

* _speed_ The value of motion speed, parameter range is `-100 ~ 100`, negative numbers represent backwards, positive numbers represent forward.
* _t_ The value of the motion time, in `seconds`, the parameter range is `0 ~ the value range limit`. If set to 1, it means the rocky will move forward for 1s. If this parameter is not set, the forward state is maintained until there is the motion stop command or new motion command.
* _straight_ Enable the gyro sensor to correct the forward direction or not. If this parameter is not set, it is not enabled by default.

`rocky.backward(speed, t = None, straight = False)`  
Rocky moves backward, parameters：

* _speed_ The value of motion speed, parameter range is `-100 ~ 100`, negative numbers represent forward, positive numbers represent backward.
* _t_ The value of the motion time, in `seconds`, the parameter range is `0 ~ the value range limit`. If set to 1, it means the rocky will move backward for 1s. If this parameter is not set, the backward state is maintained until there is the motion stop command or new motion command.
* _straight_ Enable the gyro sensor to correct the backward direction or not. If this parameter is not set, it is not enabled by default.

`rocky.turn_left(speed, t = None)`  
Rocky turns left, parameters：

* _speed_ The value of turn speed, parameter range is -100 ~ 100, negative numbers represent turn right, positive numbers represent turn left.
* _t_ The value of the motion time, in `seconds`, the parameter range is `0 ~ the value range limit`. If set to 1, it means the rocky will turn left for 1s. If this parameter is not set, the turn left state is maintained until there is the motion stop command or new motion command.

`rocky.turn_right(speed, t = None)`  
Rocky turns right, parameters：

* _speed_ The value of turn speed, parameter range is -100 ~ 100, negative numbers represent turn right, positive numbers represent turn left.
* _t_ The value of the motion time, in `seconds`, the parameter range is `0 ~ the value range limit`. If set to 1, it means the rocky will turn left for 1s. If this parameter is not set, the turn left state is maintained until there is the motion stop command or new motion command.

`rocky.drive(left_power, right_power)`  
Rocky turns according to the set value for each motor, parameters：

* _left\_power_ Motor speed of left wheel, parameter range is `-100 ~ 100`, negative numbers represent the left wheel rotates backward, positive numbers represent the left wheel rotates forward.
* _right\_power_ Motor speed of right wheel, parameter range is `-100 ~ 100`, negative numbers represent the right wheel rotates backward, positive numbers represent the right wheel rotates forward.

`rocky.turn_right_by_degree(angle, speed = 40)`  
Rocky turns right according to the set degree, parameters：

* _angle_ Angle of rotation, negative numbers represent turn left, positive numbers represent turn right.
* _speed_ Turning speed, parameter range is `0 ~ 100`, if this parameter is not set, the default speed is 40. \(Since the gyro sensor is used for turning specific angle, it is recommended not to modify the speed to avoid the turning angle being inaccurate\).

`rocky.turn_left_by_degree(angle, speed = 40)`  
Rocky turns left according to the set degree, parameters：

* _angle_ Angle of rotation, negative numbers represent turn right, positive numbers represent turn left.
* _speed_ Turning speed, parameter range is `0 ~ 100`, if this parameter is not set, the default speed is 40. \(Since the gyro sensor is used for turning specific angle, it is recommended not to modify the speed to avoid the turning angle being inaccurate\).

**Sample Code:**

```text
import codey
import rocky
import time

rocky.forward(50, 1)
rocky.stop()
rocky.backward(50, 1)
rocky.turn_left(50, 1)
rocky.turn_right(50, 1)
rocky.drive(50, 80)
time.sleep(2)
while True:
    rocky.turn_right_by_degree(80, 40)
    rocky.turn_right_by_degree(80, 20)
```

### `color_ir_sensor` – Color IR Sensor <a id="colorirsensor-&#x2013;-color-ir-sensor"></a>

**Color Infrared Sensor Introduction**

![](http://docs.makeblock.com/codeyrocky/en/python-api/rocky-api.png)

As shown in the figure, the sensors in front of the rocky are:

* **White LED**：light white to achieve detecting the visible light reflection intensity on the surface of the object with using visible light sensor.
* **Visible Light Sensor**：detect the visible light intensity.
* **RGB LED**：light LED with specific RGB value to achieve recognizing the color with using the visible light sensor.
* **Infrared Light Sensor**：detect the infrared light intensity
* **Infrared Transmitter**：transmit infrared light to achieve detecting the infrared light reflection intensity on the surface of the object with using the infrared light sensor.

**Function**

`color_ir_sensor.get_red()`  
Get the size of the red color component of the color sensor, parameter range is `0 ~ 100`.

`color_ir_sensor.get_green()`  
Get the size of the green color component of the color sensor, parameter range is `0 ~ 100`.

`color_ir_sensor.get_blue()`  
Get the size of the blue color component of the color sensor, parameter range is `0 ~ 100`.

`color_ir_sensor.is_color(color_str)`  
Judge whether a matching color is detected, parameters：

* _color\_str_ color type, including `red`, `green`, `blue`, `yellow`, `cyan`, `purple`, `white`,`black`, the corresponding parameter is `red`, `green`, `blue`, `yellow`, `cyan`, `purple`, `white`, `black`. Return value is boolean, `Ture` represents color matching, `False` represents the colors do not match.

`color_ir_sensor.get_light_strength()`  
Get the ambient light intensity d\`etected by the visible light sensor, parameter range is 0 ~ 100.

`color_ir_sensor.get_greyness()`  
Get the grayscale value detected by the visible light sensor \(using RGB LED and visible light sensor\), parameter range is `0 ~ 100`.

`color_ir_sensor.get_reflected_light()`  
Get the visible light reflection intensity detected by the visible light sensor, parameter range is `0 ~ 100`.

`color_ir_sensor.get_reflected_infrared()`  
Get the infrared light reflection intensity detected by the infrared light receiving tube, parameter range is `0 ~ 100`.

`color_ir_sensor.is_obstacle_ahead()`  
Detect if there are obstacles in front, the return value is boolean, `Ture`represents obstacles, `False` represents no obstacles.

`color_ir_sensor.set_led_color(color_name)`  
Set color for the RGB LED light of the color sensor, parameters：

* _color\_name_ including `red`, `green`, `blue`, `yellow`, `cyan`, `purple`, `white`, `black`, the corresponding parameter is `red`, `green`, `blue`, `yellow`, `cyan`, `purple`, `white`, `black`.

**Sample Code:**

```text
import codey
import rocky

while True:
    if rocky.color_ir_sensor.is_obstacle_ahead():
        rocky.color_ir_sensor.set_led_color('white')
    else:
      rocky.color_ir_sensor.set_led_color('black')
```


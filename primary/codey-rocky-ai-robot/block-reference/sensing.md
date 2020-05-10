# Sensing

**odey**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/codey-1.png)

**Rocky – Color Infrared Sensor**

![](http://docs.makeblock.com/codeyrocky/en/python-api/rocky-api.png)

### 1. button \(\) is pressed? <a id="1-button--is-pressed"></a>

If the specified button of Codey is pressed, the report condition is met. There are three buttons: Button A, Button B, and Button C.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-1-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-1-2.png)

When Codey starts up, if Button A is pressed, Codey's screen will display "Yes". If Button A is not pressed, Codey's screen will display "No".

### 2. when Codey connected to Rocky <a id="2-when-codey-connected-to-rocky"></a>

If Codey is connected to Rocky, the report condition is met.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-2-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-2-2.png)

When Codey starts up, if Codey is connected to Rocky, Codey's screen will display "Yes". If not, Codey's screen will display "No".

### 3. gear potentiometer value <a id="3-gear-potentiometer-value"></a>

Report the position of gear potentiometer. The range of the value is 0 ~ 100, rounded to nearest integer.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-3-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-3-2.png)

When Codey starts up, the gear potentiometer value will be displayed on Codey's screen.

### 4. loudness <a id="4-loudness"></a>

Report the loudness detected by Codey's sound sensor. The range of the value is 0 ~ 100, rounded to nearest tenth.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-4-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-4-2.png)

When Codey starts up, the loudness value will be displayed on Codey's screen.

### 5. ambient light intensity <a id="5-ambient-light-intensity"></a>

Report the ambient light intensity detected by Codey's light sensor. The range of the value is 0 ~ 100, rounded to nearest tenth.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-5-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-5-2.png)

When Codey starts up, the ambient light intensity value will be displayed on Codey's screen.

### 6. battery level <a id="6-battery-level"></a>

Report Codey's battery level \(0 ~ 100, rounded to nearest ten\).

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-6-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-6-2.png)

When Codey starts up, the battery level will be displayed on Codey's screen.

### 7. shaken? <a id="7-shaken"></a>

If Codey is being shaken, the report condition is met.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-7-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-7-2.png)

When Codey starts up, if being shaken, Codey's screen will display "Yes". If not, Codey's screen will display "No".

### 8. shaking strength <a id="8-shaking-strength"></a>

Report the strength by which Codey is being shaken. The range of the shaking strength is 0 ~ 100, rounded to the nearest integer.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-8-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-8-2.png)

When Codey is being shaken, Codey's screen will display the shaking strength.

### 9. Codey \(\) tilted? <a id="9-codey--tilted"></a>

If Codey is tilted towards specified direction, the report condition is met. There are four directions: "tilted to the left", "tilted to the right", "ears up", and "ears down". The threshold value is 15 degrees.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-9-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-9-2.png)

When Codey starts up, if tilted to the left, Codey's screen will display "Yes". If not, Codey's screen will display "No".

### 10. Codey positioned as \(\)? <a id="10-codey-positioned-as-"></a>

If Codey is positioned as the specified position, the report condition is met. There are three positions: "face up", "face down", and "stand on desk".

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-10-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-10-2.png)

When Codey starts up, if Codey is positioned face-up, Codey's screen will display "Yes". If not, Codey's screen will display "No".

### 11. roll angle° <a id="11-roll-angle&#xB0;"></a>

Report Codey's roll angle.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-11-1.png)

**Parameter:**

* Roll: -90° ~ 90°, rounded to the nearest integer; positive number means right-tilted; invalid value will be set to zero.

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-11-2.png)

When Codey starts up, the screen will display Codey's roll angle.

### 12. pitch angle° <a id="12-pitch-angle&#xB0;"></a>

Report Codey's pitch angle.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-12-1.png)

**Parameter:**

* Roll: -180° ~ 180°, rounded to the nearest integer; positive number means ears-up; invalid value will be set to zero.

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-12-2.png)

When Codey starts up, the screen will display Codey's pitch angle.

### 13. rotation angle around x <a id="13-rotation-angle-around-x"></a>

Report Codey's rotation angle around the x axis.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-13-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-13-2.png)

When Codey starts up, the screen will display Codey's rotation angle around the x axis.

### 14. rotation angle around y <a id="14-rotation-angle-around-y"></a>

Report Codey's rotation angle around the y axis.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-14-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-14-2.png)

When Codey starts up, the screen will display Codey's rotation angle around the y axis.

### 15. rotation angle around z <a id="15-rotation-angle-around-z"></a>

Report Codey's rotation angle around the z axis.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-15-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-15-2.png)

When Codey starts up, the screen will display Codey's rotation angle around the z axis.

### 16. reset \(\) rotation angle° <a id="16-reset--rotation-angle&#xB0;"></a>

Reset Codey's rotation angle around specified axis/axes. There are four options: x-axis, y-axis, z-axis, and all axes.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-16-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-16-2.png)

When Codey starts up, reset rotation angles around all axes.

### 17. timer <a id="17-timer"></a>

Report Codey's timer value \(second, rounded to nearest tenth\).

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-17-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-17-2.png)

When Codey starts up, Codey's screen will display timer value.

### 18. reset timer <a id="18-reset-timer"></a>

Reset Codey's timer.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-18-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-18-2.png)

Press Button A to reset Codey's timer.

### 19. obstacles ahead? <a id="19-obstacles-ahead"></a>

If Rocky's color infrared sensor detects obstacles ahead, the report condition is met.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-19-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-19-2.png)

When Codey starts up, Codey Rocky will keep moving forward at 50% power. If Rocky detects obstacles ahead, Codey Rocky will stop moving.

### 20. the color detected is \(\)? <a id="20-the-color-detected-is-"></a>

If the color detected is the specified color, the report condition is met. There are eight colors: red, green, blue, yellow, cyan, purple, black, and white.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-20-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-20-2.png)

When Codey starts up, if the color detected by Rocky's color sensor is red, Rocky's LED will light up red.

### 21. \(\) color value detected? <a id="21--color-value-detected"></a>

Report the specified color value of the obstacle detected by Rocky's color sensor. Colors include red, green, and blue.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-21-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-21-2.png)

When Codey starts up, if Rocky detects color red, the value of red will be displayed on Codey's screen.

### 22. color sensor ambient light intensity <a id="22-color-sensor-ambient-light-intensity"></a>

Report the value of ambient light intensity detected by Rocky's color sensor.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-22-1.png)

**Parameter:**

* Light intensity: 0 ~ 100, rounded to nearest tenth; value exceeding 100 will be displayed as the maximum 100.

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-22-2.png)

When Codey starts up, Codey's screen will display the value of amibent light intensity.

### 23. color sensor reflected light intensity <a id="23-color-sensor-reflected-light-intensity"></a>

Report the value of reflected light intensity detected by Rocky's color sensor.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-23-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-23-2.png)

When Codey starts up, Codey's screen will display the value of reflected light intensity.

### 24. color sensor reflected infrared light intensity <a id="24-color-sensor-reflected-infrared-light-intensity"></a>

Report the value of reflected infrared light intensity detected by Rocky's color sensor.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-24-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-24-2.png)

When Codey starts up, Codey's screen will display the value of reflected infrared light intensity.

### 25. color sensor grey-scale value <a id="25-color-sensor-grey-scale-value"></a>

Report the grey-scale value detected by Rocky's color sensor.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-24-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/sensing-24-2.png)

When Codey starts up, Codey's screen will display the grey-scale value.  



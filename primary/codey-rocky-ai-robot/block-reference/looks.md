# Looks

**LED Dot-Matrix Display**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/codey.jpg)

The face panel of Codey is a 128-LED dot matrix, which can display English characters, numbers, and images.

**Coordinate of the Face Panel**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/codey-api.png)

As shown in the figure above, the face panel has the upper-left corner as the origin of the coordinate system, and the direction of x and y is indicated by the arrow. Parameters:

* x: -15 ~ 15
* y: -7 ~ 7

### 1. show image \(\) for \(\) secs <a id="1-show-image--for--secs"></a>

Display specified image on Codey's screen for a specified period of time.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/1-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/1-2.png)

Press Button A, Codey's screen will display these three images consecutively, for 1 second, 0.5 second, and 1 second respectively. After displaying all images, Codey's screen will turn off.

### 2. show image \(\) <a id="2-show-image-"></a>

Display specified image on Codey's screen.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/2-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/2-2.png)

When Codey starts up, the image will be displayed.

### 3. show image \(\) at the x:\(\) y:\(\) <a id="3-show-image--at-the-x-y"></a>

Display specified image at specified point of the face panel.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/3-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/3-2.png)

Press Button A, the image will be displayed at the origin.

### 4. turn off screen <a id="4-turn-off-screen"></a>

Turn off Codey's screen.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/4-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/4-2.png)

Press Button A, the image will be displayed at the origin. One second later, the screen will turn off.

### 5. show \(\) <a id="5-show-"></a>

Display English characters, numbers and symbols on Codey's screen.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/5-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/5-2.png)

Press Button A, Codey's screen will display "12:00".

### 6. show \(\) until scroll done <a id="6-show--until-scroll-done"></a>

Display English characters, numbers and symbols on Codey's screen, and scroll all contents.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/6-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/6-2.png)

Press Button A, Codey's screen will scroll "morning".

### 7. show \(\) at x:\(\) y:\(\) <a id="7-show--at-x-y"></a>

Display English characters, numbers and symbols at specified point of the face panel.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/7-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/7-2.png)

Press Button A, Codey's screen will display "hi" at the origin.

### 8. light up x:\(\) y:\(\) <a id="8-light-up-x-y"></a>

Light up specified dot \(x, y\) of Codey's face panel.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/8-1.png)

**Parameters:**

* x: 0 ~ 15
* y: 0 ~ 7

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/8-2.png)

Press Button A, the dot at \(3, 3\) will light up.

### 9. light off x:\(\) y:\(\) <a id="9-light-off-x-y"></a>

Light off specified dot \(x, y\) of Codey's face panel.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/9-1.png)

**Parameters:**

* x: 0 ~ 15
* y: 0 ~ 7

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/9-2.png)

Press Button A, the dot at \(2, 2\) will light up, and light off after one second.

### 10. switch between light-up and light-off x:\(\) y:\(\) <a id="10-switch-between-light-up-and-light-off-x-y"></a>

Change the status of specified dot \(x, y\) of Codey's face panel: light off light-up dot; light up light-off dot.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/10-1.png)

**Parameters:**

* x: 0 ~ 15
* y: 0 ~ 7

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/10-2.png)

Press Button A, the dot at \(6, 6\) will light up. Press Button A again, the dot will light off.

### 11. x:\(\) y:\(\) is it lighted up? <a id="11-x-y-is-it-lighted-up"></a>

If specified dot \(x, y\) of Codey's face panel is lighted up, the report condition is met.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/11-1.png)

**Parameters:**

* x: 0 ~ 15
* y: 0 ~ 7

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/11-2.png)

Press Button A, the dot \(3, 3\) and \(5, 5\) of Codey's face panel will light up. After 3 seconds, the dot \(3, 3\) will light off.


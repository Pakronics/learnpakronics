# Sensing

**1. light sensor \(on-board\) light intensity**

Reports light intensity by the specified light sensor.

![](../../.gitbook/assets/0%20%287%29.png)

**Example:**

![](../../.gitbook/assets/1%20%2814%29.png)

When the space key is pressed, the light intensity value will be displayed on the external LED panel.

**2. ultrasonic sensor \(port3\) distance cm**

Reports the distance of obstacles detected by the ultrasonic sensor that is connected to the specified port.

![](../../.gitbook/assets/2%20%2810%29.png)

**Example:**

![](../../.gitbook/assets/3%20%286%29.png)

When the space key is pressed, the distance of obstacles detected by the ultrasonic sensor will be displayed on the external LED panel.

**3. line follower sensor \(port2\) value**

Reports the value detected by the specified line follower sensor.

![](../../.gitbook/assets/4%20%286%29.png)

**Example:**

![](../../.gitbook/assets/5%20%286%29.png)

When the space key is pressed, the value detected by the line follower sensor will be displayed on the external LED panel.

**4. line follower sensor \(port2\) detects \(leftside\) being\(black\)?**

If the color detected by the specified line follower sensor on the specified side is the specified color, the report condition is met.

![](../../.gitbook/assets/6%20%286%29.png)

**Example:**

![](../../.gitbook/assets/7%20%285%29.png)

When the green flag is clicked, if the line follower sensor detects black obstacles on the left side, mBot will stop moving.

**5. when on-board button \(pressed\)?**

If the on-board button is pressed or released, the report condition is met.

![](../../.gitbook/assets/8%20%289%29.png)

**Example:**

![](../../.gitbook/assets/9%20%281%29.png)

When the green flag is clicked, if the on-board button is pressed, the LEDs of mBot will light up red.

**6. IR remote \(A\) pressed?**

If the specified button of the IR remote is pressed, the report condition is met.

![](../../.gitbook/assets/10.png)

**Example:**

![](../../.gitbook/assets/11%20%286%29.png)

When the green flag is clicked, if button A of the IR remote is pressed, "yes" will be displayed on the external LED panel.

**7. send IR message \(hello\)**

Sends the specified IR message.

![](../../.gitbook/assets/12%20%285%29.png)

**Example:**

![](../../.gitbook/assets/13%20%284%29.png)

When the space key is pressed, IR message "hello" will be sent out.

**8. IR message received**

Reports the received IR message.

![](../../.gitbook/assets/14%20%282%29.png)

**Example:**

![](../../.gitbook/assets/15.png)

When the space key is pressed, the IR message received will be displayed on the external LED panel.

**9. timer**

Reports the value of the timer.

![](../../.gitbook/assets/16%20%282%29.png)

**Example:**

![](../../.gitbook/assets/17.png)

When the space key is pressed, the value of the timer will be displayed on the external LED panel.

**10. reset timer**

Resets the timer.

![](../../.gitbook/assets/18.png)

**Example:**

![](../../.gitbook/assets/19.png)

When the space key is pressed, the timer will be reset.


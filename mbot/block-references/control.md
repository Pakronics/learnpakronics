# Control

**1. wait \(\) seconds**

Waits for a specified period of time to run the script.

![](../../.gitbook/assets/0%20%2815%29.png)

**Example:**

![](../../.gitbook/assets/1%20%283%29.png)

When the space key is pressed, all LEDs will light up red, and 1 second later, switch to yellow.

**2. repeat \(\)**

Runs the script for the specified number of times.

![](../../.gitbook/assets/2%20%2816%29.png)

**Example:**

![](../../.gitbook/assets/3%20%2817%29.png)

When the space key is pressed, all LEDs will switch between red and yellow for 10 times.

**3. forever**

Runs the script repeatedly.

![](../../.gitbook/assets/4%20%2818%29.png)

**Example:**

![](../../.gitbook/assets/5%20%2813%29.png)

When the space key is pressed, all LEDs will switch between red and yellow.

**4. if \(\) then \(\)**

If the report condition is met, run the script.

![](../../.gitbook/assets/6%20%289%29.png)

**Example:**

![](../../.gitbook/assets/7%20%281%29.png)

When the green flag is clicked, if the on-board button is pressed, all LEDs will light up red.

**5. if \(\) then \(\) else \(\)**

If the report condition is met, run script 1. If not, run script 2.

![](../../.gitbook/assets/8.png)

**Example:**

![](../../.gitbook/assets/9%20%2811%29.png)

When the space key is pressed, if the on-board button is pressed, all LEDs will light up red, else, green.

**6. wait \(\)**

Wait until the report condition is met. Then run the script.

![](../../.gitbook/assets/10%20%287%29.png)

**Example:**

![](../../.gitbook/assets/11.png)

When the green flag is clicked, if the on-board button is pressed, all LEDs will light up red.

**7. repeat until \(\)**

Run the script repeatedly until the report condition is met.

![](../../.gitbook/assets/12%20%281%29.png)

**Example:**

![](../../.gitbook/assets/13%20%281%29.png)

When the green flag is clicked, all LEDs will light up red until the on-board button is pressed.

**8. stop \(\)**

Stop the specified script or scripts. There are three options: all, this script, or other scripts in sprite.

![](../../.gitbook/assets/14%20%284%29.png)

**Example:**

![](../../.gitbook/assets/15%20%282%29.png)

When the space key is pressed, all scripts will stop.


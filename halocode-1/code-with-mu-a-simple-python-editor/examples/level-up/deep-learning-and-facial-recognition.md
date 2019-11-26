# Deep Learning and Facial Recognition

Use the Machine Learning extension to achieve facial recognition function. When "woman" is recognized, the message "laugh" will be broadcast, and HaloCode will make a smiling face with its LED ring; otherwise, the message "angry" will be broadcast, and the LED ring of HaloCode will light up red. You can apply facial recognition to your smart-home system.

![](../../../../.gitbook/assets/0%20%2821%29.png)

**Training model**

1. Under "Sprites", click "+" in the Blocks area to add "Teachable Machine" extension.

![](../../../../.gitbook/assets/1.gif)

2. Select Teachable Machine blocks, and click "Training model" to build a new model. In this example, we'll need 3 categories.

![](../../../../.gitbook/assets/2%20%289%29.gif)

3. Name the first category "woman". Print a photo of a woman, and place the photo in front of the camera. Click and hold the button "Learn", so that enough samples will be collected. \(Change the angle of the photo to collect different samples; more samples come with better recognition result.\)

![](../../../../.gitbook/assets/3%20%285%29.gif)

4. Likewise, we can collect samples for category "man" and "student".

![](../../../../.gitbook/assets/4%20%286%29.gif)

5. When the sample collecting process is done, click "Use the model".

![](../../../../.gitbook/assets/5%20%284%29.gif)

**Add event and control**

6. Drag an Events block when green flag clicked and a Control block if \(\) then \(\). Then add a Teachable Machine \(TM\) block recognition result is \(woman\).

![](../../../../.gitbook/assets/6%20%2812%29.gif)

**Create broadcast messages**

7. Click Events blocks, and create two messages, "laugh" and "angry".

![](../../../../.gitbook/assets/7%20%2812%29.gif)

8. Add an Events block broadcast \(laugh\) and wait. \(HaloCode will execute the script that is activated by the message "laugh", and then others.\)

![](../../../../.gitbook/assets/8%20%283%29.gif)

9. Likewise, for "man" and "student", add corresponding Events block broadcast \(\) and wait. Add a Control block forever to keep facial recognition function on.

![](../../../../.gitbook/assets/9%20%288%29.gif)

**Program HaloCode**

10. Under "Devices", choose "HaloCode". Add an Events block when I receive\(\) and two Lighting blocks light up LED \(\) with color R\(\) G\(\) B\(\) to light up the second and tenth LED, as the "eyes" of the smiling face.

![](../../../../.gitbook/assets/10%20%282%29.gif)

11. Add 5 more Lighting blocks light up LED \(\) with color R\(\) G\(\) B\(\) to light up the fourth to eighth LED as the "mouth". Adjust the RGB values to set the color to light pink.

![](../../../../.gitbook/assets/11%20%281%29.gif)

12. Add a Control block wait \(0.1\) seconds and a Lighting block light off all LEDs.

![](../../../../.gitbook/assets/12%20%281%29.gif)

13. Add an Events block when I receive \(angry\) and a Lighting block all LEDs light up \(\). Set the color to red. 0.1 second later, light off all LEDs.

![](../../../../.gitbook/assets/13%20%284%29.gif)

**Programming result**

![](../../../../.gitbook/assets/14%20%283%29.gif)


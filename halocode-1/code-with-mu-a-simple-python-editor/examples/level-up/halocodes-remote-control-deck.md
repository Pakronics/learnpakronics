# HaloCode's Remote Control Deck

**Sign in to mBlock 5**

We can use "User Cloud Message" to control HaloCode remotely. We need to sign in to mBlock 5 first.

![](../../../../.gitbook/assets/0%20%286%29.gif)

**Toggle on Upload mode**

![](../../../../.gitbook/assets/1%20%286%29.gif)

**Connect to the internet**

1. Drag an Events block when HaloCode starts up and a Wi-Fi block connect to Wi-Fi \(\) password \(\). Input the Wi-Fi name and password.

![](../../../../.gitbook/assets/2%20%288%29.gif)

2. We want to know when the Wi-Fi is successfully connected. Add a Control block wait \(\), a Wi-Fi block Wi-Fi is connected?, and a Lighting block all LEDs light up \(\).

![](../../../../.gitbook/assets/3%20%2814%29.gif)

**Add a sprite**

3. Under "Sprites", click "+". From the pop-up Sprite Library window, choose "Balloon1" from the Props category.

![](../../../../.gitbook/assets/4%20%284%29.gif)

4. Right click "Balloon1" to make a duplicate. Change the costume to "c", namely color purple.

![](../../../../.gitbook/assets/5%20%289%29.gif)

5. Delete default sprite "Panda".

![](../../../../.gitbook/assets/6%20%284%29.gif)

**Program the sprite**

6. Click "+" in the Blocks area to add "User Cloud Message".

![](../../../../.gitbook/assets/7%20%2810%29.gif)

7. Program the blue balloon. Add an Events block when this sprite clicked and a User Cloud Message block send user cloud message \(\). Name the message "blue".

![](../../../../.gitbook/assets/8%20%286%29.gif)

**Add some special effects to the balloon**

8. When the balloon is clicked, we want it to appear like being clicked. When clicked, the balloon gets brighter and bigger, and goes back to original color and size in 0.3 second. Add the following blocks: change size by \(\), change \(color\) effect by \(\), wait \(\) seconds, set size to \(100\)%, set \(color\) effect to \(0\).

![](../../../../.gitbook/assets/9%20%284%29.gif)

9. Likewise, we can program the purple balloon. Add an Events block when this sprite clicked and a User Cloud Message block send user cloud message \(\). Name the message "purple". Apply the same special effects.

![](../../../../.gitbook/assets/10%20%281%29.png)

**HaloCode receives user cloud message**

10. Under "Devices", select "HaloCode".

11. Add a Wi-Fi block when receiving user cloud message \(\) and input message "blue".

![](../../../../.gitbook/assets/11%20%287%29.gif)

**Set HaloCode's LEDs**

12. Add a Lighting block all LEDs light up \(\), change the color to blue. Add a Control block wait \(\) seconds and another Lighting block light off all LEDs.

![](../../../../.gitbook/assets/12%20%286%29.gif)

13. Likewise, for receiving the "purple" message, duplicate the script, and change LED color to purple.

![](../../../../.gitbook/assets/13%20%286%29.gif)

**Programming result**

14. Upload the program to HaloCode. Disconnect HaloCode from the PC, and use a battery box to power HaloCode. Click the balloons on stage, and check the LEDs of HaloCode.

![](../../../../.gitbook/assets/14%20%281%29.gif)

![](../../../../.gitbook/assets/15.gif)


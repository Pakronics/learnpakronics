# User Cloud Message

User Cloud Message syncs your data across devices with your mBlock 5 account. As long as your HaloCode is connected to the internet, you can program it remotely.

**Sign UP / Sign In to mBlock 5**

Click the sign in/sign up icon at the tool bar, and then follow the instructions to finish signing up or signing in.

![](../.gitbook/assets/0.gif)

**Toggle on Upload mode**

Click to toggle on Upload mode.

![](../.gitbook/assets/1%20%2814%29.gif)

**Use Stage Button to Control HaloCode Remotely**

We will create a new project combined with Scratch Stage Programming. Use the button on stage to control HaloCode remotely.

**Add User Cloud Message Blocks**

Under "Sprites", click "+" in the Blocks area. The Extension Center page will pop up. Click "Add" to add User Cloud Message blocks.

![](../.gitbook/assets/2%20%2812%29.gif)

**Step One: Program Stage Button**

1. Under "Sprites", click "×" to delete "Panda" \(the default sprite\).

![](../.gitbook/assets/3%20%2816%29.gif)

2. Click "+" to add a new sprite. From the pop-up Sprite Library page, search and choose "Empty Button1". Click "OK".

![](../.gitbook/assets/4%20%281%29.gif)

3. Choose "Empty Button1", and drag an Events block when this sprite clicked to the Scripts area.

![](../.gitbook/assets/5%20%286%29.gif)

4. Add a User Cloud Message block send user cloud message \(\) and name the message "light\_on".

![](../.gitbook/assets/6%20%287%29.gif)

5. Let's add some special effects to the button. Add a Motion block change y by \(\) and set the value to "-2". Add a Looks block set color effect to \(\) and set the value to "-10".

![](../.gitbook/assets/7%20%284%29.gif)

6. Add a Control block wait \(\) seconds and input "0.2". Drag another Motion block change y by \(\) and set the value to "-2". Then add another Looks block set color effect to \(\).

![](../.gitbook/assets/8%20%289%29.gif)

**Step Two: Program HaloCode**

**Connect to the Internet**

1. Under "Devices", make sure "HaloCode" is selected. Drag an Events block when HaloCode starts up to the Scripts area. Add a Wi-Fi block connect to Wi-Fi \(\) password \(\). Input Wi-Fi SSID \(Wi-Fi name\) and password.

![](../.gitbook/assets/9%20%289%29.gif)

2. To ensure Wi-Fi is successfully connected, we need to add a Control block wait \(\) and a Wi-Fi block Wi-Fi is connected?. We want to know when Wi-Fi is connected, so let's add a Lighting block all LEDs light up \(\) to make the LED ring lights up green.

![](../.gitbook/assets/10%20%283%29.gif)

**Cloud Message Script**

When HaloCode receives the user cloud message "light\_on", we want the LED ring to light up red and then go off.

1. Drag a Wi-Fi block when receiving user cloud message \(\) and input "light\_on". Add a Lighting block all LEDs light up \(\) and set the color to red.

![](../.gitbook/assets/11%20%284%29.gif)

3. Add a Control block wait \(\) seconds and a Lighting block light off all LEDs.

![](../.gitbook/assets/12.gif)

4. Click "Upload" to upload the program to HaloCode.

![](../.gitbook/assets/13%20%282%29.gif)

5. Try clicking "Empty Button1" on the stage!

As long as HaloCode is connected to the internet, you can sign in to mBlock 5 in another computer and open the same project to control HaloCode remotely.


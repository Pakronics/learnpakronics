# Control HaloCode's LEDs via Voice Command

**Sign in to mBlock 5**

HaloCode needs to connect to the internet to use online speech recognition service. We need to sign in to mBlock 5 first.

![](<../../../../.gitbook/assets/0 (5).gif>)

**Connect to the internet**

1\. Drag an Events block when HaloCode starts up and a Wi-Fi block connect to Wi-Fi () password (). Input the Wi-Fi name and password.

![](<../../../../.gitbook/assets/1 (3).gif>)

2\. We want to know when the Wi-Fi is successfully connected. Add a Control block wait (), a Wi-Fi block Wi-Fi is connected?, and a Lighting block show ().

![](<../../../../.gitbook/assets/2 (14).gif>)

**Speech recognition**

When the button is pressed, all LEDs will light up orange. The recognition process lasts for 2 seconds. When it's done, LED 1 will light up green.

3\. Add an Events blocks when button is pressed and a Lighting block all LEDs light up (). Change the color to orange. Then add a Control block wait (1) seconds and a Lighting block show ().

![](<../../../../.gitbook/assets/3 (7).gif>)

4\. Add a Wi-Fi block recognize (English) for (2) seconds, and a Lighting block light off all LEDs to light off all LEDs after the speech recognition is done.

![](<../../../../.gitbook/assets/4 (13).gif>)

**Recognize "blue"**

5\. Add a Control block if () then () else and an Operators block () contains ()?. Add Wi-Fi block speech recognition result to the first box and input "blue" to the second box. If the speech recognition result contains "blue", all LEDs will light up blue. Add a Lighting block all LEDs light up ()

![](<../../../../.gitbook/assets/5 (11).gif>)

**Recognize "red"**

6\. Likewise, we can recognize "red".

![](<../../../../.gitbook/assets/6 (12).gif>)

7\. Upload the program. When HaloCode connects to the internet successfully, try pressing the button and say "red" to the microphone. Then check the LEDs.

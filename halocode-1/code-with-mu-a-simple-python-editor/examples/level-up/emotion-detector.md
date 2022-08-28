# Emotion Detector

When a happy face is detected, the LED ring of HaloCode will light up, and make a smiling face.

![](<../../../../.gitbook/assets/0 (7).png>)

**Add a sprite**

1\. Delete default sprite Panda

![](<../../../../.gitbook/assets/1 (8).gif>)

2\. Add a new sprite, Empty button14

![](<../../../../.gitbook/assets/2 (1).gif>)

3\. Change the color, and size of the button.

![](<../../../../.gitbook/assets/3 (2).gif>)

4\. In the Blocks Area, click "+ extension" to add Cognitive Services (AI) blocks

![](../../../../.gitbook/assets/4.gif)

5\. Drag an Events block when this sprite clicked to the Scripts Area. Add an AI block recognize emotion after (1) seconds

![](<../../../../.gitbook/assets/5 (2).gif>)

6\. Add a Control block ig () then (), an AI block emotion is (happiness)?, and an Events block broadcast (). Create a new piece of message named "laugh"

![](<../../../../.gitbook/assets/6 (5).gif>)

7\. Check the box of AI block happiness value () to display the value on stage

![](../../../../.gitbook/assets/7.gif)

**HaloCode makes a smiling face**

8\. Add an Events block 当when I receive (laugh), and a Lighting block show (). Draw a smiling face

![](<../../../../.gitbook/assets/8 (4).gif>)

9\. Add a Control block wait (2) seconds, and a Lighting block light off all LEDs

![](<../../../../.gitbook/assets/9 (7).gif>)

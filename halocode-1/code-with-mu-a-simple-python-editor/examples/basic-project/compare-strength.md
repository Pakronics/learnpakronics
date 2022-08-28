# Compare Strength

****

**Programming Result**

![](<../../../../.gitbook/assets/0 (3).gif>)

**Introduction to HaloCode's motion sensor**

The motion sensor detects how HaloCode moves, including shaking strength.

![](<../../../../.gitbook/assets/1 (6).png>)

**Set the range of shaking strength**

1\. Drag an Operators block () > () to the Scripts area, and change the value of the second parameter to "30". Add a Sensing block shaking strength to the first parameter.

![](<../../../../.gitbook/assets/2 (7).gif>)

2\. Add a Control block if () then ().

![](<../../../../.gitbook/assets/3 (9).gif>)

**Set LED animation**

3\. Add a Lighting block all LEDs light up (), and a Control block wait () seconds. Add another Lighting block light off all LEDs to light off all LEDs in 1 second.

![](<../../../../.gitbook/assets/4 (3).gif>)

4\. Likewise, for shaking strength greater than 60, we can duplicate the script. Change the value to 60 and LED color to red.

![](../../../../.gitbook/assets/5.gif)

**Add event and control**

5\. Add an Events block when HaloCode is shaking and a Control block forever.

![](<../../../../.gitbook/assets/6 (3).gif>)

**Read shaking strength**

6\. Check the box for Sensing block shaking strength.

![](<../../../../.gitbook/assets/7 (5).gif>)

7\. Shake HaloCode! See if you can make the LED ring light up red.

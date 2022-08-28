# Energy Ring

Shake your hand to power HaloCode. As HaloCode is "charging", more LEDs will light up

![](<../../../../.gitbook/assets/0 (13).png>)

1\. Choose Variables block, and click "Make a Variable". Name the variable "n"

![](<../../../../.gitbook/assets/1 (12).gif>)

2\. Add an Events block when button is pressed, a Lighting block light off LED (), and a Variables block set (n) to (). Input "1"

![](<../../../../.gitbook/assets/2 (5).gif>)

3\. Add a Control block if () then (), an Operators block () > (), and a Sensing block shaking strength. Input "20"

![](<../../../../.gitbook/assets/3 (11).gif>)

4\. Add a Lighting block light up LED () with color R()G()B(), two Variables block n and change (n) by (1), a Control block wait () secs. Input "0.2"

![](<../../../../.gitbook/assets/4 (1).gif>)

5\. Add a Control block repeat until (), an Operators block () = (), a Variables block n. Input "12"

![](<../../../../.gitbook/assets/5 (9).gif>)

6\. Add a Lighting block all LEDs light up (). Set the color to blue

![](<../../../../.gitbook/assets/6 (6).gif>)

7\. Toggle on Upload mode.

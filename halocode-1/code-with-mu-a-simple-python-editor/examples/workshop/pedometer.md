# Pedometer

![](<../../../../.gitbook/assets/0 (8).png>)

**Program HaloCode**

1\. Create 3 pieces of message: "start", "move", and "stop"

![](<../../../../.gitbook/assets/1 (13).gif>)

2\. Add an Events block when button is pressed , a Control block repeat, another Events block broadcast (start), and a Sensing block reset timer

![](<../../../../.gitbook/assets/2 (15).gif>)

3\. Add a Control block if () else (), an Operators block () > (), a Sensing block shaking strength, and an Events block broadcast (move). Input "15" to the second box of the Operators block

![](<../../../../.gitbook/assets/3 (3).gif>)

4\. Add a Control block if () then (), an Operators block () = (), a Sensing block shaking strength, and an Events block broadcast (stop)

![](<../../../../.gitbook/assets/4 (9).gif>)

5\. Add a Control block repeat until (), an Operators block () > (), and a Sensing block timer. Input "100" to the second box of the Operators block, and combine the two scripts

![](<../../../../.gitbook/assets/5 (6).gif>)

**Add a sprite**

6\. Delete default sprite Panda

![](<../../../../.gitbook/assets/6 (8).gif>)

7\. Add sprite "Empty"

![](<../../../../.gitbook/assets/7 (9).gif>)

8\. Choose "Empty", and then click "Costume". Draw a red dot

![](<../../../../.gitbook/assets/8 (8).gif>)

9\. Duplicate "Empty", and then change the costume to make a blue dot

![](<../../../../.gitbook/assets/9 (8).gif>)

10\. At the bottom of the Blocks Area, click "+ extension" to add Pen

![](<../../../../.gitbook/assets/10 (1).gif>)

**Program the red dot**

11\. Make sure the red dot is selected, and then click Variables blocks. Create a new variable "motion value"

![](<../../../../.gitbook/assets/11 (5).gif>)

12\. Add an Events block when I receive (move), and a Control block repeat () times. Input "4"

![](<../../../../.gitbook/assets/12 (1).gif>)

13\. Add a Motion block turn ↷ () degrees , and a Pen block stamp, and a Variables block change (Motion value) by (1)

![](../../../../.gitbook/assets/13.gif)

14\. Add an Events block when I receive (start), and a Motion block point in direct (90)

![](<../../../../.gitbook/assets/14 (2).gif>)

**Program the blue dot**

15\. Make sure the red dot is selected, and then click Variables blocks. Create a new variable "Slitting value"

![](<../../../../.gitbook/assets/15 (2).gif>)

16\. Add an Events block when I receive (stop), and a Control block repeat () times. Input "2"

![](<../../../../.gitbook/assets/16 (2).gif>)

17\. Add a Motion block turn ↷ () degrees , and a Pen block stamp, and a Variables block change (Slitting value) by (1)

![](<../../../../.gitbook/assets/17 (1).gif>)

18\. Add an Events block when I receive (start), and a Motion block point in direct (90)

![](<../../../../.gitbook/assets/18 (1).gif>)

# Use Global Variable to Interact with Sprites

**Programming result**

When you rotate HaloCode around the y-axis, the sun on stage will rotate as well.

**Introduction to HaloCode's Axes**

The axes of HaloCode are as follows:

![](<../../../../.gitbook/assets/0 (3).png>)

**Create a new variable**

1\. Click Variables category, and then click "Make a Variable". Name the variable "y".

![](<../../../../.gitbook/assets/1 (16).gif>)

2\. Add a Variables block set (y) to () and a Sensing block rotation angle around (). Choose "Y" axis.

![](<../../../../.gitbook/assets/2 (4).gif>)

**Add event and control**

3\. Add an Events block when button is pressed and a Control block forever.

![](<../../../../.gitbook/assets/3 (13).gif>)

**Add a sprite**

4\. Under "Sprites", click "+". Choose "Sun1".

![](<../../../../.gitbook/assets/4 (8).gif>)

5\. Delete default sprite "Panda".

![](<../../../../.gitbook/assets/5 (10).gif>)

**Program the sun**

6\. Add a Motion block turn ↷ () degrees and a Variables block y.

![](<../../../../.gitbook/assets/6 (10).gif>)

7\. Add an Events block when green flag clicked and a Control block forever.

![](<../../../../.gitbook/assets/7 (2).gif>)

8\. Rotate HaloCode and see what happens.

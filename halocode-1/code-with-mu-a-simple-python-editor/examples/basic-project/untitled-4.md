# Control Multiple HaloCodes via LAN

Multiple HaloCodes can join the same LAN (Local Area Network), and communicate with each other. We can use HaloCode to control others.

![](<../../../../.gitbook/assets/0 (15).png>)

## Control HaloCode B with HaloCode A

### HaloCode A sets up LAN

1\. Connect HaloCode A

![](<../../../../.gitbook/assets/1 (4).gif>)

2\. Enable Upload mode

![](<../../../../.gitbook/assets/2 (6).gif>)

3\. Add an Events block when HaloCode starts up, and a LAN block set up LAN named (mesh1)。

![](<../../../../.gitbook/assets/3 (12).gif>)

### HaloCode A broadcasts on LAN

4\. Add an Events block when button is pressed, and a LAN block broadcast () on LAN. Name the message "light"

![](<../../../../.gitbook/assets/4 (7).gif>)

5\. Upload the program to HaloCode A

![](<../../../../.gitbook/assets/5 (4).gif>)

### HaloCode B joins LAN

6\. Connect HaloCode B

![](<../../../../.gitbook/assets/6 (7).gif>)

7\. Enable Upload mode

![](<../../../../.gitbook/assets/7 (12).gif>)

8\. Add an Events block when HaloCode starts up, and LAN block join LAN named (mesh1)

![](../../../../.gitbook/assets/8.gif)

### HaloCode B receives LAN broadcast

9\. Add a LAN block when receiving LAN broadcast (), and input "light". Add a Lighting block all LEDs light up (), a Control block wait () seconds, and another Lighting block light off all LEDs

![](<../../../../.gitbook/assets/9 (6).gif>)

10\. Upload the program to HaloCode B

![](<../../../../.gitbook/assets/10 (4).gif>)

### Programming result

11\. Press the button HaloCode A

![](../../../../.gitbook/assets/11.gif)

**Challenge**

Challenge yourself. Can you make a new project like following example?

![](<../../../../.gitbook/assets/12 (6).gif>)

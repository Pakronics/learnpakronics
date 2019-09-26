# Make HaloCode the Steering Wheel of the Car on Stage

**Programming Result**

When you tilt HaloCode to the left, the car on stage will move leftward. When you tilt HaloCode to the right, the car will move rightward. HaloCode is just like the steering wheel of the car.

![](../../../../.gitbook/assets/0%20%283%29.gif)

**Use the motion sensor**

The motion sensor of HaloCode detects how HaloCode moves. We'll use the motion sensor in this example. When HaloCode is tilted to the left, a corresponding piece of message will be sent to the car on Scratch Stage to make it move leftward. Likewise, when HaloCode is tilted to the right, a corresponding piece of message will tell the car to move rightward.

1. Drag a Control block if \(\) then \(\) to the Scripts area. Add a Sensing block HaloCode is \(\)? to the condition.

![](../../../../.gitbook/assets/1%20%2811%29.gif)

2. Likewise, for the right side, duplicate the script, and select "right-tilted".

![](../../../../.gitbook/assets/2%20%2810%29.gif)

**Message broadcast**

3. Add two Events blocks broadcast \(\). Create two pieces of message, namely "left" and "right".

![](../../../../.gitbook/assets/3%20%2813%29.gif)

4. Add an Events block when button is pressed and a Control block forever.

**Add a sprite**

5. Under "Sprites", click "+". In the Sprites Library, choose "Car" from the Transportation category.

6. Delete the default sprite "Panda".

**Program the car**

7. Add three Motion block: set rotation style \(left-right\), point in direction \(-90\), move \(10\) steps.

8. Add an Events block when I receive \(\), and choose message "left". When the car receives message "left", it will move leftward for 10 steps.

10. Likewise, for the rightward part, duplicate the script. Choose message "right", and change the direction to "90".

**Note: the message received should be the same message that is broadcast.**

![](../../../../.gitbook/assets/4%20%282%29.gif)

11. Press the button of HaloCode and then tilt it!


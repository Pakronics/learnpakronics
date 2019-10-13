# Pedometer

![](../../../../.gitbook/assets/0%20%2825%29.png)

**Program HaloCode**

1. Create 3 pieces of message: "start", "move", and "stop"

![](../../../../.gitbook/assets/1%20%2812%29.gif)

2. Add an Events block when button is pressed , a Control block repeat, another Events block broadcast \(start\), and a Sensing block reset timer

![](../../../../.gitbook/assets/2%20%286%29.gif)

3. Add a Control block if \(\) else \(\), an Operators block \(\) &gt; \(\), a Sensing block shaking strength, and an Events block broadcast \(move\). Input "15" to the second box of the Operators block

![](../../../../.gitbook/assets/3.gif)

4. Add a Control block if \(\) then \(\), an Operators block \(\) = \(\), a Sensing block shaking strength, and an Events block broadcast \(stop\)

![](../../../../.gitbook/assets/4%20%288%29.gif)

5. Add a Control block repeat until \(\), an Operators block \(\) &gt; \(\), and a Sensing block timer. Input "100" to the second box of the Operators block, and combine the two scripts

![](../../../../.gitbook/assets/5%20%2812%29.gif)

**Add a sprite**

6. Delete default sprite Panda

![](../../../../.gitbook/assets/6%20%289%29.gif)

7. Add sprite "Empty"

![](../../../../.gitbook/assets/7%20%283%29.gif)

8. Choose "Empty", and then click "Costume". Draw a red dot

![](../../../../.gitbook/assets/8%20%2810%29.gif)

9. Duplicate "Empty", and then change the costume to make a blue dot

![](../../../../.gitbook/assets/9%20%282%29.gif)

10. At the bottom of the Blocks Area, click "+ extension" to add Pen

![](../../../../.gitbook/assets/10%20%284%29.gif)

**Program the red dot**

11. Make sure the red dot is selected, and then click Variables blocks. Create a new variable "motion value"

![](../../../../.gitbook/assets/11%20%288%29.gif)

12. Add an Events block when I receive \(move\), and a Control block repeat \(\) times. Input "4"

![](../../../../.gitbook/assets/12%20%283%29.gif)

13. Add a Motion block turn ↷ \(\) degrees , and a Pen block stamp, and a Variables block change \(Motion value\) by \(1\)

![](../../../../.gitbook/assets/13%20%281%29.gif)

14. Add an Events block when I receive \(start\), and a Motion block point in direct \(90\)

![](../../../../.gitbook/assets/14%20%282%29.gif)

**Program the blue dot**

15. Make sure the red dot is selected, and then click Variables blocks. Create a new variable "Slitting value"

![](../../../../.gitbook/assets/15%20%283%29.gif)

16. Add an Events block when I receive \(stop\), and a Control block repeat \(\) times. Input "2"

![](../../../../.gitbook/assets/16%20%281%29.gif)

17. Add a Motion block turn ↷ \(\) degrees , and a Pen block stamp, and a Variables block change \(Slitting value\) by \(1\)

![](../../../../.gitbook/assets/17.gif)

18. Add an Events block when I receive \(start\), and a Motion block point in direct \(90\)

![](../../../../.gitbook/assets/18.gif)


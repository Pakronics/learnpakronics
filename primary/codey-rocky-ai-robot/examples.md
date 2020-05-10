# Examples

![](http://docs.makeblock.com/codeyrocky/en/examples/codey-rocky-product-image.jpg)

## Codey Rocky Projects <a id="codey-rocky-projects"></a>

### 1. Change Codey's Emotions with Buttons <a id=" 1. Change Codey&apos;s Emotions with Buttons"></a>

1\) Drag a when button \(\) is pressed block from the Events category to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-1-1.png)

2\) Drag a play sound \(\) block from the Speaker category.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-1-2.png)

3\) Drag a show image \(\) block from the Looks category.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-1-3.png)

4\) Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/examples/upload.png)

5\) Press Button A to see how Codey looks!

### 2. Use Codey to Create LED Animations <a id=" 2. Use Codey to Create LED Animations"></a>

1\) Drag a when Codey is shaking block from the Events category to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-1.png)

2\) Drag a show image \(\) for \(\) secs block from the Looks category, and draw the following image. Reset the time to 0.3.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-3.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-2.png)

3\) Add a show image \(\) for \(\) secs block from the Looks category, and draw the following image. Reset the time to 0.3.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-4.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-5.png)

4\) Add another show image \(\) for \(\) secs block from the Looks category, and draw the following image. Reset the time to 0.3.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-6.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-7.png)

5\) Add a Control block repeat \(\) to wrap up the three show image \(\) for \(\) secs blocks. Reset the number to 6.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-8.png)

6\) Drag a play sound \(\) block from the Speaker category to add some sound effects. Set the sound as "jump".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-10.png)

7\) Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/examples/upload.png)

8\) Try shaking Codey to see the rabbit jumping!

![](http://docs.makeblock.com/codeyrocky/en/examples/project-2-9.png)

### 3. Turn Codey into a Musician <a id=" 3. Turn Codey into a Musician"></a>

1\) Drag an Event block when button \(\) is pressed to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-3-1.png)

2\) Add four play note \(\) for \(\) beats blocks from the Speaker category. Set the corresponding note as C4, E4, F4, and A5.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-3-2.png)

**Volume Control Script**

3\) Drag a when Codey starts up block from the Events category.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-3-3.png)

4\) Add a Speaker block set volume to \(\)% and a Sensing block gear potentiometer value, so that we can adjust the gear to change volume.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-3-4.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-3-5.png)

5\) Add a Control block forever, so we are able to adjust the sound volume all the time.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-3-6.png)

6\) Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/examples/upload.png)

7\) Press Button A to see how Codey plays music!

### 4. Make Codey Blink Eyes <a id=" 4. Make Codey Blink Eyes"></a>

1\) Drag an Event block when Codey starts up to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-1.png)

2\) Add a Looks block show image \(\) for \(\) secs. Add an Operators block pick random \(\) to \(\) to make Codey blink eyes randomly. Set the number as 2 and 5.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-4.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-2.png)

3\) Add another Looks block show image \(\) for \(\) secs. Draw the following image, and set the time as 0.2.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-5.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-3.png)

4\) Drag a Control block forever to wrap up the two show image \(\) for \(\) secs blocks, so Codey will keep blinking eyes.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-6.png)

5\) Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/examples/upload.png)

6\) Check Codey to see it blink eyes!

### 5. Make Codey Rocky Identify Colors <a id="5-make-codey-rocky-identify-colors"></a>

1\) Drag an Event block when Codey starts up to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-1.png)

2\) Add a Control block if \(\) then \(\), and a Sensing block the color detected is \(\)?.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-1.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-2.png)

3\) Add a Lighting block RGB LED lights up \(\) to make the LED lights up red when the color detected is red. Drag a play sound \(\) block and change the sound to "score" to add some sound effects.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-3.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-4.png)

4\) We want Codey Rocky to detect color blue. Right click to duplicate the blocks. Change the color to blue.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-5.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-6.png)

5\) Add a Control block forever to create a loop.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-7.png)

6\) Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/examples/upload.png)

7\) Have a try!

**Note: keep the IR sensor face-down.**

![](http://docs.makeblock.com/codeyrocky/en/examples/project-5-8.png)

### 6. Make Codey Rocky Avoid Obstacles <a id="6-make-codey-rocky-avoid-obstacles"></a>

1\) Drag an Event block when Codey starts up to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-1.png)

2\) Add a Looks block show image \(\).

![](http://docs.makeblock.com/codeyrocky/en/examples/project-6-1.png)

3\) Drag an Action block \(\) at power \(\)%, a Control block wait until \(\), and a Sensing block obstacles ahead?. Keep all default values.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-6-2.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-6-3.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-6-4.png)

4\) When Codey Rocky detects obstacles ahead, we want it to avoid them by moving backward and turning right, so we need to add three Action blocks: stop moving, move backward at power \(\)% for \(\) secs, and turn right at power \(\)% for \(\) secs.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-6-5.png)

5\) Add a Control block forever to make Codey Rocky keep avoiding obstacles.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-6-6.png)

6\) Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/examples/upload.png)

7\) Check how Codey Rocky manages to stay away from obstacles.

**Note: adjust the IR sensor to face-forward.**

### 7. Use Codey to Make Sprites Play Instruments <a id="7-use-codey-to-make-sprites-play-instruments"></a>

This project combines stage programming with Codey.

Before we start, please toggle to disable **Upload Mode**.

![](http://docs.makeblock.com/codeyrocky/en/examples/disable-upload-mode.png)

1\) Drag an Events block when button \(\) is pressed.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-1.png)

2\) When Button A is pressed, we want the sprite to receive the message. We need to add an Events block broadcast \(\). Click to create a new message "A".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-2.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-3.png)

3\) Add a new sprite. Under "Sprites", click "+". From the pop-up Sprite Library window, choose "Drum" and click "OK".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-4.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-5.png)

4\) Make sure "Drum" is selected. Drag an Event block when I receive \(\). Add a Sound block start sound \(\) and keep the default "high tom".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-6.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-8.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-7.png)

5\) Apply some animation effect to "Drum". Add a Looks block switch costume to \(\), and set the costume as "drum-b". Add a Control block wait \(\) seconds, and change the value to 0.2. Add another Looks block switch costume to \(\), and set the costume as "drum-a".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-9.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-10.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-7-11.png)

6\) Save your project. Press Button A to see what happens!

### 8. Design a Controller for Codey Rocky <a id="8-design-a-controller-for-codey-rocky"></a>

This project combines stage programming with Codey.

Before we start, please toggle to disable **Upload Mode**.

![](http://docs.makeblock.com/codeyrocky/en/examples/disable-upload-mode.png)

**Program Sprites**

1\) Under "Sprites", click "×" to delete the default sprite "Panda", and click "+" to add a new sprite. From the pop-up Sprites Library, choose "Arrow1" and click "OK".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-1.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-2.png)

2\) Select "Arrow1". From the Events category, drag a when this sprite clicked block and a broadcast \(\) block. Create a new message "Right".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-3.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-4.png)

3\) Right click "Arrow1" to duplicate. The new sprite will automatically be named "Arrow2". Click "Costumes" to change the costume. Select costume 2. When done, click "×" finish costume setting. In the Scripts area, click to create a new message "Left".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-5.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-6.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-7.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-8.png)

4\) Repeat step 3 to add another sprite "Arrow3" to broadcast message "Down".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-10.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-11.png)

5\) Repeat step 3 to add another sprite "Arrow4" to broadcast message "Up".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-12.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-13.png)

6\) Click to reposition the four arrows as the following image.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-14.png)

**Program Codey**

7\) Choose "Codey" under "Devices". Drag an Events block when I receive \(\) and set the message as "Left". Add an Action block turn left at power \(\)% for \(\) secs, and keep the default value.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-15.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-16.png)

8\) Drag an Events block when I receive \(\) and set the message to "Right". Add an Action block turn right at power \(\)% for \(\) secs, and keep the default value.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-17.png)

9\) Drag an Events block when I receive \(\) and set the message to "Up". Add an Action block move forward at power \(\)% for \(\) secs, and keep the default value.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-18.png)

10\) Drag an Events block when I receive \(\) and set the message to "Down". Add an Action block move backward at power \(\)% for \(\) secs, and keep the default value.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-8-19.png)

11\) Save your project. Click the arrows on the stage and see how Codey Rocky moves!

### 9. Make a Number Bomb Game <a id="9-make-a-number-bomb-game"></a>

1\) Drag an Event block when Codey starts up to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-4-1.png)

2\) Choose Variables category and click "Make a Variable". Name the variable "Number" and click "OK".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-1.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-2.png)

3\) Add a Variables block set Number to \(\), and keep default value.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-3.png)

4\) Add a Looks block show \(\) until scroll done and a Variables block Number.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-4.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-5.png)

5\) Add an Events block when button \(\) is pressed, and keep the default value. Add a Variables block change Number by \(\) and also keep the default value.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-6.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-7.png)

6\) Add a Speaker block play sound \(\) to apply some sound effects to the game.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-8.png)

7\) Click the following two blocks to duplicate and add them to the play sound \(\) block.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-9.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-10.png)

8\) Add a Control block if \(\) then \(\) to set how the game ends.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-11.png)

9\) From the Operators category, drag a \(\) &gt; \(\) block and a pick random \(\) to \(\) block. Set the number to 10 and 20. Then add a Variables block Number.

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-12.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-13.png)

10\) Add a Looks block show image \(\) and draw the following image. Add a Speaker block play sound \(\), and set the sound to "explosion".

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-14.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-15.png)

![](http://docs.makeblock.com/codeyrocky/en/examples/project-9-16.png)

11\) Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/examples/upload.png)

12\) Have a try!

## More Resources <a id="more-resources"></a>

### Example Programs <a id="example-programs"></a>

You can find a variety of built-in example programs in mBlock 5. Go to the Project Management page to access those programs.

![](http://docs.makeblock.com/codeyrocky/en/examples/examples-1.png)


# Action

![](http://docs.makeblock.com/codeyrocky/en/block-reference/rocky.png)

When Codey and Rocky are combined together, Codey Rocky can move. You can make Codey Rocky move forward or backward, turn left or right, or other more complicated movements. With the help of gyroscope, you can make Codey Rocky turn left/right a specified number of degrees, or move straight forward.

### 1. move forward at power \(\)% for \(\) secs <a id="1-move-forward-at-power--for--secs"></a>

Make Codey Rocky move forward at specified power for a specified period of time.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-1-1.png)

**Parameters:**

* Power: -100 ~ 100 \(negative number means opposite direction\)
* Time: 0 ~ ∞/second

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-1-2.png)

When Codey starts up, Codey Rocky will move forward at 50% power for one second.

### 2. move backward at power \(\)% for \(\) secs <a id="2-move-backward-at-power--for--secs"></a>

Make Codey Rocky move backward at specified power for a specified period of time.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-2-1.png)

**Parameters:**

* Power: -100 ~ 100 \(negative number means opposite direction\)
* Time: 0 ~ ∞/second

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-2-2.png)

When Codey starts up, Codey Rocky will move backward at 50% power for one second.

### 3. turn left at power \(\)% for \(\) secs <a id="3-turn-left-at-power--for--secs"></a>

Make Codey Rocky move turn left at specified power for a specified period of time.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-3-1.png)

**Parameters:**

* Power: -100 ~ 100 \(negative number means opposite direction\)
* Time: 0 ~ ∞/second

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-3-2.png)

When Codey starts up, Codey Rocky will turn left at 50% power for one second.

### 4. turn right at power \(\)% for \(\) secs <a id="4-turn-right-at-power--for--secs"></a>

Make Codey Rocky move turn right at specified power for a specified period of time.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-4-1.png)

**Parameters:**

* Power: -100 ~ 100 \(negative number means opposite direction\)
* Time: 0 ~ ∞/second

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-4-2.png)

When Codey starts up, Codey Rocky will turn right at 50% power for one second.

### 5. keep straight forward at power \(\)% for \(\) secs <a id="5-keep-straight-forward-at-power--for--secs"></a>

Use Rocky's gyroscope to make Codey Rocky move forward at the same direction at specified power for a specfied period of time.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-5-1.png)

**Parameters:**

* Power: -100 ~ 100 \(negative number means opposite direction\)
* Time: 0 ~ ∞/second

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-5-2.png)

When Codey starts up, Codey Rocky will move straight forward at 50% power for one second.

### 6. keep straight backward at power \(\)% for \(\) secs <a id="6-keep-straight-backward-at-power--for--secs"></a>

Use Rocky's gyroscope to make Codey Rocky move backward at the same direction at specified power for a specfied period of time.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-6-1.png)

**Parameters:**

* Power: -100 ~ 100 \(negative number means opposite direction\)
* Time: 0 ~ ∞/second

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-6-2.png)

When Codey starts up, Codey Rocky will move straight backward at 50% power for one second.

### 7. turn left \(\) degrees until done <a id="7-turn-left--degrees-until-done"></a>

Make Codey Rocky turn left specified degrees and wait until it's done.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-7-1.png)

**Parameter:**

* Angle: -∞ ~ ∞/degree \(negative number means opposite direction\)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-7-2.png)

When Codey starts up, Codey Rocky will turn left 15 degrees and then move forward at 50% power for one second.

### 8. turn right \(\) degrees until done <a id="8-turn-right--degrees-until-done"></a>

Make Codey Rocky turn right specified degrees and wait until it's done.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-8-1.png)

**Parameter:**

* Angle: -∞ ~ ∞/degree \(negative number means opposite direction\)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-8-2.png)

When Codey starts up, Codey Rocky will turn right 15 degrees and then move forward at 50% power for one second.

### 9. \(\) at power \(\)% <a id="9--at-power-"></a>

Make Codey Rocky move forward/backward, or turn left/right at specified power.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-9-1.png)

**Parameter:**

* Power: -100 ~ 100 \(negative number means opposite direction\)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-9-2.png)

When Codey starts up, Codey Rocky will keep moving forward at 50% power.

### 10. left wheel turns at power \(\)% and right wheel at power \(\)% <a id="10-left-wheel-turns-at-power--and-right-wheel-at-power-"></a>

Make the left wheel and right wheel of Codey Rocky move at specified power respectively.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-10-1.png)

**Parameter:**

* Power: -100 ~ 100 \(negative number means opposite direction\)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-10-2.png)

When Codey starts up, both the left wheel and the right wheel will move at 50% power for one second.

### 11. stop moving <a id="11-stop-moving"></a>

Make Codey Rocky stop moving.

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-11-1.png)

**Example:**

![](http://docs.makeblock.com/codeyrocky/en/block-reference/images/action-11-2.png)

When Codey starts up, Codey Rocky will move forward at 50% power for one second, and then stop moving.


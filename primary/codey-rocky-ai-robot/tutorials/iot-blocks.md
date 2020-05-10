# IoT Blocks

The Internet of Things \(IoT\) connects your devices together through the internet, where data can be shared and exchanged. With built-in Wi-Fi, Codey Rcoky can connect to the internet to realize its IoT functionality, such as obtaining data of the weather. Use IoT blocks to explore cutting-edge stuff with Codey Rocky.

## Add IoT Blocks

### 1. Make sure "Codey" is selected and click "+" in the Blocks area.

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-20-12.png)

### 2. From the pop-up Extension Center page, click "+" to add IoT blocks.

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-20-24.png)

### 3. Go back to Edit Page, you can find IoT category added to the block palette.

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-20-35.png)

## Have Some Fun

Let's try out the new IoT blocks. We will make Codey report weather.

### 1. Drag a when Codey starts up block from the Events category to the Scripts area.

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-21-45.png)

### 2. Drag a connect to Wi-Fi \(\) password \(\) block to connect Codey to your Wi-Fi. Type in the Wi-Fi name and password.

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-23-33.png)

### 3. Drag a if \(\) then \(\) block from the Control category. Add a Wi-Fi connected? block from the IoT category to the condition. Codey Rocky needs to join a Wi-Fi network to obtain weather data.

 

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-24-37.png)

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-25-37.png)

### 4. Drag a show \(\) block from the Looks category, and wrap it up with the if \(\) then \(\) block. We want Codey to show weather data, so we need to add a weather in \(\) block from the IoT category. Type in a city name. In this example, we type in "Shenzhen" and choose the drop-down list.

 

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-27-20.png)

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-30-06.png)

### 5. Click "Upload" to upload the program to Codey.

![](http://docs.makeblock.com/codeyrocky/en/tutorials/2018-12-05-11-30-20.png)

### 6. Check Codey's screen to see weather report.


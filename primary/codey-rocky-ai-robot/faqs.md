# FAQs

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-15-51.png)

## FAQ for Codey Rocky <a id="faq-for-codey-rocky"></a>

### 1. The system shows “The device driver is not enabled. Solutions”. <a id="1-the-system-shows-the-device-driver-is-not-enabled-solutions"></a>

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-20-59.png)

This problem happens mostly when we are installing mBlock 5. When the security software or VPN is enabled, the installation might be interrupted.

**Solution 1（This can solve the problem in most cases\):**

Close the security software \(including the windows firewall\) and VPN first and then re-install mBlock 5.

If Solution 1 doesn’t work, then try Solution 2.

**Solution 2:**

Close the security software and VPN. Then, re-install mBlock 5. Change the installation directory location this time.

**Solution 3：**

In some cases, users install mBlock 5 to a non-default installation location. In this case, the system authority management will block the device driver from being enabled.

**How to solve the problem:**

Re-stall the software to the default installation location.

### 2. Can Codey Rocky talk? <a id="2-can-codey-rocky-talk"></a>

Codey Rocky has no speech recognition block so it can’t talk. However, Neuron will come with a speech recognition block and can work with Codey Rocky.

### 3. I prefer to connect Codey Rocky to the computer via the computer’s self-contained Bluetooth? Is that OK? <a id="3-i-prefer-to-connect-codey-rocky-to-the-computer-via-the-computers-self-contained-bluetooth-is-that-ok"></a>

Mobile phones always come with a standard Bluetooth version while Bluetooth protocols and standards vary across different computers. Only a small portion of computers have the matching version. To ensure users better experiences, we currently don’t support connecting Codey Rocky via the computer’s self-contained Bluetooth.

### 4. I couldn’t connect Codey Rocky to a phone or an iPad. mBlock 5 keeps telling me to update the firmware. How to fix it? <a id="4-i-couldnt-connect-codey-rocky-to-a-phone-or-an-ipad-mblock-5-keeps-telling-me-to-update-the-firmware-how-to-fix-it"></a>

1）Download the latest version of mBlock 5 PC.

Get mBlock 5 [here](http://www.mblock.cc). 

2）Connect Codey Rocky to mBlock 5 for PC and update the firmware.

3）Try to connect Codey Rocky to your phone or iPad again.

### 5. When I connect Codey Rocky to an iPhone or iPad, mBlock 5 shows “Unidentified firmware”. How do I solve the problem? <a id="5-when-i-connect-codey-rocky-to-an-iphone-or-ipad-mblock-5-shows-unidentified-firmware--how-do-i-solve-the-problem"></a>

Temporary solution: Restart your phone/iPad and Codey Rocky. Try connecting again.

### 6. Can I update the firmware of Codey Rocky in the mBlock 5 app? <a id="6-can-i-update-the-firmware-of-codey-rocky-in-the-mblock-5-app"></a>

We currently do not support updating the firmware on phones, but we will roll out this feature later.

### 7. I cannot save projects to desktop and the Virus & Threats Center pops up telling me “Unauthorized changes blocked”. <a id="7-i-cannot-save-projects-to-desktop-and-the-virus--threats-center-pops-up-telling-me-unauthorized-changes-blocked"></a>

You need to reset the computer system. Close Windows Defender or add mBlock. exe to the trusted list of Defender.

### 8. Codey Rocky has connectors at its back. What’s the function? <a id="8-codey-rocky-has-connectors-at-its-back-whats-the-function"></a>

Codey Rocky has Pogo Pins magnetic connectors at its back, enabling it to be compatible with Neuron. Users are able to use mBlock 5 to control Codey Rocky and Neuron simultaneously.

### **9. The Bluetooth dongle failed to connect. What’s the problem?** <a id="9-the-bluetooth-dongle-failed-to-connect-whats-the-problem"></a>

1）Put your Codey close to the Bluetooth dongle and it will automatically pair with Codey. When the dongle stops flashing, it means that the dongle is successfully connected.

2）Press the button on the dongle and put your Codey close to the dongle. When the blue light stops flashing, it means the dongle is successfully connected. Then you can connect the device to the mBlock 5.

### **10. Why can’t I upload the programs?** <a id="10-why-cant-i-upload-the-programs"></a>

1）Make sure your Codey Rocky is successfully connected;

2）If you connect your Codey Rocky via a Bluetooth dongle, first check if the dongle is flashing \(light flashing means failed connection\). If it is flashing, turn the dongle off and connect again.

3）If you don’t have the problems mentioned above, then connect your Codey Rocky with the software and make sure you select the correct serial port \(if there are several ports, try each of them to see if it is the correct one\).

### **11. I get a blank white screen when I start the mBlock 5. What’s the problem?** <a id="11-i-get-a-blank-white-screen-when-i-start-the-mblock-5-whats-the-problem"></a>

The mBlock uses openGL so a low version of graphics driver might lead to a white screen. To solve the problem. you can use DriverGenius to update your graphics driver.

### **12. After I installed the software and clicked Connect Your Device, a pop-up window showed that the device was not enabled.** <a id="12-after-i-installed-the-software-and-clicked-connect-your-device-a-pop-up-window-showed-that-the-device-was-not-enabled"></a>

Some antivirus programs or security software might block the mBlock 5 to connect to ports. That’s why you couldn’t enable the device. So we suggest that you temporarily disable or exit the antivirus programs when you are running the mBlock.

### **13. My laptop comes with Bluetooth. Can I connect Codey Rocky to the laptop via Bluetooth?** <a id="13-my-laptop-comes-with-bluetooth-can-i-connect-codey-rocky-to-the-laptop-via-bluetooth"></a>

Makeblock provides an official Bluetooth dongle so you can use it for wireless connection. To ensure better experience, Codey Rocky only supports the Bluetooth dongle that’s provided by Makeblock. Therefore, we recommend that you purchase the Makeblock Bluetooth dongle if you expect better wireless connection and faster uploading. By the way, you won’t need a Bluetooth dongle if you run programs on mobile devices \(Phone/iPad\).

### **14. Does Codey Rocky support online testing? Do I have to upload offline to run the programs?** <a id="14-does-codey-rocky-support-online-testing-do-i-have-to-upload-offline-to-run--the-programs"></a>

Yes, Codey supports online testing now. But note that in Mac systems, after you connect Codey to mBlock 5 in the live mode, you need to switch to the upload mode first and then back to the live mode to enable the live mode.

### **15. Is Codey Rocky controlled by Scratch? Is face recognition supported?** <a id="15-is-codey-rocky-controlled-by-scratch-is-face-recognition-supported"></a>

Codey Rocky works with mBlock 5, the companion software developed by Makeblock.

Inspired by Scratch 3.0, mBlock 5 not only supports graphical programming but also allows users to program with Python. Moreover, mBlock 5 has AI blocks that support technologies like face recognition and speech recognition.

### **16. Can I find any app available on mobile devices?** <a id="16-can-i-find-any-app-available-on-mobile-devices"></a>

Codey Rocky supports mBlock 5 PC.

To download it, please visit [here](http://www.mblock.cc/software/mblock/mblock5/). 

It also supports mBlock 5 for Phone/Pad. Search mBlock 5 in app stores to download. mBlock 5 is available for iOS.

Makeblock app is available for iOS and Android.

### **17. The IoT feature didn’t work. What’s the problem?** <a id="17-the-iot-feature-didnt-work-whats-the-problem"></a>

You will need the cloud server if you want to use the IoT feature.

So you have to create an account for mBlock 5 first, sign in and connect to the network. Then, you can use the IoT feature.

How to sign up: click on the icon in the top right corner of mBlock 5 to sign up.

### **18. What should I do to add the IoT blocks?** <a id="18-what-should-i-do-to-add-the-iot-blocks"></a>

First, select Devices on the tab. Next, click the plus button + in the Blocks area to add the extension. There, you can find the IoT block.

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-24-49.png)

### **19. I want details about the IoT feature. Where can I get access to example courses?** <a id="19-i-want-details-about-the-iot-feature-where-can-i-get-access-to-example-courses"></a>

To help you better understand what Codey Rocky can do, we’ll roll out example programs next. Stay tuned for more!

### **20. Is my Codey Rocky covered by warranty? How long is the warranty ?** <a id="20-is-my-codey-rocky-covered-by-warranty-how-long-is-the-warranty-"></a>

Makeblock provides a 6-month warranty for electronic products and a 3-month warranty for motors. Other accessories are not covered by warranty \(including structural parts, consumables, batteries, etc.\) but we will send you replacements if there is damage to these parts due to manufacturing problems.

### **21. Where can I get help if I run into issues?** <a id="21-where-can-i-get-help-if-i-run-into-issues"></a>

Please contact technical support via emailing to inquiry@pakronics.com.au

### **22. Does the sound sensor only detect whether there is a sound?** <a id="22--does-the-sound-sensor-only-detect-whether-there-is-a-sound"></a>

It can detect the volume of sound.

### **23. The system shows: Your graphics driver version is too low. Please update it and try again.** <a id="23-the-system-shows-your-graphics-driver-version-is-too-low-please-update-it-and-try-again"></a>

To update the graphics driver, you can get help from other software like DriverGenius or directly download the latest official graphics driver.

The same problem might occur if you open the mBlock 5 instantly after you start the computer. It is because that it takes time for the system driver programs to work.

Solution: Restart the mBlock 5.

### **24. I installed mBlock 5 on my Mac and tried to connect Codey to the software. But I got a "System Extension Blocked" notification and the connection failed. How to solve the problem?** <a id="24-i-installed-mblock-5-on-my-mac-and-tried-to-connect-codey-to-the-software-but-i-got-a-system-extension-blocked-notification-and-the-connection-failed-how-to-solve-the-problem"></a>

Go to System Preferences-&gt;Security & Privacy. You will see the "System software from Jiangsu Qinheng Co. Ltd was blocked from loading" notification. Click the button "Allow" and try again.

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-28-20.png)

### **25. After I connect Codey Rocky to mBlock 5 on Mac, it shows that no serial port is detected.** <a id="25-after-i-connect-codey-rocky-to-mblock-5-on-mac-it-shows-that-no-serial-port-is-detected"></a>

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-29-14.png)

If this is the first time that you install mBlock 5 on the computer and you came across this problem, you can open System Preferences and adjust Security & Privacy. As shown below:

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-29-56.png)

Click Allow and restart the mBlock 5. Connect Codey Rocky to mBlock 5 and serial ports will be detected this time.

**Note: Only when the lock at the bottom is locked on and the second option is checked off, can the option Allow be available for being selected. So you need to check off the second option（App Store and authorized developers\), and make sure the button lock at the bottom is locked on.**

### **26. When I download mBlock in the system of MacOS High Sierra 10.13 or later versions, it shows that no serial driver can be detected and the software can’t connect to Codey, mBot or other hardware.** <a id="26-when-i-download-mblock-in-the-system-of-macos-high-sierra-1013-or-later-versions-it-shows-that-no-serial-driver-can-be-detected-and-the-software-cant-connect-to-codey-mbot-or-other-hardware"></a>

The macOS High Sierra 10.13 or later versions require user approval before loading new third-party kernel extensions. mBlock uses CH340 serial driver so it will fail to connect to Codey or mBot if the extension loading is not approved by users.

Find the apple notice at: [https://developer.apple.com/library/content/technotes/tn2459/\_index.html](https://developer.apple.com/library/content/technotes/tn2459/_index.html)

**Solution:**

1.Start the terminal: Finder --&gt; Go --&gt; Utilities --&gt; Terminal

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-31-20.png)

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-31-46.png)

2.Copy：sudo kextload /Library/Extensions/usbserial.kext/

3.Paste the line to the terminal and hit Enter. If a command Password shows up, input your computer password and hit Enter. The screenshots are as below:

Paste

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-32-34.png)

Input the computer password and hit Enter

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-33-07.png)

4.Open：Preference --&gt; Security & Privacy --&gt; General, and you will find a notice that System Software from developer “jiangsu Qinheng Co. Ltd” was blocked from loading. Click the button Allow as shown below:

![](http://docs.makeblock.com/codeyrocky/en/faq/2018-12-03-15-33-57.png)

**Reminder:**

mBlock 5 of later versions will be accessible at App Store. Users can download later versions at Apple Store to get the problem solved thoroughly \(update time to be determined\)

If you are to download mBlock 3, you still have to stick to the solution to solve the driver problem.


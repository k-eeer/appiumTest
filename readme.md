There are two simple test to the calculator android app: functional test with appium, and a load test with MonkeyRunner of Android Studio.

# Environment and Prerequisites:

ubuntu 18.04

Android Studio 3.5.2

Appium-Python-Client 1.0.2

Appium 1.15.1

Android Debug Bridge (adb)1.0.39


# Description and Usage:
# Functional Test:
This test tend to know whether 9+9=18

on calculator app and saves result snap shot.

First,start Android Studio emulator and Appium server

$emulator -avd Pixel_XL_API_29

$appium


Then, execute the script.

$python appiumTest.py

![image](https://github.com/k-eeer/appiumTest/blob/master/appiumTestInPython.png)


![image](https://github.com/k-eeer/appiumTest/blob/master/addtionResult.png)

# Load Test:
This test will execute apk 10 times. and save output as txt file.
you can use 'emulator list-avds' to list device you want to open

$adb start-server| ~/sdk/emulator/emulator -avd Pixel_XL_API_29


<br/><br/>

at another terminal window:<br/>
$adb shell monkey -p info.woodsmall.calculator -v 10 >appLoadTest.txt 2>&1<br/><br/>
As result in the output file, all the 10 times test executed successfully.<br/>
![image](https://github.com/k-eeer/androidAppTest/blob/master/appMonkeyResult.png)<br/>
the complete output file: https://github.com/k-eeer/androidAppTest/blob/master/appLoadTest.txt


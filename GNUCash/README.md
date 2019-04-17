# GNU Cash Android

I have already worked with the automation of Android applications, but when I worked it required me to have an Android mobile phone, to enable the USB Debugging under the Developer Options in Settings.

Unfortunately I am not an Android user and do not have an Android device to complete this task.

From what I worked previously, I recall that the requirements were:
- Android mobile device with its USB driver installed
- Mobile Application APK (GNUCashAndroid_v2.4.0.apk, in this case)
- Appium
- Android SDK
- Selenium standalone server .jar files and WebDriver script (that would be developed by myseld)

## Steps-by-Step

The steps to be able to accomplish the automation of functional testing in the APK would be:
- Android Mobile Device Setup
  - Enable USB Debugging in Settings\Developer Options
  - Connect mobile device to computer through USB
  - Check connection through command line:
  > adb devices
- Android SDK and Environment Variables Setup
  - Download Android SDK from [link](http://developer.android.com/sdk/index.html)
  - Configure ANDROID_HOME and PATH Environment Variables
  - Install Android SDK
- Appium Configuration Setup
  - Download Appium from [link](https://github.com/appium)
  - Configure App Path, Package and Activity (by running the command line *aapt dump badging <apk name>*) in Appium
  - Launch Appium by hitting the Launch button
- Test case scripting
  - Define a set of test cases and automate them using Selenium WebDriver
- Mobile Test Execution and Monitoring


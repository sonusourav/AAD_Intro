# Running the app on a device

## Run on a real device (Recommended)

### Set up your device as follows:

1. Connect your device to your development machine with a USB cable. If you're developing on Windows, you might need to [install the appropriate USB driver](https://developer.android.com/studio/run/oem-usb.html) for your device. ( For installing driver, type ADB driver for your respective mobile phone on Google and install the software)

2. To use your mobile for deploying your app, turn on **Developer Options** on your phone by following the below steps:       
- Open the Settings app.
- (Only on Android 8.0 or higher) Select System.
- Scroll to the bottom and select About phone. 
- Scroll to the bottom and tap Build number 7 times.
- Return to the previous screen to find Developer options near the bottom.

3. Open Developer options, and then scroll down to find and enable USB debugging.

4. Now you are all set to run the app on your mobile. Run the app on your device as follows:

    In Android Studio, click the app module in the Project window and then select Run > Run (or click Run in the toolbar).
    In the Select Deployment Target window, select your device, and click OK.

Android Studio installs the app on your connected device and starts it. You should now see **Hello World!** displayed in the app running on your device.

## Run on an emulator

### Run the app on an emulator as follows:

1. In Android Studio, click the app module in the Project window and then select Run:![toolbar-run](https://user-images.githubusercontent.com/34706326/54221506-a36f7380-4519-11e9-948f-813abe123f2c.png) > Run (or click Run in the toolbar).
2. In the Select Deployment Target window, click Create New Virtual Device.
3. In the Select Hardware screen, select a phone device, such as Pixel, and then click Next.
4. In the System Image screen, select the version with the highest API level. If you don't have that version installed, a Download link is shown, so click that and complete the download.
    Click Next.
    On the Android Virtual Device (AVD) screen, leave all the settings alone and click Finish.
    Back in the Select Deployment Target dialog, select the device you just created and click OK.

Android Studio installs the app on the emulator and starts it. You should now see "Hello World!" displayed in the app running on the emulator.

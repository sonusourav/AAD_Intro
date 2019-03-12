# Installation on Linux Platform

## To install Android Studio on Linux, proceed as follows:

1. Unpack the `.zip` file you downloaded to an appropriate location for your applications, such as within `/usr/local/` for your user profile, or `/opt/` for shared users.
2. To launch Android Studio, open a terminal, navigate to the `android-studio/bin/` directory, and execute `studio.sh`.
3. Select whether you want to import previous Android Studio settings or not, then click OK.
4. The Android Studio Setup Wizard guides you through the rest of the setup, which includes downloading Android SDK components that are required for development.
Further steps are similar to **Windows Installation** and can be found [here](https://github.com/oss2019/HelloAndroid/blob/master/Android%20Studio%20Installation%20-%20Windows.md).
 
### Required libraries for 64-bit machines:

If you are running a 64-bit version of Ubuntu, you need to install some 32-bit libraries with the following command:

`sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386`

If you are running 64-bit Fedora, the command is:

`sudo yum install zlib.i686 ncurses-libs.i686 bzip2-libs.i686`

### Video Tutorial

You can follow this video for Linux installation:
[Video Link](https://developer.android.com/studio/videos/studio-install-linux.mp4)

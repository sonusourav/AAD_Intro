# Android Studio Installation 
Android Studio is the official Integrated Development Environment (IDE) for Android app development, based on IntelliJ IDEA.

Before starting the installation process, please Download the latest version of [Android Studio](https://developer.android.com/studio/). You should have JDK (Java SE Development Kit) 7+and you can download it from [here](https://www.oracle.com/technetwork/java/javase/downloads/index.html).

So let's launch Android Studio.exe. Make sure before launching Android Studio, that environment variable JAVA_HOME is set to the JDK installation directory via command     
`SET JAVA_HOME`.   

Otherwise, Follow the steps [HERE](https://github.com/sonusourav/AAD_Resources/blob/master/Setting%20Environment%20Variable%20-%20JAVA_HOME.md#how-to-set-the-environment-variable-java_home).

## Installation on Windows Platform
### Requirements:

- 3 GB RAM minimum, 8 GB RAM recommended
- 1280 x 800 minimum screen resolution
- Microsoft® Windows® 7/8/10 (32- or 64-bit)

### Installation
1. Launch `android-studio.exe` to start the installation process. The installer responds by presenting the Android Studio Setup dialog box as shown. Click **Next** to go the **Android Virtual Device** (AVD) screen.

![studio2](https://user-images.githubusercontent.com/34706326/54194875-48228e80-44e3-11e9-80df-b52831f74061.jpg)

2. Choose the default settings and click **Next**.

![studio3](https://user-images.githubusercontent.com/34706326/54194592-9edb9880-44e2-11e9-924c-f1cc5edf661c.jpg)

3. After clicking Next,the **Configuration Settings** panel will show up, where the place to store android files have to be specified. After providing the location, click **Next**.

![studio4](https://user-images.githubusercontent.com/34706326/54194593-9edb9880-44e2-11e9-89ca-b58912709cd3.jpg)

4. On clicking Next, **Choose Start Menu Folder panel** shows up. Keep the default setting and click **Install**.

![studio5](https://user-images.githubusercontent.com/34706326/54194594-9edb9880-44e2-11e9-89a4-56c175913c72.jpg)

5. The following Installing panel appears:

![studio6](https://user-images.githubusercontent.com/34706326/54194595-9f742f00-44e2-11e9-9739-372893c3e78b.jpg)

6. Clicking **Show details** shows the names of files being installed and other activities. When installation finishes, the Installation Complete panel appears.

![studio7](https://user-images.githubusercontent.com/34706326/54194597-9f742f00-44e2-11e9-8376-dc989faabcc3.jpg)

7. To complete the installation, leave the **Start Android Studio** box checked and click **Finish**.

![studio8](https://user-images.githubusercontent.com/34706326/54194598-a00cc580-44e2-11e9-9c08-5bc5b9dd7cad.jpg)

### Running Android Studio

1. The first time Android Studio runs, it presents a **Complete Installation** dialog box that offers the option of importing settings from a previous installation.

![studio9](https://user-images.githubusercontent.com/34706326/54205116-af4c3d00-44fb-11e9-8878-08e1a8a4b023.jpg)

2. Choose **NOT** to import settings (the default selection) and click **OK**, which would take to the following splash screen:

![studio10](https://user-images.githubusercontent.com/34706326/54194599-a00cc580-44e2-11e9-8481-8006bfd88988.jpg)

3. A message box which says **Finding Available SDK Components** pops up.

![studio11](https://user-images.githubusercontent.com/34706326/54205045-8c218d80-44fb-11e9-800b-8b0a4990dfaa.jpg)

4. At this point, Android Studio presents the following Android Studio Setup Wizard dialog box:

![studio12](https://user-images.githubusercontent.com/34706326/54193652-8d918c80-44e0-11e9-876f-2bd587bc8925.jpg)

5. Click **Next**, and the wizard invites to select an installation type. Keep the default **Standard** setting.

![studio13](https://user-images.githubusercontent.com/34706326/54193654-8e2a2300-44e0-11e9-84a0-722fb4242645.jpg)

6. The next window asks user to select a user Interface Theme. Choose any one theme and press **Next**.

![studio14](https://user-images.githubusercontent.com/34706326/54193655-8ec2b980-44e0-11e9-8ad7-c5c6a7b2341c.jpg)

7. A **Verify Settings** window opens. Click **Finish** to begin the process of downloading SDK components.

![studio15](https://user-images.githubusercontent.com/34706326/54193657-8ec2b980-44e0-11e9-9d97-b8ccbbc1f3ee.jpg)

8. On the next window, Android Studio begins the process of downloading SDK components.

![studio16](https://user-images.githubusercontent.com/34706326/54193658-8ec2b980-44e0-11e9-8feb-15367ac4217b.jpg)

It can take several minutes for this part of the setup to finish. Finally, click **Finish** to complete the wizard.

![studio18](https://user-images.githubusercontent.com/34706326/54193661-8f5b5000-44e0-11e9-9ec6-a22ad471b5a0.jpg)

The **Welcome to Android Studio** dialog box appears.

![studio1](https://user-images.githubusercontent.com/34706326/54213076-cf82f880-4509-11e9-8837-87ceb525161b.jpg)

## Creating first App - **Hello World**

Now the installation process is done, and we can move to create our first app, **Hello World** - the beginning project of every developer.

1. Click on **Start a new Android Studio project**. Android Studio will respond with the Create New Project dialog box as shown.

![studio19](https://user-images.githubusercontent.com/34706326/54193662-8ff3e680-44e0-11e9-9986-d95a24405b4c.jpg)

2. Fill the project details and click **Next**.
- **Application Name** : It should match with the purpose of the app.
- **Company Domain**   : It is the domain name, which will be the app identity when the app will be uploaded on the playstore.     
                         It should have three terms atleast (e.g. com.iitdh.oss) and should be written in decreasing order ( com -> company name -> project {->}.. ) and not in opposite order.
- **Project Location** : Specify the Project location. Make sure the location name does not have white spaces in between.       
                         Generally, white spaces occurs in Computer Username (e.g. Sonu Sourav), in which case the user name      
                         should be changed to a single word (e.g. SonuSourav) otherwise it poses a problem in the future.
                   
  ![studio20](https://user-images.githubusercontent.com/34706326/54193664-8ff3e680-44e0-11e9-8ef0-bf5ea7d47f74.jpg)
                 
3. In the next window, select the target Android devices and click **Next**.

![studio21](https://user-images.githubusercontent.com/34706326/54193665-908c7d00-44e0-11e9-8c47-1e56a9b64c44.jpg)

4. The next window asks to select the type of Activity from the provided templates. Select **Empty Activity** and click **Next**.

![studio22](https://user-images.githubusercontent.com/34706326/54193667-908c7d00-44e0-11e9-8b5b-12f66b70a97c.jpg)

5. Next enter the Activity and layout name. Type **MainActivity** and **activity_main** in ActivityName and Layout name respectively. After this, press **Next**.

![studio23](https://user-images.githubusercontent.com/34706326/54193668-91251380-44e0-11e9-8489-1bf07a98f6bc.jpg)

6. A Installer windows opens up which creates the project. This might take some time, so sit back and relax. After its done, click **Finish**. 

![studio24](https://user-images.githubusercontent.com/34706326/54193669-91251380-44e0-11e9-9137-2e24500007a6.jpg)

7. The project is setup and we are ready to create our first app.

![studio25](https://user-images.githubusercontent.com/34706326/54193670-91251380-44e0-11e9-99b4-56443682f64a.jpg)


###

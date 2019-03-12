# How To Set the Environment Variable JAVA_HOME

Android Studio require the environment variable _JAVA_HOME_ to be set to the JDK installed directory.

## Windows Platform
### Check if _JAVA_HOME_ is present

1. First, find your JDK installed directory. For JDK 11, the default is "c:\Program Files\Java\jdk-11.0.{x}", where "{x} is the update number. Use your "File Explorer" to find this directory and take note of your JDK update number.
2. Check if _JAVA_HOME_ is already set. Start a CMD and run the following command:

    `SET JAVA_HOME`

3. If you get a message "`Environment variable JAVA_HOME not defined`", proceed to the next step.                 
If you get "`JAVA_HOME=C:\Program Files\Java\jdk-11.0.{x}`", then you are good to go to android studio installations.    
But before that just once verify that it is set correctly to your JDK directory (correct path is given). If not, proceed to the next step.
  
### To set the _JAVA_HOME_ environment variable:

4. To set the environment variable JAVA_HOME in Windows 10:

- Launch "Control Panel" ⇒ (Optional) "System and Security" ⇒ "System" ⇒ Click "Advanced system settings" on the left pane.
- Switch to "Advanced" tab ⇒ Click "Environment Variables"
- Under "System Variables" (the bottom pane) ⇒ Click "New" (or Look for "_JAVA_HOME_" and "Edit" if it is already set) ⇒ In   "Variable Name", enter "_JAVA_HOME_" ⇒ In "Variable Value", enter your JDK installed directory you noted in Step 1. (In the latest Windows 10: you can push the "Browse Directory" button and navigate to the JDK installed directory to avoid typo error.)
   
5. To verify, RE-START a CMD (restart is needed to refresh the environment variables) and issue:

   > `SET JAVA_HOME`   
   > `JAVA_HOME=c:\Program Files\Java\jdk-11.0.{x}`                <== Verify that this is YOUR JDK installed directory

*Note : Windows' environment variables (such as JAVA_HOME, PATH) are NOT case-sensitive.*

## Mac Platform
### Check if _JAVA_HOME_ is present

1. In some Mac systems, JDK has been pre-installed. To check if JDK has been installed, open a "Terminal" (Search "Terminal"; or Finder ⇒ Go ⇒ Utilities ⇒ Terminal) and type this command:   
`javac -version`

-  If a JDK version number is returned (e.g., JDK x.x.x), then JDK has already been installed. If the JDK version is prior to 1.8, proceed to install the latest JDK; otherwise, proceed to Android Studio installation. 
- If message "command not found" appears, JDK is NOT installed. Install JDK.
- If message "To open javac, you need a Java runtime" appears, select "Install" and follow the instructions to install JDK. 

### To set the _JAVA_HOME_ environment variable:

2. All you have to do is:     
`echo export "JAVA_HOME=\$(/usr/libexec/java_home)" >> ~/.bash_profile`  and restart your shell.   

   If you have multiple JDK versions installed and you want it to be a specific one, you can use the -v flag to java_home like so:     
   `echo export "JAVA_HOME=\$(/usr/libexec/java_home -v 1.7)" >> ~/.bash_profile`

## Linux Platform
### Check if _JAVA_HOME_ is present
Open a Terminal and type this command:

`$ javac -version`

If a JDK version number (e.g., "javac x.x.x") appears, JDK has already been installed. You can skip the installation and goto step 2.

### Download and Install JDK
1. Goto [JDK (Java SE) download site](http://www.oracle.com/technetwork/java/javase/downloads/index.html).   

  >Under "Java Platform, Standard Edition" ⇒ "Java SE 11.0.{x}" ⇒ Click JDK's "Download" ⇒ Under "Java SE Development Kit  11.0.{x}" ⇒ Check "Accept License Agreement" ⇒ Select "Linux", "tar.gz" package, (e.g., "jdk-11.0.{x}-linux-x64_bin.tar.gz" - >171MB).   

The tarball will be downloaded in directory "~/Downloads", by default.

2. We shall install JDK under "/usr/local/java" (or Ubuntu's default JDK directory /usr/lib/jvm; or /opt/java). First, create a directory "java" under "/usr/local". Open a Terminal and issue these commands:   
`$ cd /usr/local`   
`$ sudo mkdir java`

   Extract the downloaded package (Check your downloaded filename!)   
`$ cd /usr/local/java`   
`$ sudo tar xzvf ~/Downloads/jdk-11.0.{x}-linux-x64_bin.tar.gz`    
*//x: extract, z: for unzipping gz, v: verbose, f: filename*

  JDK shall be extracted in a folder "/usr/local/java/jdk-11.0.{x}", where {x} is the update number.
 
 3. Inform the Ubuntu to use this JDK/JRE:

    *Setup the location of java, javac and javaws*    
    `$ sudo update-alternatives --install "/usr/bin/java" "java" "/usr/local/java/jdk-11.0.{x}/bin/java" 1`
    
    *// --install symlink name path priority*    
    `$ sudo update-alternatives --install "/usr/bin/javac" "javac" "/usr/local/java/jdk-11.0.{x}/bin/javac" 1`     
    `$ sudo update-alternatives --install "/usr/bin/javaws" "javaws" "/usr/local/java/jdk-11.0.{x}/bin/javaws" 1`
     
    *// Use this Oracle JDK/JRE as the default*     
    `$ sudo update-alternatives --set java /usr/local/java/jdk-11.0.{x}/bin/java`
     
     *// --set name path*       
     `$ sudo update-alternatives --set javac /usr/local/java/jdk-11.0.{x}/bin/javac`    
     `$ sudo update-alternatives --set javaws /usr/local/java/jdk-11.0.{x}/bin/javaws`

    The above steps set up symlinks java, javac, javaws at /usr/bin (which is in the PATH), that link to /etc/alternatives and then to JDK bin directory.    
    
    The "alternatives" system aims to resolve the situation where several programs fulfilling the same function (e.g., different version of JDKs). It sets up symlinks thru /etc/alternatives to refer to the actual programs to be used.

    `$ ls -ld /usr/bin/java*`   
    >lrwxrwxrwx 1 root root xx xxx xx xx:xx /usr/bin/java -> /etc/alternatives/java     
    lrwxrwxrwx 1 root root xx xxx xx xx:xx /usr/bin/javac -> /etc/alternatives/javac    
    >lrwxrwxrwx 1 root root xx xxx xx xx:xx /usr/bin/javaws -> /etc/alternatives/javaws
     
    `$ ls -ld /etc/alternatives/java*`     
    >lrwxrwxrwx 1 root root xx xxx xx xx:xx /etc/alternatives/java -> /usr/local/java/jdk-11.0.{x}/bin/java     
    lrwxrwxrwx 1 root root xx xxx xx xx:xx /etc/alternatives/javac -> /usr/local/java/jdk-11.0.{x}/bin/javac     
    >lrwxrwxrwx 1 root root xx xxx xx xx:xx /etc/alternatives/javaws -> /usr/local/java/jdk-11.0.{x}/bin/javaws

    Alternatively, you can include the JDK's bin and JRE's bin into the PATH directly.
  
### To set the _JAVA_HOME_ environment variable:

4. Add JDK's binary directory ("bin") to the "PATH" by editing "/etc/profile":

`$ cd /etc`    
`$ gksudo gedit profile`                *// OR "sudo nano profile" to use the console-based nano editor*

Add these lines at the end of the file "/etc/profile", replace "{x}" with the actual number:

>export JAVA_HOME=/usr/local/java/jdk-11.0.{x}      
>export PATH=$JAVA_HOME/bin:$PATH

Rerun the configuration file by:

*// Refresh*    
`$ source /etc/profile`
 
*// Check the new settings for JAVA_HOME and PATH*     
`$ echo $JAVA_HOME`     
>/usr/local/java/jdk-11.0.{x}
 
`$ echo $PATH`    
.....:/usr/local/java/jdk-11.0.{x}/bin

# How To Set the Environment Variable JAVA_HOME

Android Studio require the environment variable _JAVA_HOME_ to be set to the JDK installed directory.

### To set the _JAVA_HOME_ environment variable:

1. First, find your JDK installed directory. For JDK 11, the default is "c:\Program Files\Java\jdk-11.0.{x}", where "{x} is the update number. Use your "File Explorer" to find this directory and take note of your JDK update number.
2. Check if _JAVA_HOME_ is already set. Start a CMD and run the following command:

    `SET JAVA_HOME`

3. If you get a message "`Environment variable JAVA_HOME not defined`", proceed to the next step.                 
If you get "`JAVA_HOME=C:\Program Files\Java\jdk-11.0.{x}`", then you are good to go to android studio installations.    
But just verify that it is set correctly to your JDK directory (correct path is given). If not, proceed to the next step.
   
4.To set the environment variable JAVA_HOME in Windows 10:

- Launch "Control Panel" ⇒ (Optional) "System and Security" ⇒ "System" ⇒ Click "Advanced system settings" on the left pane.
- Switch to "Advanced" tab ⇒ Click "Environment Variables"
- Under "System Variables" (the bottom pane) ⇒ Click "New" (or Look for "_JAVA_HOME_" and "Edit" if it is already set) ⇒ In   "Variable Name", enter "_JAVA_HOME_" ⇒ In "Variable Value", enter your JDK installed directory you noted in Step 1. (In the latest Windows 10: you can push the "Browse Directory" button and navigate to the JDK installed directory to avoid typo error.)
   
5. To verify, RE-START a CMD (restart is needed to refresh the environment variables) and issue:

   > `SET JAVA_HOME`   
   > `JAVA_HOME=c:\Program Files\Java\jdk-11.0.{x}`                <== Verify that this is YOUR JDK installed directory

*Note : Windows' environment variables (such as JAVA_HOME, PATH) are NOT case-sensitive.*

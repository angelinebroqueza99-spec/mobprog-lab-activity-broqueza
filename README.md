## Laboratory Discussion

### 1. What challenges did you encounter while installing or configuring Flutter?
Installing VS Code, Git, and Flutter was easy. The problems started when I ran my first app. The Android build failed because Gradle could not install the Android NDK, and I also got a Gradle lock error. Flutter then could not delete the build folder because my project was inside OneDrive.

### 2. Did you encounter any errors when running flutter doctor?
Yes, it showed two errors. Visual Studio was missing the "Desktop development with C++" part, but I did not need it because I did not build a Windows app. It also said "Android sdkmanager not found" because the Android SDK Command-line Tools were not installed. This was the cause of my NDK error.

### 3. How did you resolve installation, dependency, SDK, or device-related issues?
I installed the Android SDK Command-line Tools in Android Studio and accepted the licenses with `flutter doctor --android-licenses`. I stopped the Java processes, deleted the `.gradle` folder, and ran `flutter clean` to fix the Gradle lock error. I moved my project from OneDrive to `C:\dev` to fix the build folder error. I also used `cd` to go to my project folder before running commands. Finally, I tested the app in Chrome, and it showed my Hello World message.

### 4. What did you learn about configuring a Flutter development environment?
I learned that Flutter needs more than the SDK, such as the Android SDK, Command-line Tools, Gradle, and a device or browser. I learned to read error messages and use `flutter doctor -v` to find problems. I also learned that OneDrive can cause build errors. Flutter commands must be run inside the project folder.

### 5. What practices will you follow to make future Flutter development easier?
I will keep my projects in `C:\dev` instead of OneDrive. I will run `flutter doctor -v` and fix errors before building. I will check that I am in the project folder before running commands. I will also read the whole error message and save my work to GitHub often.
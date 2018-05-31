
# Getting Setup

Follow the instructions at [Flutter Setup](https://flutter.io/setup) if installing for the first time. 

## Choosing an IDE

The course uses Android Studio as their default IDE. However note that Android Studio and IntelliJ IDEA are both from [JetBrains](https://jetbrains.com) and provide near-identical integrated experiences for Flutter. 

I plan to use [IntelliJ IDEA (currently v. 2018 1.4)](https://www.jetbrains.com/idea/) as my default IDE during the initial learning phase, and switch to [Android Studio (currently v 3.1)](https://developer.android.com/studio/) later for projects. Hopefully that will give me a sense of how similar (or different) the two development experiences are, and I'll update these notes then.

Note that you can also do all your development in a simple text editor, and use the [```flutter``` utility](https://flutter.io/faq/#what-is-inside-the-flutter-sdk) to build, run and test your applications from the command line.

Finally, regardless of your choice of development environment (text editor or IDE), you will still need to install Android Studio (to support Android builds) and XCode (to support iOS builds). So in the long run, you might want to use Android Studio as the default editor.

## The Upgrade Process

If, like me, you already installed an earlier release of Flutter (e.g., alpha), you can use the ```flutter upgrade```  command to upgrade it directly. In fact, if you run the ```flutter doctor``` command regularly, as recommended, you will likely see prompts like this asking you to upgrade.

```
$ flutter doctor

  ╔════════════════════════════════════════════════════════════════════════════╗
  ║ WARNING: your installation of Flutter is 28 days old.                      ║
  ║                                                                            ║
  ║ To update to the latest version, run "flutter upgrade".                    ║
  ╚════════════════════════════════════════════════════════════════════════════╝
```

Running the upgrade command automatically triggers the ```flutter doctor``` command to do a post-upgrade check to see if any new dependencies need to be fixed.

```
$ flutter upgrade

Upgrading Flutter from /Users/.../flutter/flutter...
From https://github.com/flutter/flutter
   8be2682ee..ce6fbeb5b  master     -> origin/master
Already up to date.

Upgrading engine...
Already up-to-date.

Flutter 0.3.2 • channel beta • https://github.com/flutter/flutter.git
Framework • revision 44b7e7d3f4 (4 weeks ago) • 2018-04-20 01:02:44 -0700
Engine • revision 09d05a3891
Tools • Dart 2.0.0-dev.48.0.flutter-fe606f890b

Running flutter doctor...
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel beta, v0.3.2, on Mac OS X 10.13.4 17E199, locale en-US)
[✓] Android toolchain - develop for Android devices (Android SDK 28.0.0-rc1)
[✓] iOS toolchain - develop for iOS devices (Xcode 9.3.1)
[✓] Android Studio (version 3.1)
[✓] IntelliJ IDEA Ultimate Edition (version 2018.1.2)
[!] Connected devices
    ! No devices available

! Doctor found issues in 1 category.
```

The "No devices available" warning happens because I am not currently running an Android emulator or an iOS simulator, nor do I have a physical device connected. 

_Let me fix that by starting an iPhone simulator (on MacOS)._ 

```
$ open -a Simulator.app
```

_We can use ```adb``` to find and run Android emulators from the command line. But you must have the Android SDK installed first. If using an IDE, we can simply pick Android or iOS target devices at runtime from that menu._

Running the iPhone simulator should fix the warning - let's check. (_Update: Updated May 31, 2018._)

```
$ flutter doctor

Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel beta, v0.4.4, on Mac OS X 10.13.4 17E199, locale en-US)
[✓] Android toolchain - develop for Android devices (Android SDK 28.0.0-rc1)
[✓] iOS toolchain - develop for iOS devices (Xcode 9.3.1)
[✓] Android Studio (version 3.1)
[✓] IntelliJ IDEA Ultimate Edition (version 2018.1.4)
[✓] Connected devices (1 available)

• No issues found!
```

You can also attach a real device (e.g., over USB) and have that be a valid target. Note that you can safely ignore the warning during the development phase, but is a great way to check for connected devices prior to testing.


## Creating your first app: IDE vs. CLI

You can create a Flutter app using the Flutter IDE workflow or by using the Flutter CLI (```flutter create hello_rectangle```).

If you follow the latter approach, you can technically do all your development with any text-based editor (e.g. Sublime) and use ```flutter``` for all build/run steps. I recommend doing this initially (just to gain familiarity with the tool) then loading the created project into an IDE for subsquent exploration.

Not only does this prove the IDE and CLI are compatible (and interchangeable for development needs) but the IDE provides valuable visual tools (e.g., Widget Inspector) that bring added value during build and testing phases.

[Next: Create the HelloRectangle App](102-HelloRectangleApp.md)

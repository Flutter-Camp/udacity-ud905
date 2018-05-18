# Build Native Mobile Apps With Flutter

Notes from [UD905 - Udacity Course on Flutter](https://www.udacity.com/course/build-native-mobile-apps-with-flutter--ud905) 
released May 2018 in conjunction with Google I/O. The course 
currently has two parts:

 1. [The Flutter Framework](#1-the-flutter-framework). Focus on fundamentals.
 2. [Building Interactive Apps](#2-building-interactive-apps). Focus on Material Design. 
 
 In this readme I hope to capture relevant notes from my 
 walk-through of this course that would support running this
 as a self-guided or study-group based workshop.
 
 <hr/>
 
## 1. The Flutter Framework
 
### Introduction

> What is Flutter?

 * Modern REACTIVE framework
 * Fast 2D RENDERING engine
 * Rich TOOLING for development
 * Ready-made WIDGET collections
 
> What you'll learn:

 * How to structure & architect apps
 * How to build app for Android & iOS
 * How to use tools efficiently
 
> Main topics
 
 * Widgets
 * State Management
 * Packages
 * Material Design
 * User Interface & Gestures
 
> Why Flutter?

 * One codebase, multiple native platforms
 * Performant: No bridges, direct render to GPU
 * Rapid prototyping: Hot reload, high fidelity
 * Open source: Everything is customizable
 
> Why Dart?
 
Flutter apps are written using [Dart](https://dartlang.org)
and get compiled into native (Android or iOS) apps that can 
be shipped in respective device app markets.

 * Dart is performant: fast, smooth animations
 * Just-in-time compilation: powers Hot Reload!
 * Ahead-of-time compilation: tree-shaking, optimal apps
 * Static types, sound type system: easy to develop & debug
 * OO Development: will be familiar to Java, Swift & JS developers
 
### Getting Setup

Before building your first app, first [validate your setup](https://flutter.io/setup). The
course uses Android Studio. I am going to focus on using
IntelliJ IDEA (as IDE) and Flutter CLI (```flutter```) to 
the extent possible so that we don't give a false
impression that development requires Android experience 
or familiarity.

_Note: I had previously installed Flutter during its alpha release and
 simply upgrade it regularly. I was prompted to do so 
automatically to do so as you can see._

```
$ flutter doctor

  ╔════════════════════════════════════════════════════════════════════════════╗
  ║ WARNING: your installation of Flutter is 28 days old.                      ║
  ║                                                                            ║
  ║ To update to the latest version, run "flutter upgrade".                    ║
  ╚════════════════════════════════════════════════════════════════════════════╝

```
_So I ran the upgrade process as requested:_

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

_The "No devices available" warning happens because I am not 
currently running an Android emulator or an iOS simulator, 
nor do I have a physical device connected. Let me fix that 
by starting an iPhone simulator (on MacOS)._ 


```
$ open -a Simulator.app
```
This should fix the warning though, to be clear, you 
can ignore the warning for now and start with the
development phase if you want to.

```
$ flutter doctor

Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel beta, v0.3.2, on Mac OS X 10.13.4 17E199, locale en-US)
[✓] Android toolchain - develop for Android devices (Android SDK 28.0.0-rc1)
[✓] iOS toolchain - develop for iOS devices (Xcode 9.3.1)
[✓] Android Studio (version 3.1)
[✓] IntelliJ IDEA Ultimate Edition (version 2018.1.2)
[✓] Connected devices (1 available)

• No issues found!
```

_You can also use ```adb``` to run Android emulators 
from the command line. But you must have the Android
SDK installed first. Later on, when using the
IntelliJ IDE, we can pick Android or iOS target devices
at runtime from that menu._


> Getting Started: CLI vs. IDE

You can create a Flutter app using the Flutter IDE workflow
or by using the Flutter CLI (```flutter create hello_rectangle```).
If you follow the latter approach, you can technically
do all your development with any text-based editor (e.g.
Sublime) and use ```flutter``` for all build/run steps. 
I recommend this for simple exploration. 

However, the IDE provides additional tooling 
(e.g., exploring widget tree) that can be useful
in the long run. Android developers may also 
prefer to stick with Studio for its familiarity. I
will use/explore IntelliJ IDEA instead and report on
the relevant tooling options/support here.

_I am going to use the CLI to create, and
then use the "Open" feature of the IDE to load the 
existing project for the build/debug phases just to
explore both environments._


### Hello Rectangle App

Alright let's create that project!

```$xslt
$ flutter create hello_rectangle
All done! In order to run your application, type:

<truncated output ...>

  $ cd hello_rectangle
  $ flutter run

Your main program file is lib/main.dart in the hello_rectangle directory.
```

Alright. This creates a ```hello_rectangle/``` directory.
I opened this up with IntelliJ IDEA and looked into the ```lib/main.dart``` file. On first opening this, I see a **"Dart is not enabled for this ..."**
message on the IDE, with options to **"Enable Dart Support"** and **"Open Dart Settings"**. I simply clicked _Enable Dart Support_ and was good to go.

Check out the [Hello Rectangle README.md](hello_rectangle/README.md) for more details on the next steps & notes.

### Flutter Internals

Learn more about the Reactive Framework and the Development Tools through these resources (detailed notes TBD).

1. [Flutter Rendering](https://www.youtube.com/watch?v=UUfXWzp0-DU)
2. [Flutter Engine](https://github.com/flutter/engine/wiki)
3. [Hot Reload](https://flutter.io/hot-reload/)
4. [Flutter Inspector](https://dart-lang.github.io/observatory/)
5. [Dart Style Guide](https://www.dartlang.org/guides/language/effective-dart/style)
6. [Dart Observatory](https://dart-lang.github.io/observatory/)


<hr/>
 
## 2. Building Interactive Apps

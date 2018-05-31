# Hello Rectangle App

Alright let's create that project!

```
$ flutter create hello_rectangle

All done! In order to run your application, type:

<truncated output ...>

  $ cd hello_rectangle
  $ flutter run

Your main program file is lib/main.dart in the hello_rectangle directory.
```

This creates a ```hello_rectangle/``` directory. Try opening that project in your IDE and look for the _lib/main.dart_ file.

> When opening this for the first time, you may see a "Dart is not enabled for this .." alert with two options: "Enable Dart Support" or "Open Dart Settings". I simply clicked the first, and was good to go.

Let's look at the boilerplate code.


## 1. Inspect: Boilerplate Codebase

The new [Flutter](https://flutter.io/) project contains the following:

 * lib/main.dart - _the Flutter source; main is the entry point for app_
 * android/ - _the android build created from the Flutter source_
 * ios/ - _the iOS build created from the Flutter source_
 * test/ - _the default test harness setup for UI/widget testing_
 * .gitignore - _Git version control; rarely edited_
 * .metadata, .packages - _configuration info; do not edit_
 * .idea - _exists for IntelliJ IDEA config only; .gitignore it_
 * hello_rectangle.iml, hello_rectangle_android.iml - _used by IntelliJ; do not edit._
 * pubspec.yaml - _used to manage [Dart Package](https://www.dartlang.org/tools/pub/pubspec) dependencies_
 
> Run the default created app first, to make sure setup is correct.

 You should see the "Flutter Demo Home page" with the _You have pushed this button many times_ label. This verifies your app was created and that your IDE is setup to build/run the code.

## 2. Replace: Starter Code

Delete the contents of _main.dart_ and replace it with the contents found in this [_starter code_](https://github.com/flutter/udacity-course/blob/master/course/01_hello_rectangle/solution_01_hello_rectangle/lib/main.dart) from the Udacity course.

> Build and run it as before. Check that the emulator (or simulator) now shows the updated app screen.

This should be a full white screen with a centered green rectangle containing the word "Hello!". 

You may notice that the IDE will flag the test directory with errors - the default test looks for MyApp, which is no longer existent. _We'll fix tests later. For now keep going._



## 3. Resources: Flutter Internals

Learn more about the Reactive Framework and the Development Tools through these resources (detailed notes TBD).

1. [Flutter Rendering](https://www.youtube.com/watch?v=UUfXWzp0-DU)
2. [Flutter Engine](https://github.com/flutter/engine/wiki)
3. [Hot Reload](https://flutter.io/hot-reload/)
4. [Flutter Inspector](https://dart-lang.github.io/observatory/)
5. [Dart Style Guide](https://www.dartlang.org/guides/language/effective-dart/style)
6. [Dart Observatory](https://dart-lang.github.io/observatory/)

_I'll review these and add notes on each later, so check back_

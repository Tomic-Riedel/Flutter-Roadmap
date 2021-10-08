# Running Native Swift, ObjectiveC, Java, or Kotlin Code

When building apps with flutter sometimes we might get stuck on implementing some features which flutter can't do because its a platform specific feature for that flutter provides a channel called Platform Channel with which we can call platform specific apis. This is a part where some people get scared even I got scared because I am not a native android or ios developer. But the docs of android and flutter are so good I figured it out in a day. 

**One thing to note is that using Platform Channels to communicate to the platform takes some time it should be avoided as long as you have an option to do that with pure dart code.**

[Writing custom platform-specific code](https://flutter.dev/docs/development/platform-integration/platform-channels). This will help get you started to write platform specific code, it has all the things you need to know about Platform Channels.

There are 2 types of Platform Channels one is called MethodChannel and another one is called EventChannel. MethodChannel does what it says it does, lets you call methods from the platform. EventChannel on the other hand will help you listen to events from the platform an example would be listening to sensors. Now the problem is there isn't enough docs about EventChannel on the official docs of flutter but there is an excelent article 
[An In-Depth Dive Into Streaming Data Across Platform Channels on Flutter](https://www.raywenderlich.com/20518849-an-in-depth-dive-into-streaming-data-across-platform-channels-on-flutter)

Sometimes you might need to show a native view in your flutter app as a widget for example webview Flutter's got you covered for that too with PlatformViews 
[Hosting native Android and iOS views in your Flutter app with Platform View](https://flutter.dev/docs/development/platform-integration/platform-views).

You can also use dart:ffi to call native C api's which is much faster than Platform Channels [Binding to native code using dart:ffi](https://flutter.dev/docs/development/platform-integration/c-interop)
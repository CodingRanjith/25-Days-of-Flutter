<div align="center">
<img  height="100%"  src="https://i.ibb.co/6srHHVp/flutter.webp" />
</div>

<div align="center">

  <h1>Day - 01 in Flutter</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/coding-ranjith-97b6ab238">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>

  <a class="header-badge" target="_blank" href="https://youtube.com/@coding-ranjith">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=Youtube&logo=youtube&style=social">
  </a>

<sub>Author: <a href="https://www.linkedin.com/in/coding-ranjith-97b6ab238" target="_blank">Coding Ranjith</a><br>
<small>February to March, 2024</small></sub>

</div>


- Introduction to Flutter, setup development environment (Flutter SDK, IDE). 
  - [Learn about Flutter's role and advantages.](#introduction)
  - [Install Flutter SDK and set up an IDE.](#setup)
  - [Create your first Flutter project.](#first-flutter-app)
 
    
--- 

## Introduction

### Learn about Flutter's role and advantages.

### What is Flutter?

<div align="center">
<img  height="80%"  src="https://i.ibb.co/SXNVs8p/60bb4a2e143f632da3e56aea-Flutter-app-development-2.png"/>
</div>

Flutter is Google's UI toolkit for building natively compiled applications for mobile, web, and desktop from a single codebase. It allows developers to create beautiful and fast user experiences across multiple platforms.

### Key Features of Flutter:

- **Single Codebase**: Write code once and deploy it on multiple platforms like iOS, Android, web, and desktop.
- **Hot Reload**: Instantly see the changes you make to your code without restarting your app.
- **Fast Performance**: Flutter apps are compiled directly to native code, providing near-native performance.
- **Rich Widget Library**: Flutter provides a rich set of pre-built UI components called widgets for building beautiful interfaces.
- **Expressive UI**: Create complex UIs with custom animations and transitions using Flutter's powerful widget system.
- **Open Source**: Flutter is an open-source project, allowing developers to contribute and extend its capabilities.

## Resources

- [Flutter Documentation](https://flutter.dev/docs): Official documentation for Flutter, including guides, tutorials, and API references.
- [Flutter Samples](https://flutter.dev/docs/cookbook): Explore Flutter code samples and cookbook recipes for common app scenarios.
- [Flutter Community](https://flutter.dev/community): Engage with the Flutter community through forums, meetups, and events.
- [Dart Documentation](https://dart.dev/guides): Official documentation for the Dart programming language.


### What is an IDE?

An Integrated Development Environment (IDE) is a software application that provides comprehensive facilities to programmers for software development. An IDE typically consists of a code editor, compiler, debugger, and build automation tools.

### Popular IDEs for Flutter Development:

- **Visual Studio Code**: A lightweight but powerful code editor with built-in support for Flutter development.
- **Android Studio**: An official IDE for Android development, also suitable for Flutter development with additional plugins.

## Setup

### Install Flutter SDK and set up an IDE

#### Install Flutter SDK

To install the Flutter SDK, follow the instructions provided in the official Flutter documentation:

[Install Flutter](https://flutter.dev/docs/get-started/install)

Make sure to add the Flutter SDK to your system PATH for easy access to Flutter commands.

#### Set up an IDE

Choose an IDE for Flutter development based on your preference:

- **Visual Studio Code**: Install the Flutter and Dart plugins from the VS Code marketplace.
  [Visual Studio Code](https://code.visualstudio.com/download)

- **Android Studio**: Install the Flutter plugin from the IDE settings or marketplace.

After installing the IDE and plugins, configure them to use the Flutter SDK installed on your system.

## First Flutter App

### Create your first Flutter project

To create a new Flutter project, run the following command in your terminal:

```bash
flutter create my_first_flutter_app

```

<div align="center">
<img  height="80%"  src="https://i.ibb.co/vkL3BFs/day-1-1.png"/>
</div>

This will create a new Flutter project named my_first_flutter_app.

Navigate to the project directory and open it in your preferred IDE.

Run the project using the following command:

```bash
flutter run
```

<div align="center">
<img  height="80%"  src="https://i.ibb.co/7bxGbKz/day-1-2.png"/>
</div>

A new Flutter app will be launched on your connected device or emulator.

### Modify the Flutter App

Open the lib/main.dart file in your IDE and make changes to the default app.

For example, you can modify the title property of the MyApp widget:

```bash 
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'My First Flutter App',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Welcome to Flutter'),
        ),
        body: Center(
          child: Text('Hello World'),
        ),
      ),
    );
  }
}
```

Save the changes, and they will reflect in the running Flutter app.

### Upgrade to Latest Flutter Version 

To upgrade to the latest version of Flutter, run the following command in your terminal:

```bash 
flutter upgrade
```
This will upgrade your Flutter SDK to the latest stable release.


[Day 2 >>](https://github.com/CodingRanjith/25-Days-of-Flutter/tree/main/Day-02)


❤️👨‍💻❤️ HAPPY CODING ❤️😇❤️



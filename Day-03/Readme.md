<div align="center">
<img  height="100%"  src="https://i.ibb.co/6srHHVp/flutter.webp" />
</div>

<div align="center">

  <h1>Day - 03 in Flutter</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/coding-ranjith-97b6ab238">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>

  <a class="header-badge" target="_blank" href="https://youtube.com/@coding-ranjith">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=Youtube&logo=youtube&style=social">
  </a>

<sub>Author: <a href="https://www.linkedin.com/in/coding-ranjith-97b6ab238" target="_blank">Coding Ranjith</a><br>
<small>February to March, 2024</small></sub>

</div>


- Exploring Advanced Topics in Flutter Development.


--- 

## Introduction

### Welcome to Day 3 of the 25 Days of Flutter series! Today, we'll dive into advanced topics in Flutter development, building upon the foundation we've established in the previous days.

## Topics Covered

### 1. Flutter Widgets

Widgets are the building blocks of Flutter UIs. We'll explore various types of widgets, including:

- **Material Design Widgets**: Widgets following Google's Material Design guidelines for UI elements.
- **Cupertino Widgets**: Widgets with an iOS-style design for Cupertino (iOS-flavored) applications.
- **Custom Widgets**: Creating custom widgets to encapsulate UI elements and functionality.

### 2. Flutter Layouts

Layouts determine how widgets are arranged and displayed within a Flutter application. We'll cover layout concepts such as:

- **Row and Column**: Arranging widgets horizontally (row) or vertically (column).
- **Container**: A versatile widget for customizing the layout, padding, margin, and decoration of child widgets.
- **Stack**: Stacking widgets on top of each other with absolute or relative positioning.

### 3. Flutter Gestures

Gestures enable user interaction with Flutter applications. We'll explore gesture detection and handling, including:

- **Tap Gesture**: Detecting taps on widgets.
- **Swipe Gesture**: Detecting swipe motions across the screen.
- **Drag Gesture**: Handling drag-and-drop interactions.

### 4. Flutter State Management

State management is essential for managing data and UI state in Flutter applications. We'll discuss state management techniques, including:

- **setState()**: Managing state within a StatefulWidget using the setState() method.
- **Provider Package**: Using the Provider package for simple and scalable state management.
- **Bloc Pattern**: Implementing the Business Logic Component (BLoC) pattern for managing complex application state.

### 5. Flutter IDE

Choosing the right Integrated Development Environment (IDE) can significantly impact your Flutter development workflow. We'll explore popular IDEs for Flutter development, including:

- **Visual Studio Code**: A lightweight and powerful code editor with excellent Flutter support.
- **Android Studio**: An official IDE for Android development, offering robust Flutter integration.
- **IntelliJ IDEA**: Another option for Flutter development, offering a feature-rich environment.

## Examples

### Example 1: Flutter Widget

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Flutter Widget Example'),
        ),
        body: Center(
          child: Text('This is a Flutter widget.'),
        ),
      ),
    );
  }
}
```

<div align="center">
<img  height="80%"  src="https://i.ibb.co/njktjz5/3-1.png"/>
</div>

### Example 2: Flutter Layout

```dart 
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Flutter Layout Example'),
        ),
        body: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text('First Widget'),
            Text('Second Widget'),
            Text('Third Widget'),
          ],
        ),
      ),
    );
  }
}
```

<div align="center">
<img  height="80%"  src="https://i.ibb.co/ynK9gbD/3-2.png"/>
</div>

### Example 3: Flutter Gesture

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Flutter Gesture Example'),
        ),
        body: GestureDetector(
          onTap: () {
            print('Widget tapped!');
          },
          child: Container(
            width: 200,
            height: 200,
            color: Colors.blue,
            child: Center(
              child: Text(
                'Tap Me!',
                style: TextStyle(
                  fontSize: 20,
                  color: Colors.white,
                ),
              ),
            ),
          ),
        ),
      ),
    );
  }
}
```

<div align="center">
<img  height="80%"  src="https://i.ibb.co/Y7rpTRD/3-3.png"/>
</div>

### Resources

- [Flutter Widget Catalog](https://flutter.dev/docs/development/ui/widgets): Official catalog of Flutter widgets with examples and usage guidelines.
- [Flutter Layout Cheat Sheet](https://medium.com/flutter-community/flutter-layout-cheat-sheet-5363348d037e): A comprehensive cheat sheet for Flutter layout widgets.
- [Flutter Gesture Detection Guide](https://flutter.dev/docs/development/ui/advanced/gestures): Official guide to handling gestures in Flutter applications.
- [Flutter State Management Guide](https://flutter.dev/docs/development/data-and-backend/state-mgmt): Official guide to state management in Flutter.



### Example Login Page 

```dart

import 'package:flutter/material.dart';

void main() {
  runApp(LoginApp());
}

class LoginApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Login Demo',
      home: LoginPage(),
    );
  }
}

class LoginPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Login'),
      ),
      body: Center(
        child: LoginForm(),
      ),
    );
  }
}

class LoginForm extends StatefulWidget {
  @override
  _LoginFormState createState() => _LoginFormState();
}

class _LoginFormState extends State<LoginForm> {
  final TextEditingController _usernameController = TextEditingController();
  final TextEditingController _passwordController = TextEditingController();

  @override
  Widget build(BuildContext context) {
    return Padding(
      padding: const EdgeInsets.all(20.0),
      child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          TextField(
            controller: _usernameController,
            decoration: InputDecoration(
              labelText: 'Username',
            ),
          ),
          SizedBox(height: 20),
          TextField(
            controller: _passwordController,
            obscureText: true,
            decoration: InputDecoration(
              labelText: 'Password',
            ),
          ),
          SizedBox(height: 20),
          ElevatedButton(
            onPressed: () {
              // Placeholder for login logic
              final username = _usernameController.text;
              final password = _passwordController.text;

              // Perform login validation here
              if (username == 'admin' && password == 'password') {
                // Navigate to the home screen or perform other actions
                ScaffoldMessenger.of(context).showSnackBar(
                  SnackBar(content: Text('Login successful!')),
                );
              } else {
                // Show error message for invalid credentials
                ScaffoldMessenger.of(context).showSnackBar(
                  SnackBar(content: Text('Invalid username or password')),
                );
              }
            },
            child: Text('Login'),
          ),
        ],
      ),
    );
  }
}

```

<div align="center">
<img  height="80%"  src="https://i.ibb.co/R40dLRW/3-4.png"/>
</div>

[Day 4 >>]()


❤️👨‍💻❤️ HAPPY CODING ❤️😇❤️


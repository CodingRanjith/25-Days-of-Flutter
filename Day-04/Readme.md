<div align="center">
<img height="100%" src="https://i.ibb.co/6srHHVp/flutter.webp" />
</div>

<div align="center">

  <h1>Day - 04 in Flutter</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/coding-ranjith-97b6ab238">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>

  <a class="header-badge" target="_blank" href="https://youtube.com/@coding-ranjith">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=Youtube&logo=youtube&style=social">
  </a>

<sub>Author: <a href="https://www.linkedin.com/in/coding-ranjith-97b6ab238" target="_blank">Coding Ranjith</a><br>
<small>February to March, 2024</small></sub>

</div>

## Flutter Widgets

In Day 4, we'll explore various essential Flutter widgets that are commonly used to build user interfaces. These widgets play a crucial role in creating interactive and visually appealing apps.

### Topics Covered

1. **Flutter Scaffold**
   - Introduction to the Scaffold widget and its role in providing a basic app layout structure.
   - Example:

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
             title: Text('Scaffold Example'),
           ),
           body: Center(
             child: Text('Hello, Flutter!'),
           ),
         ),
       );
     }
   }

```

2. **Flutter Container**

   - Understanding the Container widget and its flexibility in customizing the appearance of child widgets.
   - Example:

```dart
Container(
  width: 100,
  height: 50,
  color: Colors.blue,
  child: Center(
    child: Text(
      'Custom Button',
      style: TextStyle(color: Colors.white),
    ),
  ),
)
```

3. **Flutter Row & Column**

   - Exploring the Row and Column widgets for arranging child widgets horizontally and vertically, respectively.
   - Example:

```dart

Column(
  mainAxisAlignment: MainAxisAlignment.center,
  children: [
    Text('Item 1'),
    Text('Item 2'),
    Text('Item 3'),
  ],
)
```

4. **Flutter Text**

  - Learning about the Text widget for displaying text on the screen with various styling options.
  - Example:

```dart 
Text(
  'Hello Flutter!',
  style: TextStyle(fontSize: 20, color: Colors.blue),
)
```

5. **Flutter TextField**

   - Understanding the TextField widget for capturing user input as text, along with its features like       placeholder text and input validation.
   - Example:

```dart

TextField(
  decoration: InputDecoration(
    labelText: 'Username',
    hintText: 'Enter your username',
  ),
)
```

6. **Flutter Buttons**

   - Introduction to different types of buttons in Flutter, including ElevatedButton, TextButton, and OutlinedButton.
   - Example:

```dart
ElevatedButton(
  onPressed: () {
    // Button click action
  },
  child: Text('Elevated Button'),
)
```

7. **Flutter Stack**

   - Exploring the Stack widget for overlaying widgets on top of each other in a layered manner.
   - Example:

```dart

Stack(
  children: [
    Container(color: Colors.blue, height: 200),
    Positioned(
      top: 50,
      left: 50,
      child: Text('Overlay Text', style: TextStyle(color: Colors.white)),
    ),
  ],
)
```

8. **Flutter Forms**

   - Learning how to create forms in Flutter to collect user input efficiently.
   - Example:

```dart
Form(
  child: Column(
    children: [
      TextFormField(
        decoration: InputDecoration(labelText: 'Username'),
        validator: (value) {
          if (value.isEmpty) {
            return 'Please enter a username';
          }
          return null;
        },
      ),
      // Other form fields...
    ],
  ),
)
```

9. **Flutter AlertDialog**

   - Understanding the AlertDialog widget for displaying important messages or prompting users for confirmation.
   - Example:

```dart

ElevatedButton(
  onPressed: () {
    showDialog(
      context: context,
      builder: (BuildContext context) {
        return AlertDialog(
          title: Text('Confirmation'),
          content: Text('Are you sure you want to delete?'),
          actions: [
            TextButton(
              onPressed: () {
                Navigator.of(context).pop();
              },
              child: Text('Cancel'),
            ),
            TextButton(
              onPressed: () {
                // Delete operation
              },
              child: Text('Delete'),
            ),
          ],
        );
      },
    );
  },
  child: Text('Show AlertDialog'),
)
```

10. **Flutter Icons**

   - Introduction to using icons in Flutter applications using the Icon widget and the Material Icons library.
   - Example:

```dart 

IconButton(
  icon: Icon(Icons.delete),
  onPressed: () {
    // Delete action
  },
)
```



[Day 5 >>]()


❤️👨‍💻❤️ HAPPY CODING ❤️😇❤️






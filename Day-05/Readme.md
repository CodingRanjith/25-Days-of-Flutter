<div align="center">
<img height="100%" src="https://i.ibb.co/6srHHVp/flutter.webp" />
</div>

<div align="center">

  <h1>Day - 05 in Flutter</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/coding-ranjith-97b6ab238">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>

  <a class="header-badge" target="_blank" href="https://youtube.com/@coding-ranjith">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=Youtube&logo=youtube&style=social">
  </a>

<sub>Author: <a href="https://www.linkedin.com/in/coding-ranjith-97b6ab238" target="_blank">Coding Ranjith</a><br>
<small>February to March, 2024</small></sub>

</div>

## Flutter Widgets (Topics 11-20)

In Day 5, we'll explore more Flutter widgets that are commonly used to build user interfaces. These widgets play a crucial role in creating interactive and visually appealing apps.

### 11. Flutter Images

Learn how to display images in Flutter applications using the Image widget.

#### Example:

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text('Image Example')),
        body: Image.network(
          'https://example.com/image.jpg',
          width: 200,
          height: 200,
        ),
      ),
    );
  }
}
```

### 12. Flutter Card

Explore the Card widget for displaying information in a structured manner with a consistent design.

### Example:

```dart 
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text('Card Example')),
        body: Center(
          child: Card(
            child: ListTile(
              leading: Icon(Icons.album),
              title: Text('Title'),
              subtitle: Text('Description'),
            ),
          ),
        ),
      ),
    );
  }
}
```

### 13. Flutter Tabbar

Learn how to implement tab bars in Flutter applications for organizing content.

### Example:

```dart 
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: DefaultTabController(
        length: 3,
        child: Scaffold(
          appBar: AppBar(
            title: Text('Tab Bar Example'),
            bottom: TabBar(
              tabs: [
                Tab(icon: Icon(Icons.directions_car)),
                Tab(icon: Icon(Icons.directions_transit)),
                Tab(icon: Icon(Icons.directions_bike)),
              ],
            ),
          ),
          body: TabBarView(
            children: [
              Icon(Icons.directions_car),
              Icon(Icons.directions_transit),
              Icon(Icons.directions_bike),
            ],
          ),
        ),
      ),
    );
  }
}
```

### 14. Flutter Drawer

Discover how to create a navigation drawer in Flutter applications for accessing additional screens or options.

### Example:

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
          title: Text('Drawer Example'),
        ),
        drawer: Drawer(
          child: ListView(
            padding: EdgeInsets.zero,
            children: <Widget>[
              DrawerHeader(
                decoration: BoxDecoration(
                  color: Colors.blue,
                ),
                child: Text('Drawer Header'),
              ),
              ListTile(
                title: Text('Item 1'),
                onTap: () {
                  // Update UI based on item selected
                },
              ),
              ListTile(
                title: Text('Item 2'),
                onTap: () {
                  // Update UI based on item selected
                },
              ),
            ],
          ),
        ),
        body: Center(
          child: Text('Home Screen'),
        ),
      ),
    );
  }
}

```

### 15. Flutter Lists 

Introduction to displaying lists of data using various list view widgets in Flutter.

### Example:

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
          title: Text('List Example'),
        ),
        body: ListView.builder(
          itemCount: 5,
          itemBuilder: (BuildContext context, int index) {
            return ListTile(
              leading: Icon(Icons.list),
              title: Text('Item $index'),
              onTap: () {
                // Action to perform when item is tapped
              },
            );
          },
        ),
      ),
    );
  }
}

```

### 16. Flutter GridView

Understand how to create grid layouts for displaying data in a tabular format.

### Example:

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
          title: Text('GridView Example'),
        ),
        body: GridView.count(
          crossAxisCount: 2,
          children: List.generate(6, (index) {
            return Center(
              child: Text(
                'Item $index',
                style: TextStyle(fontSize: 24),
              ),
            );
          }),
        ),
      ),
    );
  }
}

```
### 17. Flutter Toast

Learn how to show toast messages in Flutter applications using the Toast package.

### Example:

```dart 

import 'package:flutter/material.dart';
import 'package:fluttertoast/fluttertoast.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Toast Example'),
        ),
        body: Center(
          child: ElevatedButton(
            onPressed: () {
              Fluttertoast.showToast(
                msg: 'This is a toast message!',
                toastLength: Toast.LENGTH_SHORT,
                gravity: ToastGravity.BOTTOM,
              );
            },
            child: Text('Show Toast'),
          ),
        ),
      ),
    );
  }
}

```
### 18. Flutter Checkbox

Explore the Checkbox widget for capturing boolean input from users.

### Example:

```dart 

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  bool isChecked = false;

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Checkbox Example'),
        ),
        body: Center(
          child: Checkbox(
            value: isChecked,
            onChanged: (bool value) {
              setState(() {
                isChecked = value;
              });
            },
          ),
        ),
      ),
    );
  }
}

```

### 19. Flutter Radio Button

Understand how to create radio buttons in Flutter applications for selecting a single option from a list.

### Example:

```dart 

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  int selectedValue;

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Radio Button Example'),
        ),
        body: Column(
          children: [
            RadioListTile(
              title: Text('Option 1'),
              value: 1,
              groupValue: selectedValue,
              onChanged: (int value) {
                setState(() {
                  selectedValue = value;
                });
              },
            ),
            RadioListTile(
              title: Text('Option 2'),
              value: 2,
              groupValue: selectedValue,
              onChanged: (int value) {
                setState(() {
                  selectedValue = value;
                });
              },
            ),
          ],
        ),
      ),
    );
  }
}
```

### 20. Flutter Progress Bar

Learn how to show progress indicators in Flutter applications using the CircularProgressIndicator widget.

### Eample:

```dart

import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  bool isLoading = false;

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Progress Bar Example'),
        ),
        body: Center(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              ElevatedButton(
                onPressed: () {
                  setState(() {
                    isLoading = !isLoading;
                  });
                },
                child: Text(isLoading ? 'Stop Loading' : 'Start Loading'),
              ),
              SizedBox(height: 20),
              if (isLoading) CircularProgressIndicator(),
            ],
          ),
        ),
      ),
    );
  }
}

```


[Day 6 >>]()


❤️👨‍💻❤️ HAPPY CODING ❤️😇❤️


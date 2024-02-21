<div align="center">
<img height="100%" src="https://i.ibb.co/6srHHVp/flutter.webp" />
</div>

<div align="center">

  <h1>Day - 06 in Flutter</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/coding-ranjith-97b6ab238">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>

  <a class="header-badge" target="_blank" href="https://youtube.com/@coding-ranjith">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=Youtube&logo=youtube&style=social">
  </a>

<sub>Author: <a href="https://www.linkedin.com/in/coding-ranjith-97b6ab238" target="_blank">Coding Ranjith</a><br>
<small>February to March, 2024</small></sub>

</div>

## Day 6 Topics:

21. **Flutter Snackbar**
    - Understanding how to display snackbars in Flutter applications for showing temporary messages or notifications.
    - Example: Showing a snackbar with an undo option after an action.

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
          title: Text('Snackbar Example'),
        ),
        body: Center(
          child: ElevatedButton(
            onPressed: () {
              _showSnackbar(context);
            },
            child: Text('Show Snackbar'),
          ),
        ),
      ),
    );
  }

  void _showSnackbar(BuildContext context) {
    ScaffoldMessenger.of(context).showSnackBar(
      SnackBar(
        content: Text('This is a snackbar'),
        duration: Duration(seconds: 2),
        action: SnackBarAction(
          label: 'Undo',
          onPressed: () {
            // Add action here
            print('Undo action pressed');
          },
        ),
      ),
    );
  }
}
```

22. **Flutter Tooltip**
    - Exploring the Tooltip widget for providing additional information when users hover over a widget.
    - Example: Adding tooltips to buttons and icons for explaining their functionality.

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
          title: Text('Tooltip Example'),
        ),
        body: Center(
          child: Tooltip(
            message: 'This is a tooltip',
            child: IconButton(
              icon: Icon(Icons.info),
              onPressed: () {
                // Add onPressed action here
                print('IconButton pressed');
              },
            ),
          ),
        ),
      ),
    );
  }
}
```

23. **Flutter Slider**
    - Learning how to implement sliders in Flutter applications for selecting a value from a range.
    - Example: Adjusting the volume level with a slider widget.

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
  double _value = 0.0;

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Slider Example'),
        ),
        body: Center(
          child: Slider(
            value: _value,
            onChanged: (newValue) {
              setState(() {
                _value = newValue;
              });
            },
            min: 0.0,
            max: 100.0,
          ),
        ),
      ),
    );
  }
}
```

24. **Flutter Switch**
    - Understanding how to create toggle switches in Flutter applications for turning options on or off.
    - Example: Enabling dark mode with a switch widget.

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
  bool _darkMode = false;

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: _darkMode ? ThemeData.dark() : ThemeData.light(),
      home: Scaffold(
        appBar: AppBar(
          title: Text('Switch Example'),
        ),
        body: Center(
          child: Switch(
            value: _darkMode,
            onChanged: (newValue) {
              setState(() {
                _darkMode = newValue;
              });
            },
          ),
        ),
      ),
    );
  }
}
```

25. **Flutter Charts**
    - Introduction to using charts for data visualization in Flutter applications using libraries like fl_chart.
    - Example: Displaying sales data using a line chart.

```dart
import 'package:flutter/material.dart';
import 'package:fl_chart/fl_chart.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Chart Example'),
        ),
        body: Center(
          child: LineChart(
            LineChartData(
              lineBarsData: [
                LineChartBarData(
                  spots: [
                    FlSpot(0, 1),
                    FlSpot(1, 3),
                    FlSpot(2, 2),
                    FlSpot(3, 4),
                    FlSpot(4, 3),
                  ],
                  isCurved: true,
                  colors: [Colors.blue],
                  barWidth: 4,
                  belowBarData: BarAreaData(show: false),
                ),
              ],
              titlesData: FlTitlesData(show: false),
            ),
          ),
        ),
      ),
    );
  }
}
```

26. **Bottom Navigation Bar**
    - Exploring the BottomNavigationBar widget for navigation between multiple screens or sections of an app.
    - Example: Implementing a bottom navigation bar with different tabs.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: BottomNavBarDemo(),
    );
  }
}

class BottomNavBarDemo extends StatefulWidget {
  @override
  _BottomNavBarDemoState createState() => _BottomNavBarDemoState();
}

class _BottomNavBarDemoState extends State<BottomNavBarDemo> {
  int _selectedIndex = 0;

  void _onItemTapped(int index) {
    setState(() {
      _selectedIndex = index;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Bottom Navigation Bar Example'),
      ),
      body: Center(
        child: Text('Selected Index: $_selectedIndex'),
      ),
      bottomNavigationBar: BottomNavigationBar(
        items: const <BottomNavigationBarItem>[
          BottomNavigationBarItem(
            icon: Icon(Icons.home),
            label: 'Home',
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.search),
            label: 'Search',
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.settings),
            label: 'Settings',
          ),
        ],
        currentIndex: _selectedIndex,
        onTap: _onItemTapped,
      ),
    );
  }
}
```

27. **Flutter Themes**
    - Learning how to apply themes to Flutter applications for consistent styling and branding.
    - Example: Applying a custom theme with specific colors and fonts.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData(
        primaryColor: Colors.blue,
        accentColor: Colors.orange,
        fontFamily: 'Roboto',
      ),
      home: ThemeDemo(),
    );
  }
}

class ThemeDemo extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Theme Example'),
      ),
      body: Center(
        child: Text(
          'Custom Theme Demo',
          style: TextStyle(
            fontSize: 24,
            fontWeight: FontWeight.bold,
          ),
        ),
      ),
    );
  }
}
```

28. **Flutter Table**
    - Understanding how to create tables in Flutter applications for displaying data in rows and columns.
    - Example: Creating a timetable with rows for days and columns for time slots.

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: TableDemo(),
    );
  }
}

class TableDemo extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Table Example'),
      ),
      body: Center(
        child: Table(
          border: TableBorder.all(),
          children: [
            TableRow(
              children: [
                TableCell(
                  child: Center(
                    child: Text('Row 1, Column 1'),
                  ),
                ),
                TableCell(
                  child: Center(
                    child: Text('Row 1, Column 2'),
                  ),
                ),
              ],
            ),
            TableRow(
              children: [
                TableCell(
                  child: Center(
                    child: Text('Row 2, Column 1'),
                  ),
                ),
                TableCell(
                  child: Center(
                    child: Text('Row 2, Column 2'),
                  ),
                ),
              ],
            ),
          ],
        ),
      ),
    );
  }
}
```

29. **Flutter Calendar**
    - Exploring packages and libraries for integrating calendars into Flutter applications.
    - Example: Integrating a calendar widget to display events and appointments.

```dart
import 'package:flutter/material.dart';
import 'package:table_calendar/table_calendar.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: CalendarDemo(),
    );
  }
}

class CalendarDemo extends StatefulWidget {
  @override
  _CalendarDemoState createState() => _CalendarDemoState();
}

class _CalendarDemoState extends State<CalendarDemo> {
  CalendarFormat _calendarFormat = CalendarFormat.month;
  DateTime _focusedDay = DateTime.now();
  DateTime? _selectedDay;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Calendar Example'),
      ),
      body: TableCalendar(
        calendarFormat: _calendarFormat,
        focusedDay: _focusedDay,
        firstDay: DateTime(2010),
        lastDay: DateTime(2030),
        selectedDayPredicate: (day) {
          return isSameDay(_selectedDay, day);
        },
        onDaySelected: (selectedDay, focusedDay) {
          setState(() {
            _selectedDay = selectedDay;
            _focusedDay = focusedDay;
          });
        },
        onPageChanged: (focusedDay) {
          _focusedDay = focusedDay;
        },
      ),
    );
  }
}
```

30. **Flutter Animation**
    - Introduction to animation in Flutter for creating interactive and engaging user interfaces.
    - Example: Adding animated transitions between screens and widgets.
```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: AnimationDemo(),
    );
  }
}

class AnimationDemo extends StatefulWidget {
  @override
  _AnimationDemoState createState() => _AnimationDemoState();
}

class _AnimationDemoState extends State<AnimationDemo>
    with SingleTickerProviderStateMixin {
  late AnimationController _controller;
  late Animation<double> _animation;

  @override
  void initState() {
    super.initState();
    _controller = AnimationController(
      duration: Duration(seconds: 1),
      vsync: this,
    );
    _animation = Tween<double>(begin: 0, end: 300).animate(_controller)
      ..addListener(() {
        setState(() {});
      });
    _controller.forward();
  }

  @override
  void dispose() {
    _controller.dispose();
    super.dispose();
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Animation Example'),
      ),
      body: Center(
        child: Container(
          width: _animation.value,
          height: _animation.value,
          color: Colors.blue,
        ),
      ),
    );
  }
}
```

[Day 7 >>]()


❤️👨‍💻❤️ HAPPY CODING ❤️😇❤️
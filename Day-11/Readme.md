<div align="center">
  <img height="100%" src="https://i.ibb.co/6srHHVp/flutter.webp" />
</div>

<div align="center">
  <h1>Day - 11 in Flutter</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/coding-ranjith-97b6ab238">
    <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://youtube.com/@coding-ranjith">
    <img src="https://img.shields.io/badge/style--5eba00.svg?label=Youtube&logo=youtube&style=social">
  </a>
  <sub>Author: <a href="https://www.linkedin.com/in/coding-ranjith-97b6ab238" target="_blank">Coding Ranjith</a><br>
  <small>February to March, 2024</small>
  </sub>
</div>

## Day 11 Topics:

1. **Flutter Notifications**
   - Introduction to handling notifications in Flutter applications.
   - Displaying local and push notifications using packages like `flutter_local_notifications` and `firebase_messaging`.

```dart
import 'package:flutter_local_notifications/flutter_local_notifications.dart';

Future<void> showNotification() async {
  var android = AndroidNotificationDetails(
      'channel id', 'channel NAME', 'CHANNEL DESCRIPTION');
  var iOS = IOSNotificationDetails();
  var platform = NotificationDetails(android: android, iOS: iOS);
  await flutterLocalNotificationsPlugin.show(
    0,
    'New Notification',
    'Flutter is awesome!',
    platform,
    payload: 'Welcome to Flutter Notifications',
  );
}
```

2. **Flutter Permissions**
   - Understanding how to request and handle permissions in Flutter apps.
   - Managing permissions for accessing device features like camera, location, contacts, etc.

```dart
import 'package:permission_handler/permission_handler.dart';

Future<void> requestCameraPermission() async {
  var status = await Permission.camera.status;
  if (!status.isGranted) {
    await Permission.camera.request();
  }
}
```

3. **Flutter File Handling**
   - Learning how to read from and write to files in Flutter apps.
   - Working with local files and directories for data storage and retrieval.

```dart
import 'dart:io';

Future<void> writeFile() async {
  final file = File('path_to_file.txt');
  await file.writeAsString('Hello, Flutter!');
}
```

4. **Flutter Connectivity**
   - Exploring methods to check network connectivity status in Flutter.
   - Handling different network states and scenarios in the app.

```dart
import 'package:connectivity/connectivity.dart';

Future<void> checkConnectivity() async {
  var connectivityResult = await (Connectivity().checkConnectivity());
  if (connectivityResult == ConnectivityResult.mobile) {
    print('Mobile data connected');
  } else if (connectivityResult == ConnectivityResult.wifi) {
    print('WiFi connected');
  }
}
```


5. **Flutter Background Tasks**
   - Introduction to executing background tasks in Flutter applications.
   - Running background tasks like data syncing, periodic updates, etc.

```dart
import 'package:background_fetch/background_fetch.dart';

void backgroundFetch() {
  BackgroundFetch.registerFetch(onFetch);
}

void onFetch(String taskId) async {
  print('[Background Fetch] Event received: $taskId');
  BackgroundFetch.finish(taskId);
}
```

6. **Flutter Local Database**
   - Understanding the implementation of local databases in Flutter apps.
   - Using packages like `sqflite` or `moor` for SQLite database operations.

```dart
import 'package:sqflite/sqflite.dart';
import 'package:path/path.dart';

Future<void> createDatabase() async {
  final database = openDatabase(
    join(await getDatabasesPath(), 'my_database.db'),
    onCreate: (db, version) {
      return db.execute(
        'CREATE TABLE my_table(id INTEGER PRIMARY KEY, name TEXT)',
      );
    },
    version: 1,
  );
}
```

7. **Flutter Settings Screen**
   - Creating a settings screen in Flutter for managing app preferences.
   - Implementing features like theme selection, language settings, etc.

```dart
import 'package:flutter/material.dart';
import 'package:shared_preferences/shared_preferences.dart';

class SettingsScreen extends StatefulWidget {
  @override
  _SettingsScreenState createState() => _SettingsScreenState();
}

class _SettingsScreenState extends State<SettingsScreen> {
  bool _darkMode = false;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Settings'),
      ),
      body: SwitchListTile(
        title: Text('Dark Mode'),
        value: _darkMode,
        onChanged: (value) async {
          SharedPreferences prefs = await SharedPreferences.getInstance();
          setState(() {
            _darkMode = value;
            prefs.setBool('darkMode', value);
          });
        },
      ),
    );
  }
}
```
8. **Flutter Push Notifications**
   - Understanding the process of sending and receiving push notifications in Flutter apps.
   - Integrating Firebase Cloud Messaging (FCM) for push notification support.

```dart
// Firebase Cloud Messaging setup and usage
// Example code can be found in Firebase documentation.
```

9. **Flutter Device Sensors**
   - Exploring device sensors like accelerometer, gyroscope, compass, etc., in Flutter.
   - Accessing sensor data for building sensor-driven apps.

```dart
import 'package:sensors/sensors.dart';

void listenToAccelerometer() {
  accelerometerEvents.listen((AccelerometerEvent event) {
    print('Accelerometer: $event');
  });
}
```

10. **Flutter Geolocation**
    - Learning how to integrate geolocation features into Flutter apps.
    - Using packages like `geolocator` for location tracking and map integration.

```dart
import 'package:geolocator/geolocator.dart';

Future<void> getCurrentLocation() async {
  Position position = await Geolocator.getCurrentPosition(
      desiredAccuracy: LocationAccuracy.high);
  print('Latitude: ${position.latitude}, Longitude: ${position.longitude}');
}
```

## Resources:

- [Flutter Local Notifications Package](https://pub.dev/packages/flutter_local_notifications)
- [Firebase Cloud Messaging (FCM) Documentation](https://firebase.google.com/docs/cloud-messaging)
- [Flutter Permissions Plugin](https://pub.dev/packages/permission_handler)
- [Flutter File Handling Guide](https://flutter.dev/docs/cookbook/persistence/reading-writing-files)
- [Flutter Connectivity Package](https://pub.dev/packages/connectivity)
- [Flutter Background Tasks Package](https://pub.dev/packages/background_fetch)
- [Flutter Local Database (sqflite) Package](https://pub.dev/packages/sqflite)
- [Flutter Settings Screen Implementation Guide](https://flutter.dev/docs/cookbook/design/themes)
- [Flutter Push Notifications with FCM](https://firebase.flutter.dev/docs/messaging/usage)
- [Flutter Device Sensors Package](https://pub.dev/packages/sensors)
- [Flutter Geolocator Package](https://pub.dev/packages/geolocator)

❤️👨‍💻❤️ HAPPY CODING ❤️😇❤️

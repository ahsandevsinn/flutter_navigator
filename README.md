
# flutter_navigator Package


Welcome to the flutter_navigator package! This package is designed to simplify and streamline navigation in your Flutter applications, making your code more reusable and easier to maintain.



## Features

- Simplified Navigation: Reduce the amount of boilerplate code needed for navigation.

- Reusability: Write navigation code once and reuse it across your entire application.

- Enhanced Readability: Cleaner and more readable codebase by using a simplified navigation syntax.



## Installation

Add the following to your pubspec.yaml file:


```bash
  dependencies:
  flutter_navigator: ^1.0.0
```
Then run:
```bash
  flutter pub get

```
## Usage
With the flutter_navigator package, you can navigate between pages using a much simpler syntax. Instead of writing the complete syntax every time, such as:

```bash
 Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondRoute()),
);
```
You can use:

```bash
push(context, HomePage());
```

## Example

```bash
import 'package:flutter/material.dart';
import 'package:flutter_navigator/flutter_navigator.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: HomePage(),
    );
  }
}

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Home Page'),
      ),
      body: Center(
        child: ElevatedButton(
          onPressed: () {
            push(context, SecondPage());
          },
          child: Text('Go to Second Page'),
        ),
      ),
    );
  }
}

class SecondPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Second Page'),
      ),
      body: Center(
        child: ElevatedButton(
          onPressed: () {
            push(context, HomePage());
          },
          child: Text('Back to Home Page'),
        ),
      ),
    );
  }
}
```
## Benefits

Contributions are welcome! Please fork this repository and submit a pull request for any features, bug fixes, or enhancements.


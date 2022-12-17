# Switch-Button


import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    home: AboutPage(),
  ));
}

class AboutPage extends StatefulWidget {
  @override
  State<AboutPage> createState() => _AboutPageState();
}

class _AboutPageState extends State<AboutPage> {
  bool _switchValue = true;
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: _switchValue ? Colors.white : Colors.black,
      body: Center(
        child: Container(
          height: 200,
          width: 200,
          color: _switchValue ? Colors.pink : Colors.red,
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              // Text(
              //   'Switch button',
              //   style: TextStyle(fontSize: 30, color: Colors.black),
              // ),
              Switch(
                  value: _switchValue,
                  activeColor: Colors.black,
                  activeTrackColor: Colors.lightBlue,
                  onChanged: (newvalue) {
                    setState(() {
                      _switchValue = newvalue;
                    });
                  })
            ],
          ),
        ),
      ),
    );
  }
}

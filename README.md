import 'package:flutter/material.dart';
void main() => runApp(myapp());

class myapp extends StatefulWidget {
  @override
  _myappState createState() => _myappState();
}

class _myappState extends State<myapp> {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData(
        primaryColor: Colors.black,
      ),
      debugShowCheckedModeBanner: false,
      title: "My Home",
      home: homepage(),
      
    );
  }
}
class homepage extends StatefulWidget {
  @override
  _homepageState createState() => _homepageState();
}

class _homepageState extends State<homepage> {
  int dataToChange = 0;

  void datachange() {
  setState(() {
    dataToChange += 1;
  });

  }
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(
          "My App"
        ),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              "$dataToChange", style: TextStyle(fontSize: 24.0,
              fontWeight: FontWeight.bold),
            ),
            RaisedButton(
              onPressed: (
                
              ) {
                datachange();

              },
              child: Text(
                "Click Me", style: TextStyle(
                  fontSize: 24.0,
                  color: Colors.white
                ),
              ),
              color: Colors.cyan,
            )
          ],
        ),
      ),
      
    );
  }
}

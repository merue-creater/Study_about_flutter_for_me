//import 'dart:ffi'; -> Erase this code than fixed it.

import 'package:flutter/material.dart';

const List<String> list = <String>['One', 'Two', 'Three', 'Four'];

void main() {
  runApp(const MyApp()) ;
}

class  MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);
  @override
  Widget build(BuildContext context) {

    return MaterialApp(
      home: Scaffold(//상중하로 나눠주는 위젯
        appBar: AppBar(
          title: DropdownButton(
            items: const[
              DropdownMenuItem(value: 'one',child: Text('one',style: TextStyle(color: Colors.black),),),
              DropdownMenuItem(value: "two",child: Text("two"),),
          ],
            onChanged: null,
          ),
          actions:<Widget>[
            IconButton(
                icon: const Icon(Icons.zoom_in,color: Colors.black,),
              onPressed: (){}, iconSize: 40,
            ),
            IconButton(
                icon: const Icon(Icons.menu, color: Colors.black,),
              onPressed: () {},iconSize: 40,),
            IconButton(
              icon: const Icon(Icons.notifications, color: Colors.black,),
              iconSize: 40,
              onPressed: () {},)
          ],
          backgroundColor: Colors.white,
          //leading: Icon(Icons.star),//
        ),//상단에 들어갈 위젯

        body: Container(
          height: 150, padding: EdgeInsets.all(10),
          child: Row(
            children: [Image.asset('ViichanBear.png',width: 150,),
              Container(
                width: 300,
                child: Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: [
                    Text('챠니챠니',),
                    Text('VIichan'),
                    Text('700'),
                    Row(
                      mainAxisAlignment: MainAxisAlignment.end,
                      children: [
                        Icon(Icons.favorite),
                        Text('116')
                      ],
                    )
                  ],
                ),
              )
        ],
          ),

        ),
        //중단
        bottomNavigationBar: BottomAppBar(
          color: Colors.green,
          child: Row(
            children: [
              IconButton(icon: Icon(Icons.call),onPressed: () {},iconSize: 40,),
              IconButton(icon: Icon(Icons.home),onPressed: () {},iconSize: 40,),
              IconButton(icon: Icon(Icons.arrow_back),onPressed: () {},iconSize: 40,),
            ],
          )
        ),
        )
    );
  }
}

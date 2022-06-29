---
title: 35个好用的Flutter插件
abbrlink: 280
date: 2022-01-28 23:11:49
updated: 2022-01-28 23:11:49
tags:
categories:
keywords:
description:
top_img:
comments:
cover:
toc:
toc_number:
toc_style_simple:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
---

## 视频

[Top 35 Flutter Widgets](https://www.youtube.com/watch?v=M9J-JJOuyE0)

[30 Flutter Tips and Tricks (2)](https://www.youtube.com/watch?v=Kq5ZsygfWAc)

[69 Flutter Tips and Tricks (3)](https://www.youtube.com/watch?v=hDVZykwl13I)

## stepper: ^0.0.2

步骤跳转

```dart
void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: MyHomePage(
        title: "Demo App",
      ),
    );
  }
}

class MyHomePage extends StatefulWidget {
  MyHomePage({Key key, this.title}) : super(key: key);

  final String title;

  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Padding(
        padding: const EdgeInsets.only(
          left: 16,
          right: 16,
        ),
        child: HorizontalStepper(
            steps: [
              HorizontalStep(
                title: "Step 1",
                widget: Center(
                  child: Text("Step 1"),
                ),
                state: HorizontalStepState.SELECTED,
                isValid: true,
              ),
              HorizontalStep(
                title: "Step 2",
                widget: Center(
                  child: Text("Step 2"),
                ),
                isValid: true,
              ),
              HorizontalStep(
                title: "Step 3",
                widget: Center(
                  child: Text("Step 3"),
                ),
                isValid: true,
              ),
              HorizontalStep(
                title: "Step 4",
                widget: Center(
                  child: Text("Step 4"),
                ),
                isValid: true,
              )
            ],
            selectedColor: const Color(0xFF4FE2C0),
            unSelectedColor: Colors.grey.shade400,
            leftBtnColor: const Color(0xffEA7F8B),
            rightBtnColor: const Color(0xFF4FE2C0),
            selectedOuterCircleColor: const Color(0xFF40A8F4),
            type: Type.TOP,
            circleRadius: 30,
            onComplete: () {
              print("completed");
            },
            textStyle: TextStyle(
              fontSize: 14,
              fontWeight: FontWeight.bold,
              decoration: null,
            )),
      ),
    );
  }
}
```

## FittedBox

一个可以让内部文字按比例缩放的Material的 Widget

```dart
Container(
	width: 300,
  height:100,
  child: FittedBox(
  	child: Text('FittedBox',style: TextStyle(fontSize: 100,color:Colors.white))
  ),
  
)
```



## flutter_zoom_drawer: ^2.2.2+1

缩放式测栏

```dart
ZoomDrawer(
      controller: ZoomDrawerController,
      style: DrawerStyle.DefaultStyle,
      menuScreen: MENU_SCREEN,
      mainScreen: MAIN_SCREEN,
      borderRadius: 24.0,
      showShadow: true,
      angle: -12.0,
      backgroundColor: Colors.grey[300],
      slideWidth: MediaQuery.of(context).size.width*.65,
      openCurve: Curves.fastOutSlowIn,
      closeCurve: Curves.bounceIn,
    )
```

# Bottom_Navigation_code

code for Bottom Navigation bar 

// ignore_for_file: prefer_const_constructors

import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';
import 'package:navigation_bar/main.dart';


void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'Bottom Navigation bar',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: const MyHomePage(),
    );
  }
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key,});
  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

var nameArray=["Manzar", "Shehzad", "Usama", "Haseeb", "Saqib", "Mustafa", "Noman", "Mohsin", "Usama", "All Class",];
var imagesList =[
  Image.network("https://i0.wp.com/eacademy.edu.vn/wp-content/uploads/2023/photos1/1/WhatsApp-DP-Cute-268.jpg?resize=1080%2C1350&ssl=1"),
  Image.network("https://ashisheditz.com/wp-content/uploads/2023/09/cute-whatsapp-dp.jpg"),
  Image.network("https://i.pinimg.com/564x/90/8f/76/908f76ea93c49062710f069f582421e1.jpg"),
  Image.network("https://goodstatus.in/wp-content/uploads/2023/01/29-1.webp"),
  Image.network("https://cdn4.sharechat.com/compressed_gm_40_img_47114_a0a7ce5_1694520044647_sc.jpg?tenant=sc&referrer=pwa-sharechat-service&f=647_sc.jpg"),
  Image.network("https://topclasstrading.com/wp-content/uploads/2023/10/cute_boy_dp_image-3490.jpg"),
  Image.network("https://cdn.statusqueen.com/dpimages/thumbnail/cute_dp_image-3721.jpg"),
  Image.network("https://cdn.statusqueen.com/dpimages/thumbnail/cute_dp_image-3536.jpg"),
  Image.network("https://cdn.statusqueen.com/dpimages/thumbnail/cute_girl_dp_image-3685.jpg"),
  Image.network("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTC6sNe-dnKVY8GijAm_DblKWcpzu9OSXa8Z-iwNaQiAJ5jtgBWGUk-KcEYnjX24dU4o74&usqp=CAU"),];

class _MyHomePageState extends State<MyHomePage> {

  int countNumbers = 0;
  onclick(int value){
    setState(() {
      countNumbers = value;
    });
  }
  List<Widget> list= [
  SizedBox(
    height: double.infinity,
    width: double.infinity,
    child: ListView.separated(itemBuilder: (context, index) {

    return const Card(
      child:  ListTile(
        leading: CircleAvatar(
          radius: 30,
          backgroundImage: imagesList[index].image,
          child: Icon(Icons.person_2_rounded),
        ),
        title: Text(nameArray.elementAt(index)),
        subtitle: Text("New Message"),
        trailing: Icon(Icons.circle,color: Colors.green,),
      ),
    );},
    separatorBuilder:(context, index) {
      return const Divider(height: 5,thickness: 1,color: Colors.pink,);
    }, itemCount: nameArray.length,

  ),),
    const SizedBox(height: double.infinity,width: double.infinity,child: Center(child: Text("Search tab")),),
    const SizedBox(height: double.infinity,width: double.infinity,child: Center(child: Text("Add Tab")),),
    Container(
      height: double.infinity,
      width: double.infinity,
      color: Colors.black12,
      child: Column(
        children:[
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Container(
              width: double.infinity,
              height: 150,
              decoration: BoxDecoration(
                color: Colors.white,
                borderRadius: BorderRadius.circular(10),
              ),
              child: Padding(
                padding: const EdgeInsets.all(8.0),
                child: Center(
                  child: ListTile(
                    mouseCursor: MaterialStateMouseCursor.clickable,
                    leading: CircleAvatar(
                      radius: 40,
                      backgroundImage: NetworkImage("https://cdn.statusqueen.com/dpimages/thumbnail/cute_dp_image-3721.jpg"),
                    ),
                    title: Text("Mohsin Raza",style: TextStyle(fontSize: 22,fontWeight: FontWeight.bold,color: Colors.black,),),
                    subtitle: Text("a Flutter Developer",style: TextStyle(color: Colors.green),),
                    trailing: Icon(Icons.edit),
                  ),
                ),
              ),
            ),
          ),
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Container(
              height: 80,
            width: double.infinity,
            decoration: BoxDecoration(
              borderRadius: BorderRadius.circular(10),
              color: Colors.white,
            ),
              child: Center(
                child: ListTile(
                  leading: Icon(CupertinoIcons.settings_solid,size: 40,),
                  title: Text("Setting",style: TextStyle(color: Colors.black,fontSize: 16),),
                ),
              ),
            ),
          ),
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Container(
              height: 80,
              width: double.infinity,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10),
                color: Colors.white,
              ),
              child: Center(
                child: ListTile(
                  leading: Icon(CupertinoIcons.settings_solid,size: 40,),
                  title: Text("Setting",style: TextStyle(color: Colors.black,fontSize: 16),),
                ),
              ),
            ),
          ),
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Container(
              height: 80,
              width: double.infinity,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10),
                color: Colors.white,
              ),
              child: Center(
                child: ListTile(
                  leading: Icon(CupertinoIcons.settings_solid,size: 40,),
                  title: Text("Setting",style: TextStyle(color: Colors.black,fontSize: 16),),
                ),
              ),
            ),
          ),
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Container(
              height: 80,
              width: double.infinity,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(10),
                color: Colors.white,
              ),
              child: Center(
                child: ListTile(
                  leading: Icon(CupertinoIcons.settings_solid,size: 40,),
                  title: Text("Setting",style: TextStyle(color: Colors.black,fontSize: 16),),
                ),
              ),
            ),
          )

        ]
      ),),

];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        leading: const Icon(Icons.menu_outlined),
        backgroundColor: Colors.green.shade400,
        title: const Text("myChat", style: TextStyle(color: Colors.white,fontSize: 14),),
        centerTitle: true,
        actions: const [
          Padding(
            padding: EdgeInsets.all(8.0),
            child: Icon(Icons.message_rounded),
          ),
        ],
      ),
      bottomNavigationBar: BottomNavigationBar(items: const [
        BottomNavigationBarItem(icon: Icon(CupertinoIcons.home,),label: 'Home'),
        BottomNavigationBarItem(icon: Icon(CupertinoIcons.search,),label: 'Search'),
        BottomNavigationBarItem(icon: Icon(CupertinoIcons.add_circled,),label: "add"),
        BottomNavigationBarItem(icon: Icon(CupertinoIcons.person_alt_circle,),label: 'profile'),

      ],

       showUnselectedLabels: true,
       unselectedItemColor: Colors.black,
       unselectedLabelStyle: const TextStyle(color: Colors.black,fontSize: 14),
       mouseCursor: MaterialStateMouseCursor.clickable,
        selectedItemColor: Colors.green.shade400,
        backgroundColor: Colors.white,
        currentIndex: countNumbers,
        onTap: onclick,

      ),
      body:list.elementAt(countNumbers),

    );
  }
}

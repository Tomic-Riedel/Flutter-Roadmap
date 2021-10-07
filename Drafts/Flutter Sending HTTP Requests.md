# Flutter Sending HTTP Requests

Now coming to most important thing that you should take note of, is that how you going to communicate with third party servers/services. What do I mean by that is how you going to send data over the internet if your server is in different state or country. **Any idea?**

Now thats where **HTTP**(HyperText Transfer Protocol) comes into play. 
There are different types of operations you can perform like:
- **GET** : To get or to retrieve data.
- **POST** : To add new data.
- **PUT** : For checking if resource is exists then update , else create new resource.
- **PATCH** : To update existing resource.
- **DELETE**: To delete existing resource.
We usually call these operations as **CRUD** (create, read, update and delete). After some basic theory lets move on to practical knowledge.

### Sending HTTP request from Flutter
For sending HTTP requests dart team have created a wonderful package which makes developers work easy. 
> [http package](https://pub.dev/packages/http "http") 

Using this package you can perform all the **CRUD** operations.

#### All CRUD operations Step by Step 
1. [This article](https://flutter.dev/docs/cookbook/networking/fetch-data "This article") will walk you through how to **retrieve** or to **GET data from servers**.
2. [This article](https://flutter.dev/docs/cookbook/networking/send-data "This article") will walk you through how to **send** or to **POST data to servers**.
3. [This article](https://flutter.dev/docs/cookbook/networking/update-data "This article") will walk you through how to **update** or to **PUT and PATCH data to servers**.
4. [This article](https://flutter.dev/docs/cookbook/networking/delete-data "This article") will walk you through how to **remove** or to **DELETE data from servers**.

### Some advance concepts
Now you have learned how to perform all the CRUD operations. Clap for yourself beacuse you are 80% done to master the HTTP concept.

Now comes the tricky part. Lets say you are getting huge JSON data from your server and parsing these JSON takes time. So sometimes it might create some buggy UI or jank to avoid this we usually isolate these expensive computation from UI and do the work in background.
So to parse JSON in background we can follow this tutorial provided by Flutter team https://flutter.dev/docs/cookbook/networking/background-parsing .

By now you have become PRO in handling any kind of HTTP request.

And you can learn more about networking by following [this link](https://flutter.dev/docs/cookbook#networking "this link.").

And **do not** forget [Flutter official docs](https://flutter.dev/docs "flutter official docs") and [Flutter official cookbook](https://flutter.dev/docs/cookbook "Flutter official cookbook") are your best friends to learn flutter.



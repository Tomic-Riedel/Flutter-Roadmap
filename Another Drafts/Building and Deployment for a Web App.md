## Debugging, Building and Deployment for a Flutter Web App
Flutter's code for Web and Mobile it's the same! Do not forget that. When you code a mobile application with Flutter, you simultaneously create the code for a web application,, but, you have to **compile it to Javascript code**, first.

### Debugging

#### Enabling Flutter Web Support
First, you have to enable Flutter Web Feature into your enviroment. Be sure you have [**Flutter 2.0**](https://flutter.dev/docs/development/tools/sdk/release-notes/release-notes-2.0.0), so, first upgrade you're Flutter version with `flutter upgrade` into your terminal.

Newest versions of Flutter enable automatically the web support, but, be sure with `flutter config --enable-web` into your terminal.

Finally, to create the folders of web support, position into your flutter project, and run `flutter create .` into the terminal. With this command, you make sure that the **yourProject/web/** folder is now active.

#### Running your Web App
As you know, Flutter only be able to make [**Progressive Web Applications**](https://web.dev/progressive-web-apps/), i.e **Single Page Applications**; keep this in mind when deciding if Flutter Web is ideal for your own project.

If you run `flutter devices` into your terminal, you would be seeing some **web navigator** as connected devices; like **Chrome**, or **Edge**. In this case, do `flutter run -d <navigator_name>` e.g, if you have **Chrome** connected, do:

    flutter run -d chrome

Now, you're running your app in **debbug mode** in a web nagivator! Flutter Web Support brings the **hot reload** tool, so, code in real time your web application.

### Bulding
Have you finished code your app, and do you want to release it to the public? You have to build it first. And take care of the options you have.

#### Web Renders
Now, with **Flutter 2.5.2**, you can choose between two different renderers. This renders give you the possibility to manage your app performance into the web navigators:

> **HTML renderer**
>
>Uses a combination of **HTML elements,** CSS, Canvas elements, and SVG elements. This renderer has a **smaller download size.**
>
> **CanvasKit renderer**
>
> This renderer is fully **consistent with Flutter mobile and desktop,** has **faster performance** with higher widget density, but **adds about 2MB in download size.**

If you do not specify the web render in a debugging or building, you are **optimizing for download size** on mobile browsers and optimizing for **performance on desktop browsers**, with the auto-default render.


#### Bulding with a Web Render
Have you already chosen it? Now, if you're sure to realease your app, do:

    flutter build web --web-renderer <renderer_name> --release
For **HTML** renderer:

    flutter build web --web-renderer html --release
For **CanvasKit** renderer:

    flutter build web --web-renderer canvaskit --release

You can try the renders in debbug and profile mode, with:

    flutter run -d chrome --web-renderer <renderer-name>
    
    flutter run -d chrome --web-renderer <renderer-name> --profile

When you build your app, a new directory has created: **yourProject/build/web/** 👈🏻 This is the folder that contains your web app; the folder you will deploy in internet.

### Deploying

With a deploying, you should give final details into your **build/web/** folder:

 1. Change the default **favicon.png** file. This icon will appear in the browser tab whe someone mark as favorite your web site. Use the same file name.

 2. Change the default icons of **/icons/** folder. You should use the same icon, but with **190 x 190** and **520 x 520** size respectively. When you add your own icons, be sure to use the same name of the default files.

 3. Go to **manifest.json** and change..
	 - **name.**
	 - **short-name.**
	 - **background-color.**
	 - **theme-color.**
	 - **description.**

	Attributes value, to your own app qualities.
	
4. Go to **version.json** and change the value of **version** and **build_number**, to your own data.
5. **VERY IMPORTANT:** Go to your **index.html** file, and find the **head >> base >> href** tag. On it, add the link of the **DNS server** on which the app will be hosted, and add a **/** int the start and end of the link.
For example:

	`<base href="/https://arhcoder.com/">`

	If you don't know this link, follow this...

### Deploying Free on GitHub Pages
For deploying a Flutter Web App, you have to create a **new repository** to host the build app **(not the dart code project),** and update on it your **/buld/web/** directory.

Default GitHub Page url is:

    https://yourGithubUser.github.io/yourRepositoryName/
For example:

    https://arhcoder.github.io/eight-queens-game-web/

Use these link to put into your **index.html >> head >> base >> href** tag, with the instructions previously given, ***BEFORE YOU UPDATE THE REPOSITORY WITH THE BUIL WEB APP.***

**NOTE: You can edit the html tags of the index.html file like title,  and description content, for more details.**

Now you are ready to deploy your Flutter Web App!
Push your files into your repository, then go to **Settings** in your GitHub repo, and find the headland **GitHub Pages**; on it, activate the GitHub Page option reading the **docs/** on the **master branch**.
<hr>

***YOU DID IT!***

Your Flutter Web App is now on the internet. You know what's the link, so, share with the world your new Web Application.

<hr>
💙

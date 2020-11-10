## Introduction to Ionic-react?

Hi everyone

Today I am going to explain how to get started with ionic framework to build different hybrid mobile application using your web technologies.

### What is the ionic framework?

Ionic Framework is an open-source UI toolkit for building performant, high-quality mobile and desktop apps using web technologies — HTML, CSS, and JavaScript — with integrations for popular frameworks like Angular, React, and Vue.JS.

Today we are going to cover how to use React and ionic to create a hybrid mobile application.

### Install ionic-cli from your terminal
```shell
npm install -g @ionic/cli
```

- Like we create a React app using `create-react-app`  we can create react app using ionic/cli from your terminal

```shell
ionic start
```

- Then you will be asked to select a framework you want to use for your application, I am choose to react but you can choose whatever you are comfortable.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604982661864/qhtY-0MVV.png)

- After you choose framework you are asked to enter a name for your project 

- After choosing the framework and project name you will be asked to select a template from the following list

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1605024964962/OUm4BMZoH.png)

- Templates are as follows

  - blank - An empty project with a single page
  - list     - A list based layout application 
  - sidemenu - A sidemenu based layout 
  - tabs - A tabs based layout
  - my-first-app - A tabs based fully functional photo Gallery application using native camera elements for android and IOS
  - conference  - A kitchen-sink application that shows off all Ionic features 

- Out of the above templates two are fully functional application those are my-first-app which is a photo gallery app, conference apps is a kitchen-sink application which show how much we can do with ionic framework using native elements from ionic.

-  For this tutorial I am choosing the my-first-app template and file structure will look like this.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1605027860572/RCEROuxcz.png)

- After the creation of template change the directory to the project folder and start the  project using the following command

```shell
ionic serve
```

- Now you can see the server started at `http://localhost:8100` and will open in your default browser the UI look something like this

- By default the application opens tab1 which will look something like this

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1605029207256/iOGAqFB7s.png)

- If you go to tab 2 where you can see the camera button floating, click on it will open your webcam and you can take a picture which will be stored locally memory. 
 
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1605029303301/GHtXWpfJ8.png)

 - Open browser dev tools,view the application different devices you can feel the native look, I have taken a simple photo using the webcam from my computer and all the images will be displayed in a grid format.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1605027629814/oo10VSSNG.png)

- Utill now we only created a web application so in order to create a native hybrid application you need to add either capacitor or Cordova for the project. We will look at those in the next part of this series and much more about ionic in general.

## Resources 

- [Ionic-docs](https://ionicframework.com/docs/)

> If you have any doubts related to this article or anything related to tech or software-engineering in general, drop a comment here or you can message me on twitter [@ksridhar02](https://twitter.com/ksridhar02).

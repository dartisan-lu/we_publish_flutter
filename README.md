# We Publish Flutter

This is a simple demo application, to show how easy it is to publish a Flutter Web Application on GitHub and make it public accessible. 

## First step:

Installation of Flutter. Simply follow the steps under https://docs.flutter.dev/get-started/install for your system.

## Second step:

create a new Flutter project. This contains a demo application, which also is published under this repository.

````shell
flutter create we_publish_flutter
````

we can already start locally the application in Chrome:

````shell
cd we_publish_flutter
flutter run -d chrome
````

## Third step:

Building the web application, in compiling the Dart/Flutter code to HTML/JS. 

`````shell
flutter build web
`````

This creates the artifacts in the folder ./build/web 

We copy now all the files under the ./docs of our project. 

### This finishes the development part, let now publish it :smile:

## First step:

Creating a Github account and/or public Repository. Follow the instructions to initialize the project with GIT

`````
git init

`````


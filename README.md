# We Publish Flutter

This is a simple documentation, to publish a Flutter Web application on GitHub pages and show/share it with friends and colleagues.

## First step:

Installation of Flutter. Simply follow the steps under https://docs.flutter.dev/get-started/install for our system.

## Second step:

Create a new Flutter project. This contains a demo application, which also is published under this repository:

````shell
flutter create we_publish_flutter
````

We can already start locally the application in Chrome:

````shell
cd we_publish_flutter
flutter run -d chrome
````

## Third step:

Building the web application, in building the HTML/JS files from our Dart/Flutter files:

`````shell
flutter build web --base-href /we_publish_flutter/
`````

:exclamation: :exclamation: :exclamation: *ATTENTION* :exclamation: :exclamation: :exclamation:

The parameter --base-href is needed as the page from our repository is not based on the root but the name we choose for our GitHub repository. It can be found in the generated index.html file:

````html
  <base href="/we_publish_flutter/">
````

This creates the artifacts in the folder ./build/web. 

We copy now all the files from ./build/web to ./docs (create the folder if it does not exist). 

### This finishes the development part, let now publish it :smile:

## First step:

Creating a GitHub account and/or public repository (https://github.com/). Follow the instructions from GitHub to initialize the project with GIT:

`````
git init
git add .
git remote add origin https://github.com/XXXXXXXXXXXXXXXX
git commit -m "Init Project"
git branch -M main
git push -u origin main
`````

All files are now pushed to GitHub.

## Second step:

Now we publish the web pages from the folder /docs

We edit the Settings (from the menubar) 

![](https://github.com/dartisan-lu/we_publish_flutter/blob/main/images/screenshot_settings.png?raw=true)

and select Pages on the left navigation bar:

![](https://github.com/dartisan-lu/we_publish_flutter/blob/main/images/screenshot_pages.png?raw=true)

Here we modify the parameters:

![](https://github.com/dartisan-lu/we_publish_flutter/blob/main/images/screenshot_pages_config.png?raw=true)

as follows:

* Deploy from a branch
* switch branch to main
* switch /(root) to /docs
* save

Now under *Actions* we can follow the build:

![](https://github.com/dartisan-lu/we_publish_flutter/blob/main/images/screenshot_settings.png?raw=true)

## Third step:

Congratulation, we published our page. We can access it now, by our domain / repos name, in my case: https://dartisan-lu.github.io/we_publish_flutter/

## Bonus step:

If you want to clean the statistics of the project, 

![](https://github.com/dartisan-lu/we_publish_flutter/blob/main/images/screenshot_statistic.png?raw=true)

and remove the generated files, add a file: *.gitattributes* in the root of the project with the values:

````
android/** linguist-vendored
ios/** linguist-vendored
web/** linguist-vendored
linux/** linguist-vendored
macos/** linguist-vendored
windows/** linguist-vendored
docs/** linguist-vendored
````

Now the project should be 100% Dart.

That's it, never was it so easy to create and publish a Web Application. 

Have fun, and have a happy programming day :smile:

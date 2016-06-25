# Getting started with React Native

Let's get you up to speed, dude. 

### What's React Native? 
React Native is a nifty framework that lets you build native apps with React (that [really cool library](https://facebook.github.io/react/) created by Facebook). So you'd essentially be able to create iOS and Android applications using JavaScript. 

### Why React Native? 
The great thing about React Native is that it emphasizes efficiency and a consistent developer experience across platforms. In other words, a lot of the logic you code for one platform is easily transferrable to another. You can learn a bunch of useful information about React Native [here](https://facebook.github.io/react-native).

### If React Native documentation already exists, then what the hell is this? 
First of all, relax. The purpose of this documentation is to:
  - be paired with Facebook's existing documentation
    - This is a really high-level overview on how to get working on Hearye quickly. I'll be glazing over a lot of important conceptual stuff
  - familiarize developers with Hearye's current development environment and practices 

Let's get started.

### Installation
We're going to be developing for iOS in this guide so you're going to want to have OS X. If you have Windows/Linux, tough shit; just kidding, here's an [alternate method for getting OS X using VirtualBox](http://lifehacker.com/5938332/how-to-run-mac-os-x-on-any-windows-pc-using-virtualbox) Once you have that, you'll need a few things to get started:
  - XCode
  - Homebrew
  - Node
  - Watchman
  - React Native Command Line Tools

#### XCode
  You cannot escape the wrath of XCode. XCode is a development environment to help create native iOS applications. We're just going to use it for its iOS simulator to run and test our apps. Go to the App Store, look up XCode, and download it. 

#### Homebrew
  Homebrew is a really, really, really good package manager for OS X. We're going to be using it to download some of the other stuff on our list. You can find details on how to install it [here](http://brew.sh/). 

#### Node
  Node is the one true dev language. We're going to be leveraging its package manager, NPM (Node package manager).
  In your terminal, use `brew install node`. If it says that you've already installed it, use `brew upgrade node` to install its latest version. None of that deprecated bullshit. 

#### Watchman
  Watchman is basically a service that watches files in a directory and triggers certain tasks on certain events. We'll need it for our app's build.
  Run `brew install watch` to download it. 

#### React Native CLI
  We need `react-native-cli` to do all those cool react-y things in the terminal like building and running our app. We're going to install it globally so you'll have it with you all the time!
  Run `npm install -g react-native-cli`. Run `react-native -v` to check the version and make sure you've installed it. 

### Initialize that shit
  To initialize our project, we could do `react-native init [name of project] --version [specified_version_number]`. In this case, we'll use `react-native init myDopeProject --version 0.24.0`. Then, wait for it to build. It's going to take quite a while. 
  After it's done, if you `ls` in your terminal, you can see it has created a folder with the project name you've specified. Navigate `cd` into this project folder.

### React Native Architecture
  If you check out the root file directory of your newly created project folder, you should see:
    ```
      index.ios.js
      android.ios.js 
      Android\
      iOS\
        \myDopeProject
          \myDopeProject.xcodeproj
        \myDopeProjectTests
      node_modules\
      package.json
    ```
  
  Since we'll be focusing on iOS in these docs, ignore the android stuff for now. `index.ios.js` is our main ios file, in which we'll be writing most of our code. In the `iOS\` folder, you'll find the the iOS assets needed to build and run the app, including the main project file `*.xcodeproj`. If you click into `*.xcodeproj`, you'll open the default code in your XCode environment. `package.json` is a file that keeps track of your npm dependencies, which are located in `node_modules`. It also defines scripts that automate certain tasks like running your app. If you check it, it defines a `start` script in the `scripts` object. You can run `npm start` to run that script. 

  ### Run that shit
  In your root directory in your terminal, run `npm start`. Your app will now build and you should be able to see it in your iOS Simulator.




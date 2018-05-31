# Lab Notes: Xcode Intro

## Learning Goals

* Students will be able to use all features in Xcode playgrounds
* Students will be able to navigate the main panes of Xcode (single view application), device sizes, and file tree
* Students will be able to add and modify UI elements on the storyboard
* Students will be able to run and navigate the simulator to see a small project on a device

## Plan

In this session you'll work guide the students through 2 activities - one on Xcode Playgrounds (15 minutes) and one on Xcode Projects (45 minutes).


### Getting Started - Playgrounds

* On your laptop, find the Xcode application by typing `cmd + space`, typing in `xcode`, then press return
* Click `Get started with a playground`
* Select 'blank', then click the blue `Next` in the bottom right corner
* You will be prompted to save this file. The default name is `MyPlayground` - let's change that to PlaygroundIntro, then click the blue `Create` button in the bottom right corner


### Playgrounds

Xcode Playgrounds are just what they sounds like - a safe place to play with code and see what happens. It's a great place to iterate on small problems so you can quickly see the outcome of a given method (without running an entire project). It's also a place that developers go to solve problems just for fun/practice. As we learn programming concepts this week, we will utilize Xcode Playgrounds here and there since it's a lot easier and quicker to run than a project.

#### Expected

* Create three variables - your name, age, and favorite thing to do during the summer.
* Print to the console a sentence that uses all three of your variables!

#### Extension

* Print the same sentence out three times, using a loop!


### Getting Started - Projects

* Use `cmd + q` to exit Xcode. We will now have a fresh start!
* On your laptop, find the Xcode application by typing `cmd + space`, typing in `xcode`, then press return.
* Click 'Create a new Xcode project'
* A box will pop up with some options. Make sure you are on it `iOS` tab (top left corner)
* Click `Single View App` (which should already be selected). Click the blue `Next` button in the bottom right corner to move on
* Give your project a name - for now, let's type in `ProjectsIntro` into the `Product Name` field. Click the blue `Next` button in the bottom right corner to move on
* A final box will pop up asking you to save this project to your computer. Make sure the checkbox next to `Source Control` IS checked (we will talk about what this means later), then click the blue `Create` button in the bottom right corner

### Projects

Xcode Projects provide us developers with a lot more tools! It allows us to create an entire application - from the User Interface (UI) to functionality with Swift code. There are multiple panes, and different things that can be used within each pane. It is a large application and can be overwhelming; we will learn the most important features, step by step.

#### Expected

* Use the file tree to navigate to the storyboard
* Add three UI Elements from the Object Library to your storyboard - two labels and a button. switch, or slider
* Run your application on the simulator
* Change the background color of your application
* Change the color or font or size of your UI Elements
* Re-run your application on the simulator - are your changes reflected?

#### Extension

* Add an icon image:
  - In your simulator, click to `home` button (circle at bottom center). Find your application by the `Product Name` you typed in earlier. What is the icon above it? Let's make a custom icon so your users have a visual to click on!
  - Go to [INSERT URL OR SOMETHING] and download the zip file with photos
  - In Xcode's Navigation Pane, click `Assets.xcassets`, then click `AppIcon` in the Document Outline
  - Using `Finder`, drag and drop the two images you would like to use for your icon (you need one that ends in -60@2x _and_ one that ends in -60@3x) into the 2x and 3x boxes right above the label for `iPhone App - iOS 7-11 - 60pt`
  - Re-run your simulator, click `home` and you should see your new icon!

* Still have work time? Find an image on Google Images and bring that into your project with an image UI Element

## Circle Back

As we close our tutorial time, we'll either write in our journals or discuss as a group:

- What is the difference between an Xcode Playground and Project? When would you want to use one or the other?
- What did you enjoy about building the UI?
- What questions do you still have about building a UI?

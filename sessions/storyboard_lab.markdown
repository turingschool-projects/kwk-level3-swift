# Lab Notes: StoryBoards

## Learning Goals

* Students will be able to add UI elements to the StoryBoard using the Object Library
* Students will be able to make UI look clean on all device sizes using constraints


## Plan

This lab is a time for you to explore Xcode's Object Library and build any single-page app you want! Be creative, goofy, or practice making the app you've been dreaming of.


### Getting Started

* On your laptop, find the Xcode application by typing `cmd + space`, typing in `xcode`, then press return
* Click `Create a new Xcode project`
* Under `Choose a template for your new project`, select `iOS`
* Under `Application`, select `Single View App`
* Click the blue `Next` button in the bottom right corner
* You will be prompted to save this file. For `Product Name`, type in "StoryBoards", then click the blue `Create` button in the bottom right corner


### StoryBoards

Xcode includes the tools to make the user interface (UI) of our app look the way we want it to. We first have to drag and drop items onto the StoryBoard from the Object Library, then we use constraints to make sure the objects look the way we want them to on any device!


#### Expected

Plan out an app (it could be one screen on your favorite app, the app you're dreaming about making, or just a few simple elements!) by drawing it out on a sketch paper. Have in mind which UI Objects you will need on your StoryBoard.

In your new project, drag and drop at least 3 UI Objects (View, Image, Label) in from the Object Library. Each time you add one, do the following:
- Check the appearance on the simulator
- Set constraints on each UI Object
- Check the simulator again

Now, add an icon image. Run in simulator to make sure it was loaded in correctly!

#### Extension

Start over! (You probably just want to create a new project to keep your old work.) Delete the ViewController from your StoryBoard and drag on a Navigation Controller. This should pull up 2 screens on your StoryBoard - a Navigation Controller pointing to a TableView. Delete the TableView, then drag on a View Controller. `ctrl + drag` from the Navigation to View, then select "View" to create a "segue" - (feel free to Google Xcode segues to learn more!)

Drag a 'Navigation Bar' onto the View Controller. Edit the title. Drag 1 or more Navigation Item onto the Navigation Bar - play around with the different icons that are built in that you can use!

Finish the UI for the rest of your app now that you have a Navigation Bar!


## Circle Back

As we close our tutorial time, we'll either write in our journals or discuss as a group:

- Provide some guiding questions to reflect on - should be a mix of technical and a reflection on challenges/how are you navigating bugs/what is your problem solving like, etc.

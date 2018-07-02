# Lab Notes: Build Your ViewFinder UI

## Learning Goals

* Students will implement their wireframes into a UI
* Students will create navigation controllers and segues


## Plan

In this lab, you will bring your wireframes to life!


### Getting Started

* On your laptop, find the Xcode application by typing `cmd + space`, typing in `xcode`, then press return
* Click `Create a new Xcode project`
* Under `Choose a template for your new project`, select `iOS`
* Under `Application`, select `Single View App`
* Click the blue `Next` button in the bottom right corner
* **!IMPORTANT!** You must check the `Use Core Data` box! **!IMPORTANT!**
* You will be prompted to save this file. For `Product Name`, type in "______" - whatever name your want to officially title your app, then click the blue `Create` button in the bottom right corner
* **!IMPORTANT!** You must check the `Create Git respository on Mac` box! **!IMPORTANT!**
* NOTE: This will be your ACTUAL project! From now on, you won't really be creating new projects, just opening this one up and working from wherever you left off.


### Build Your ViewFinder UI

Similar to our StoryBoard and Actions/Outlets lessons, we will need to start with the UI, then fill in the details as we go. So today's lab is focused on getting your UI set up!


#### Expected

* Delete the ViewController from the StoryBoard scene
* Delete ViewController.swift file from the Navigation Pane (move to trash)
* On the StoryBoard, drag on a TableViewController from the Object Library
* With the TableViewController selected, click Editor --> Embed In --> Navigation Controller
  - This will embed the view inside of a Navigation Controller, which will allow us to use a back button, and other similar buttons on the top of the page
* With the Navigation Controller selected, in the Utilities Pane, select the Attributes Inspector, scroll down to the View Controller section, and check the box next to `Is Initial View Controller`
![Use this as a reference if needed:](./slide_images/initial_view.png)

* _Run on your iPad to make sure it's working_

* In the Document Outline, click on the Navigation Item (under Table View Controller). Now, look at the Attributes Inspector in the Utilities Pane, and you should see a form for Title. Write the name of your app into that field.
![Use this as a reference if needed:](./slide_images/title_nav_item.png)

* Drag a `Bar Button Item` from the Object Library onto your Navigation Bar on the Table View. In the Utilities Pane, you can change the title under `Bar Item`. You can also use the drop-down menu title `System Item` to select aiOS icon.
* Drag a new `View Controller` onto your StoryBoard. `ctrl + click` then drag your `Add` button on the Table View over to your new View Controller. Select `show`. This is telling the computer, "when the user clicks on this `add` button, take them to this other view, please." This is called a `segue`.
![Use this as a reference if needed:](./slide_images/add_segue.gif)

* _Run on your iPad to make sure it's working_

* Drag a `Navigation Item` onto the new ViewController. Change the title in the Utilities Pane.
* The default `back button` will list the entire app name - feel free to change that to "back" or leave as is. You change it by clicking on the home page title, then filling in the `back button` form in the Utilities Pane.

* _Run on your iPad to make sure it's working_

* Add buttons for Camera, PhotoLibrary, and Albums (if all of those are in your wireframes!)
* Add in your ImageView, TextField for caption, and `Save` button. Apply constraints so it looks good on all devices.
* Insert a placeholder image in the ImageView.

* _Run on your iPad to make sure it's working_

#### Extension

* Fill in the blanks from your wireframe - add in colors, fonts, background images, etc. that make this the app you and your partner are dreaming of 💫

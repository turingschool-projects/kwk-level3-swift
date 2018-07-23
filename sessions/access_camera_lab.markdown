# Lab Notes: Access Camera & Photo Library

## Learning Goals

* Students will UIImagePickerController and Apple Documentation to provide their app with access to the users' camera and photo library.


## Plan

In this small app, we are going to practice building one important piece of functionality that our final project will need. This will hopefully give you confidence that you can write and implement built in code to make something AWESOME happen!


### Getting Started

* On your laptop, find the Xcode application by typing `cmd + space`, typing in `xcode`, then press return
* Click `Create a new Xcode project`
* Under `Choose a template for your new project`, select `iOS`
* Under `Application`, select `Single View App`
* Click the blue `Next` button in the bottom right corner
* You will be prompted to save this file. For `Product Name`, type in "AccessCamera", then click the blue `Create` button in the bottom right corner


### Access Camera & Photo Library

Accessing the camera and/or photoLibrary are absolutely necessary components of many apps these days - including the one we will build over the course of this week! Apple makes it easier on us by providing some code, a class called UIImagePickerController, that does a lot of the hard work for us. It's important we use it exactly as it was intended to get it to work.


#### Expected

* Decide who is going to drive/navigate and set a timer for the switch.
* Create a project with one button and one Image View. When the button is tapped, the user should see the camera open, be able to take a photo, select it, then see the photo displayed in the Image View.
* Following your notes or going back through the [slides](./access_camera_slides.markdown), get your app up and running!
* Add another button, and when that button is tapped, the user should be taken to the photo library. Refer back to the [documentation](https://developer.apple.com/documentation/uikit/uiimagepickercontroller?changes=_8) if you're not sure how 😉


#### Extension

* Add a third button, which the user can tap to select from their albums.
* Practice your UI skills by changing color, fonts, and more on there buttons. Make sure it looks great on all devices and both orientations. Maybe give your app a title? Add an icon for the buttons?


## Circle Back

As we close our tutorial time, we'll either write in our journals or discuss as a group:

- Why did we need to inherit from the UIImagePickerControllerDelegate and UINavigationControllerDelegate?
- Why did we set up each button to an `action` rather than an `outlet`?
- What did you enjoy about this lesson/lab?
- Which feature of our app are you most excited about building? Why? 

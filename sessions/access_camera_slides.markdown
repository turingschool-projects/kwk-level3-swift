footer: KWK Swift/iOS: Accessing iPad Camera
slidenumbers: true

# Accessing iPad Camera

---

# Learning Goals

* Students will be able to access a user's camera or photo library

---

# Privacy

![inline](slide_images/permissions.PNG)

^ Have you ever had an app pause, and ask a question like this? To use a user's information - whether it be from the microphone, camera, health info, etc., an app has to have the PERMISSION of a user. Apple designs the way these little boxes appear, provides us with the buttons, and handles them as necessary when tapped. But we have to go in and tell the app "Please get the users permission for XYZ" Today, we need to get the user's permission to access their camera.

---

# Info.plist

![inline](slide_images/camera-permissions.gif)

^ To tell the app that we want to ask for permission for the camera, we need to find the Info.plist file within our project on the Navigation Pane.
Click on the top row - `Information Property List`, click the small plus sign, and it will create a new row. Under Key, select `Privacy - Camera Usage ...`, then under Value, type in a short message explaining how the camera will be used.
Once you set this up in your project, it is set up forever and you should never need to some back to this page (unless you have other permissions to tell the app about!)
RECOMMENDED that you MODEL this as well as showing the giphy slide.

---

# UIImagePickerController

* Use your Google skills - find the Apple documentation for UIImagePickerController
* Read through the overview:
  - What is it?
  - What does it help us with?

^ Have students take a few minutes to read through the overview of the Apple Documentation for UIImagePickerController. The goal of this exploration is NOT that they completely understand it - the documentation can be a bit dense and there is more info than we need in here. This is just a time to give them practice sifting through it while they are safe to struggle understanding it all.
Link: https://developer.apple.com/documentation/uikit/uiimagepickercontroller?changes=_8

---

# UIImagePickerController

![inline](slide_images/apple_ui_intro.png)

^ Let's break this down:
When we see this 'view controller' - this tells us this a view controller, or the code behind a storyboard, in which Apple has already written all the code for. It's a 'freebie'!
'Manages the system interface' - interface is referring to anytime more than one program works together. We know that a program is just code, so this means that different pieces of code are coming together to make this view controller.
'... for taking pictures, etc.' tells us what use this view controller has. The name 'ImagePicker' should provide a hint, but reading the documentation carefully to make sure we are working with what we really want to work with is important.

---

# UIImagePickerController

![inline](slide_images/apple_ui_overview.png)

^ Now we get a little more info: we get these code snippets that tell us what code we will need to write to use (interface with) the code apple gives us.
This also shows how to specifically access the camera vs. the photoLibrary!

---

# Access the Camera - Setup

1. Inherit from UIImagePickerControllerDelegate and UINavigationControllerDelegate
2. Create an instance of UIImagePickerController, stored in variable
3. Tell that instance to give it's information to this class

^ We need to do a little set up. Our class needs to `inherit`, or take in the information that two apple classes have - UIImagePickerControllerDelegate and UINavigationControllerDelegate. We already know about UIImagePickerController, the Delegate added on tells the program, whenever I get information from the camera, this delegate class is the place I will send that information back to (information being the photo selected/taken). The UINavigationControllerDelegate is what allows us to navigate from our screen to the camera screen. Behind the scenes, it's a SEGUE, just written with code rather than the segue's we've seen with the arrows on the storyboard.
Code on next slide:

---

# Access the Camera - Setup

![inline](slide_images/camera-setup.png)

^ We need to do a little set up. Our class needs to `inherit`, or take in the information that two apple classes have - UIImagePickerControllerDelegate and UINavigationControllerDelegate. We already know about UIImagePickerController, the Delegate added on tells the program, whenever I get information from the camera, this delegate class is the place I will send that information back to (information being the photo selected/taken). The UINavigationControllerDelegate is what allows us to navigate from our screen to the camera screen. Behind the scenes, it's a SEGUE, just written with code rather than the segue's we've seen with the arrows on the storyboard.
Code on next slide:

---

# Access the Camera - Button Tap

1. Create a button
2. Establish an action between the button and ViewController.swift
3. Tell the app to go into the camera (via sourceType)
4. Present the imagePicker!

^ We are going to create a button, and establish an action for it. When we tap this button, our plan is that the camera will open up for our user to take a photo.
Let's give the button an appropriate title (maybe "take a photo!", and maybe name the action "takePhotoTapped" or something to that effect.)

---

# Access the Camera - Button Tap

![inline](slide_images/camera-action.png)

^ On Line 22 in the picture, we are saying, go into the instance of that UIImagePickerController, select the sourceType of camera.
On line 24, we are telling it, "stop showing whatever you are showing, and present (show) the view where the user can see use their camera!" The present function is built in, and take three arguments:
1) What do you want me to show? In this case, imagePicker.
2) Do you want a smooth animation? We will usually say yes here.
3) Once this is complete, do you want me to do anything else? We will always say 'nil'/no here.

---

# Let's try it out!

* Run on device, _not_ simulator!
* Did you see the permissions message?
* Are you able to take, select, and re-take a picture?
* What happens once you select a picture?

^ Students should get permission message (some may not, that's ok as long as camera still opens up), should get into camera and be able to take/retake/select. Once a picture is selected, user should be taken back to original screen and nothing happens.

---

# Lab

* Decide who is going to drive/navigate and set a timer for the switch.
* Following your notes or going back through the slides, get your app up and running so it can access the camera like we did in class.
* Add another button, and when that button is tapped, the user should be taken to the photo library. Refer back to the documentation if you're not sure how 😉

---

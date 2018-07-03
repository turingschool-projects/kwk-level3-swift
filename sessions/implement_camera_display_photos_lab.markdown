# Lab Notes: Implement Camera & Display Photos

## Learning Goals

* Students will implement accessing the camera/photo library and displaying photos into their personal apps

## Plan

Using your references and all that great practice with accessing the camera and displaying selected photos, we are starting to put the pieces together!!

### Getting Started

* Provide directions for any set up needed
* Some common ones - open an Xcode Playground, Project, or get on your iPad Swift Playgrounds App.

### Implement Camera & Display Photos

#### Expected

* Add a new ViewController - code version of the `Add Photo View` on our StoryBoard. Here's how: File --> New --> File --> iOS --> Cocoa Touch Class --> Click `Next` -->

* Give your View Controller an appropriate name (maybe AddPhotoViewController? NewPhotoViewController?), make sure it is a subclass of UIViewController --> Click `Next` --> Click `Create`

![inline](slide_images/save_new_vc.png)

* Now we need to connect the View in the StoryBoard to the code. While you have the `New Photo/Add Photo` View selected, go to the Identity Inspector in the Utilities Pane. In the form for class, type in (it will autocomplete) the name you gave your ViewController class.

![inline](slide_images/vc_new_setup.png)

* _Run your app in the simulator to make sure it's working! Not much should happen; that's ok. We just want to make sure it doesn't crash._

* Use the Info.plist to ask user for permission to access camera and photo library.

(For the following steps, look back at [Accessing Camera Slides](./access_camera_slides.markdown) if you're stuck!)
* Inherit from UIImagePickerControllerDelegate and UINavigationControllerDelegate

* Create an instance of UIImagePickerController, stored in variable

* Tell that instance to give it's information to this class

* Create actions for each button, and an outlet for the placeholder photo

* Inside of your actions, write the code necessary to access the camera/library/albums, based on which action you are in.

* Write the imagePickerController function. Look back at the [Displaying Photos Slides](./displaying_photos_slides.markdown) or your practice projects as a reference if needed.


#### Extension

* Continue refining you UI - colors, fonts, sizing, etc.

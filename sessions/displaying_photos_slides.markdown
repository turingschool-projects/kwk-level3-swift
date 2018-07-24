footer: KWK Swift/iOS: Displaying Photos
slidenumbers: true

# Displaying Photos

---

<!--

explain what that info dictionary is doing.

explain how this function is being called.

there are two things we want to do once this is called - tell the image to show up where we want it, then dismiss this VIEW so the imagePicker goes away!

finish code - picture should be distorted, change to aspect fit.

 -->

# Learning Goals

* Students will be able to display photos selected from UIImagePicker
* Students will be able to format pictures as they like

---

# Our Goal

![inline](slide_images/display_photo_demo.gif)

^ Feel free to have yours up and running OR just show the giphy so the students get a feel of what we are working towards.

---

#  Keep Track of that Image View

* Let's get an image onto our StoryBoard, including a placeholder image
* What do we use to keep track of, or update, data?

^ answer - outlets! They are created similar to actions, we drag and drop from the StoryBoard to the code.  

---

#  Keep Track of that Image View

* Let's call the outlet: `newImageView`
* We will use `newImageView.image` later to access and change the image

---

#  func `imagePickerController`

* Another built-in function
* Will be called once a user selects a photo
* This is where we need to tell it what to do once the user has selected a photo!

^ imagePickerController is another function that Apple has written - we want to keep track of and know when a user selects a photo from the camera, library, or albums. Once a user selects a photo, this function will be called, or will `fire`, and execute any code written inside of the code block ( the `{ }` curly braces).
DISCUSS: What do we want to tell the app to do at this point?
Possible answers/ideas to guide them towards: 
1) We want to update that original photo on our main view controller with the photo that was selected by the user. 
2) We want the user to be taken back to the screen where they can see their photo in that space from answer # 1.

---

#  func imagePickerController

![inline](slide_images/image_picker_controller.png)

^ We have some pseudo-code here as we think through how to actually make this happen.
FIRST, we have to access the photo. It is in that "info" dictionary. We access it with:
let selectedImage = info[UIImagePickerControllerOriginalImage]. In the event there is no photo, we need to unwrap this with an "if let" to make sure we have a UIImage. This looks like:
if let selectedImage = info[UIImagePickerControllerOriginalImage] as? UIImage { 
}
Now that we know we have the photo, we need to now access the outlet: newImageView. To tell the computer we want to access the image specifically, let's use `newImageView.image` and assign it to the value of the selectedImage.
if let selectedImage = info[UIImagePickerControllerOriginalImage] as? UIImage {
  newImageView.image = selectedImage
}

---

#  func imagePickerController

![inline](slide_images/new_image_update.png)

^ Now we have updated our image, BUT the user wouldn't ever know, because we haven't told the app to go away from the 'select a photo' screen.
MODEL: Go back to Xcode and model:
call the "dismiss" function on the imagePicker instance.
imagePicker.dismiss(...some stuff...) (arguments should auto-populate)
We want to tell this dismiss function that we DO want to animate, and on completion, don't do anything. It looks like this:
imagePicker.dismiss(animated: true, completion: nil)
NOW, let's run it and see if it works!
RECOMMENDATION: use photo library and run on simulator rather than camera/device, that way all students can see.

---

# Lab

* Create a brand-new app that ...
  - Has 1 button (it can either access camera, library, or albums - you choose!)
  - Has a placeholder image where you want the selected image to appear
  - Will allow user to tap button, select an image, then see that image in place of placeholder

# Lab Notes: Core Data

## Learning Goals

* Students will use Core Data to store and retrieve photos/captions

## Plan

This is the most `tutorial-based` lab you will complete at Level 3 camp. Core Data is a big framework and we don't have time to learn it at a deep level. Today, follow along the step-by-step. Please **don't** copy and paste code - 1) it won't allow you to think about what the code you're typing is _doing_, and 2) you may have different names for some important variables, and need to think carefully about that. There are some reminders throughout, but keep in mind that copy and pasting along will _not_ make this piece of functionality work in your app!

### Getting Started

* Open up your ViewFinder project
* Make sure you have completed the [Implement Camera and Display Photos Lab](https://github.com/turingschool-projects/kwk-level3-swift/blob/master/sessions/implement_camera_display_photos_lab.markdown)

### Core Data

#### Expected

Before you get start using Core Data, you're going to need to do some setup on your Table View.

* File--> New --> File --> Cocoa Touch Class --> Click `Next`, name can be whatever you think is appropriate (PostTableViewController, PhotoTableViewController, etc.), and make sure it is a subclass of UITableViewController.

* On StoryBoard, select the TableViewController, in Utilities say that it should be of ____ class (whatever you just created). This connects the view to the code!

* Delete the `override func numberOfSections` function - we don't need it!

* Uncomment out the entire `override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell { ... }` function.

* Inside that function `tableView` that you just uncommented, delete the line that starts with `let cell = ...`

* In place of it, write `let cell = UITableViewCell()`. This `cell` is referring to each row in the table. Because we stored an instance of `UITableViewCell` in the `cell` variable, `cell` now has all these attributes on it that we can take advantage of!

* On the next line, write `cell.textLabel?.text = "anything you want in here!"` Let's break this down. `cell` access the instance of the `UITableViewCell`. Calling `.textLabel` on it asked to access the label, then adding the `?` unwrapped it. Lastly, we have to call `.text` to actually take the text out of the textLabel attribute.

* _Run your simulator - do you see the text show up in every row?_

* We can also add a small image on each row, to give the user a preview of what picture they'll see when they tap on a row. Let's add this line of code below the line where you assigned your textLabel with a string: `cell.imageView?.image = UIImage(named: "name-of-image-from-assets")`

* Your code should look something like this (left), and your app should look something like this (right):

![inline](slide_images/table_code_screen.png)

Core Data:

* Create an action for your save/add button. When this button is tapped, we need to do quite a few things:
  - get the Core Data context
  - create an instance of the Core Data Object (I called my Photo; yours may be something else, so keep that in mind while you are going through this!)
  - store the caption
  - get the photo in a better format, then store it
  - update all of this in Core Data
  - use the navigationController to send out user back to the table view

* Let's start by making sure we can access the context (❗️do NOT just copy and paste this in; you have to create the action❗️)

  ```swift
  @IBAction func savePhotoTapped(_ sender: UIButton) {

    if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {

    }

  }

  ```

* We now have access to the Core Data context, so we need to dig into that specific Entity we made earlier. (In the class example it was called `Photos`. Again, if you are using your own naming which is TOTALLY ok, make sure you switch the right things out.) This line of code is saying: "I'm creating an instance of the Photos Entity from Core Data, a mini database. I'm telling it to use the Photos entity and that I want the context. I am storing all that information in a constant called photoToSave".

This code won't _do_ anything yet; but it's important in the setup!

```swift
if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {

  let photoToSave = Photos(entity: Photos.entity(), insertInto: context)

}
```

* Looking back at our long to-do list, it's time to store the caption! In this example, `captionText` is the OUTLET connected to the text field the user types into.

```swift
if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {

  let photoToSave = Photos(entity: Photos.entity(), insertInto: context)

  photoToSave.caption = captionText.text

}
```

* Now it's time to store the photo, which is unfortunately not as simple as the caption.
Look at the following:
  - newImageView is the OUTLET connected to the placeholder icon that we want to update.
  - we are unwrapping it to make sure we have the image.
  - on the next line, we are converting the `userImage` into a format that program can read. Once that's done, we store that `userImageData` as the `imageData` property on `photoToSave`

```swift
  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {

  let photoToSave = Photos(entity: Photos.entity(), insertInto: context)

  photoToSave.caption = captionText.text

  if let userImage = newImageView.image {

      if let userImageData = UIImagePNGRepresentation(userImage) {
          photoToSave.imageData = userImageData
      }

  }
}

```

* This has been a lot of work! Take a deep breathe. Only two steps left:
  - update all of this in Core Data
  - use the navigationController to send out user back to the table view

* To update everything in Core Data, we will get the context, then call the `saveContext()` function on it:

```swift
  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {

  let photoToSave = Photos(entity: Photos.entity(), insertInto: context)

  photoToSave.caption = captionText.text

  if let userImage = newImageView.image {

      if let userImageData = UIImagePNGRepresentation(userImage) {
          photoToSave.imageData = userImageData
      }    
  }
  (UIApplication.shared.delegate as? AppDelegate)?.saveContext()

}
```

* Lastly, we need to tell the navigationController that we want to send the user back to the other View Controller.

```swift
  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {

  let photoToSave = Photos(entity: Photos.entity(), insertInto: context)

  photoToSave.caption = captionText.text

  if let userImage = newImageView.image {

      if let userImageData = UIImagePNGRepresentation(userImage) {
          photoToSave.imageData = userImageData
      }    
  }
  (UIApplication.shared.delegate as? AppDelegate)?.saveContext()

  navigationController?.popViewController(animated: true)

}
```


* Check the simulator - what's happening? What's still missing, and why?

* At the top of your TableViewController class (it probably has a slightly different name), let's create an empty array, which will soon hold all our Core Data data. Call it whatever you would like/makes sense to you based on your Core Data Entity name. This example used `Photos` as the Core Data Entity name.

```swift
var photos : [Photos] = []
```

* We are saving the photos/captions, but we aren't asking Core Data for them and we aren't telling the Table View Controller to display them. In your TableViewController file (it probably has a slightly different name), right below the `viewDidLoad()` function, write a new function:

```swift
function getPhotos() {

}
```

* Again, we need to get into the Core Data context:

```swift
function getPhotos() {

  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {
    // now we need to search through Core Data to find our photos/captions
  }

}
```

* Now that we have access to the context, we will use a function called `fetch()` to retrieve data from Core Data. As you write your own code, _remember_, this example used `Photos` as the name of the entity in Core Data, and `photos` is the variable that holds an array that was created at the top of the class.

```swift
function getPhotos() {

  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {

    if let coreDataPhotos = try? context.fetch(Photos.fetchRequest()) as? [Photos] {

      if let unwrappedPhotos = coreDataPhotos {
        photos = unwrappedPhotos
        tableView.reloadData()
      }

    }
  }

}
```

* This `getPhotos()` function is all ready to go and will really help us out. BUT, we aren't calling it anywhere. Let's write a new functions, `viewWillAppear` (it should auto-populate as you start typing it), and inside of it, call the `getPhotos()` function.

```swift
override func viewWillAppear(_ animated: Bool) {
  getPhotos()
}
```

* We are getting so close! We just need to work on two functions. Take a little brain break if you need one!

* We need to update one of the `tableView()` functions (the one with numberOfRowsInSection in the argument). Let's change the return value to photos.count

```swift
override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
     return photos.count
}
```

* Run your simulator - what is different? What are we still missing? We should be seeing the right number of rows, but still seeing that placeholder image on the table. That's because we still have that icon hard-coded in on this line: `cell.imageView?.image = UIImage(named: "camera-icon")`. Let's change that!

* We first need to access the current photo we are looking at.

```swift
let cellPhoto = photos[indexPath.row]

cell.textLabel?.text = cellPhoto.caption

```

* The function should end up like this:

```swift
override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
    let cell = UITableViewCell()

    let cellPhoto = photos[indexPath.row]

    cell.textLabel?.text = cellPhoto.caption

    if let cellPhotoImageData = cellPhoto.imageData {
        if let cellPhotoImage = UIImage(data: cellPhotoImageData) {
            cell.imageView?.image = cellPhotoImage
        }
    }

    return cell
}
```

* You should now see your photos showing up on the list, and the list should only be as long as the number of photos you have!

### ❗️Commit Your Work ❗️

In Xcode, select `Source Control`, `Commit`, type in a message describing your changes (probably "Add Core Data"), then click Commit Files.

#### Expected

* ADD IN INSTRUCTIONS FOR DELETE FUNCTIONALITY ON TABLE VIEW


### ❗️Commit Your Work ❗️

In Xcode, select `Source Control`, `Commit`, type in a message describing your changes (probably "Add delete functionality"), then click Commit Files.

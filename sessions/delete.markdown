# Lab Notes: Build Photo Detail View

## Learning Goals

* Students will ...
* Students will ...

## Plan

This is the final step in functionality for our app!


### Getting Started

* Open up your ViewFinder project
* Make sure you have completed the [Core Data Lab](https://github.com/turingschool-projects/kwk-level3-swift/blob/master/sessions/core_data_lab.markdown) before starting


### Build Photo Detail View

#### Expected

* Drag a new View Controller onto your StoryBoard. Drag an Image View onto it and size however you would like. Drag a Navigation Item from the Object Library onto it as well.

* Create a segue between the Table View Controller and the new View Controller. Make sure you have the entire controller selected when you click and drag.
![inline](slide_images/new_segue.png)

* Create a View Controller file so we can write code that controls the new View. File --> New --> File --> Cocoa Touch Class --> Class Name: (something like PhotoDetailViewController, up to you), Subclass of: (_must_ be UIViewController) --> Click `Next` --> Click `Create`

* To connect this View Controller to the View on the StoryBoard, select the View on the Storyboard. In the Utilities Pane, select the `Identity Inspector`, and under Custom Class, list the class as the name of the file you just created.

* Create an outlet for the image on the StoryBoard to our new code file.

* Right below the outlet, create a variable, for this example we will use `photo`, with the optional type (again in this example), `Photos`. `Photos` was used here because it is the entity name in Core Data.

```swift
let photo : Photos?
```

* In _Table_ View Controller, write a `tableView` function - when you start typing, it will being to autocomplete. Select the function that includes `didSelectRowAt`. Inside that function, call the `performSegue` function - it will auto-complete. The `sender:` value should be `photos[indexPath.row]` - photos was the variable that started off as the empty array. For the `withIdentifier` value, we need to hop over to the StoryBoard to get some information.
  - In the StoryBoard, click on the segue you established between the Table View Controller and the Photo Detail View. In the Utilities Pane, click on the Attributes Inspector. Under StoryBoard Segue, we need to type in an Identifier. It should be descriptive - maybe `moveToDetail`, or `detailSegue`.
  - Whatever you just named the segue Identifier in the step above, that should go, in a string, as the value of the `withIdentifier` argument in the `performSegue` function back in the Table View Controller.

* Now that we've told the program to perform the segue, we need to tell it how to prepare. Below the `performSegue` function, start typing out `prepare` and an `override func prepare(for segue ...)` should auto-populate.

* Inside the `prepare` function, we first need to check if we are dealing with the correct segue - in this example's case, `moveToDetail`. Your code should look something like this:

```swift
override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
    if segue.identifier == "moveToDetail" {
        // need to get access to View Controller we want to move to
    }
}
```

* Now that we know the request was made to use the correct segue, let's use an `if let` to get into the segue `destination` - the `PhotoDetailViewController`.

```swift
override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
    if segue.identifier == "moveToDetail" {
        if let photoDetailView = segue.destination as? PhotoDetailViewController {

        }
    }
}
```

* Our next line of code will make sure that we have the type of Core Data object we are expecting. In this case we only have `Photos`.

```swift
override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
    if segue.identifier == "moveToDetail" {
        if let photoDetailView = segue.destination as? PhotoDetailViewController {
          // now we need to say, whichever row was tapped, take that photo
          // and send it to the over view
        }
    }
}
```

* Let's take the photo that was tapped on and send it to the PhotoDetailViewController.

```swift
override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
    if segue.identifier == "moveToDetail" {
        if let photoDetailView = segue.destination as? PhotoDetailViewController {

          if let photoToSend = sender as? Photos {
                   photoDetailView.photo = photoToSend
          }

        }
    }
}
```

* Run your application - what is happening when you tap on a row in the Table View? What is still missing?

* In the PhotoDetailViewController (or whatever you titled yours!), we need to write some code in the `viewDidLoad` function. This will tell the View, "as soon as you load, please do XYZ." The XYZ in this case will be, display the photo I told you about!

* First, we need to make sure we have a photo.

```swift
override func viewDidLoad() {
    super.viewDidLoad()

    if let realPhoto = photo {

    }
}
```

* Now, we need can make the title on the nav bar match the title you gave the photo:

```swift4
override func viewDidLoad() {
    super.viewDidLoad()

    if let realPhoto = photo {
        title = realPhoto.caption
    }
}
```

* Lastly, we are going to use a bit of code we wrote in the Table View Controller to get the imageData, convert it to the right format, then make that Image View show the photo that was tapped on!

```swift
override func viewDidLoad() {
    super.viewDidLoad()

    if let realPhoto = photo {
        title = realPhoto.caption

        if let cellPhotoImageData = realPhoto.imageData {
            if let cellPhotoImage = UIImage(data: cellPhotoImageData) {
                photoDetail.image = cellPhotoImage
            }
        }

    }
}
```

#### Extension

* This is an early finisher/extension activity!

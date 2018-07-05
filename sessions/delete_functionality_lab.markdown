# Lab Notes: Delete Functionality

## Learning Goals

* Students will build delete functionality on a single row in the table view

## Plan

Give the instructor a 1-2 sentence overarching explanation of this lesson


### Getting Started

* Open up your ViewFinder project
* Make sure you have completed the [Build Photo Detail View Lab](https://github.com/turingschool-projects/kwk-level3-swift/blob/master/sessions/build_photo_detail_view.markdown) before starting

### Delete Functionality

We've seen some of the great built-in Apple tools that we can use as we develop iOS apps - something we will implement today is the `swipe left to open an option to delete`. This will allow our users to delete a photo/cation from the Table View, similar to this:

![inline](slide_images/delete_swipe.png)

#### Expected

* In your Table View Controller, un-comment out the `tableView` function that has `canEditRowAt` in the argument **and** the `tableView` function that includes `commit editingStyle` in the argument.

* Inside that second `tableView` function, delete the `else if` statement. Delete the code inside of the `if` block.

* Run your simulator - you should be able to swipe on a row and see a delete button appear on the right side. However, this button shouldn't work yet!

* Look at that `if` block in your code. It is saying, "If the editing style is 'delete', then do something." Since that 'something' is empty, nothing is happening when we tap that `delete` button.

* Inside of the `if` block, let's write a print statement. Running the app again, try to delete. Do you see the print statement show up in your Debug Area?

* NOW, let's write some code to actually get this row to delete! Since we want to delete this from Core Data, we need to get the context again.  

```swift
if editingStyle == .delete {
  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {
    // now that we have access to Core Data, we need to select the row, then delete the photo
    // we also need to save the context and reload
  }
}
```

* Next, let's select the row that was swiped - this will look familiar (keep in mind, this example used `photos` as that empty array that we created at the top of the class. You might be using a different variable):

```swift
if editingStyle == .delete {
  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {
    let photoToDelete = photos[indexPath.row]
    // now delete, then save, then reload
  }
}
```

* Now, we actually need to delete this photo! We will use a `delete` function, that takes one argument - the thing we want to delete!

```swift
if editingStyle == .delete {
  if let context = (UIApplication.shared.delegate as? AppDelegate)?.persistentContainer.viewContext {
    let photoToDelete = photos[indexPath.row]
    context.delete(photoToDelete)

    //save to context, then reload
  }
}
```

* Last step - we've also seen these before. Let's add the following lines in below the line where we deleted the photo from the context.

```swift
    (UIApplication.shared.delegate as? AppDelegate)?.saveContext()
    getPhotos()
```
* Run your app - is the delete functionality working? It should be. If not, re-read through this, double-checking everything, then ask another team or an instructor for a second pair of eyes.


#### Extension

* Do some research - can you find any documentation or blogs on how to show the trash can icon instead of the word 'Delete' on that red space that appears when you swipe? `UITableViewCellEditingStyle` might be helpful to include in your google search. If you find a good resource and want to change to an icon for your project, go for it!

# Lab Notes: Choose Your Own ... Feature!

## Learning Goals

* Students will refine app or add functionality to their app.


## Plan

This lab time can be used to clean up any code, refine your UI, _OR_ add a feature to your app! You get to choose how you spend your time, and you get to do the research on _how_ to make it happen.


### Getting Started

* Open up your ViewFinder project
* Make sure you have completed the [Delete Functionality Lab](https://github.com/turingschool-projects/kwk-level3-swift/blob/master/sessions/delete_functionality_lab.markdown) before starting
* Make **100% sure** that you have `committed` you project. This way, if your new feature breaks your project, you can just get rid of today's changes without losing your whole project.


### Choose Your Own ... Feature!

#### Expected

* Spend a few minutes deciding with your partner on what you would like to dedicate this time to. A few ideas:
  - Work on your UI - colors, backgrounds, fonts, sizing, etc. Is there anything from your wireframe that you still haven't had time to implement and you want to add it in? Now is the time! Do you want to modify your Table View so the image is a bit bigger?
  - Do you want to have a `Welcome` view that your user always starts at? It could have the authors names, info about the app ... anything you want!
  - Add a feature! You could add another textField and ask the user to type in an emoji, then place that emoji over their photo. Many other possibilities... Just keep in mind that your instructors couldn't have predicted what you want to add, so they may not know exactly how to do it - be ready to Google 💪

**Tips:**

Modify Table View:
- step 1
- step 2
- step 3

Emoji Over Photo Detail:
- In your <ProjectName>.xcdatamodeld file, add another attribute to your entity that currently has the photo and caption.
- In your AddPhotoViewController, you will need to create another textField. In the function that is fired when you click `Submit`, you will also need to store the emoji in Core Data, similar to the way you saved the caption text.
- In you Photo Detail View, add a Label to the StoryBoard. In the `viewDidLoad` function, you'll need to update that label with the emoji that is stored in Core Data.

## Circle Back

As we close our work time, we'll either write in our journals or discuss as a group:

- What about this project are you most proud of?
- What was the biggest challenge?
- What do you want to build next?
- What surprised you as you were becoming an iOS developer?

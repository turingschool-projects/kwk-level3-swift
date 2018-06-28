footer: KWK Swift/iOS: StoryBoards
slidenumbers: true

# StoryBoards

^ [Here is a repo with an example of a UI you can create](https://github.com/turingschool-projects/storyboard-sample/tree/master) - I tried re-create a simplified version of Spotify's Podcast play screen. This is definitely something you want to do several times in your prep - practicing where you will stop, show them things they might get tripped up on, etc.

---

# Learning Goals

* Students will be able to add UI elements to the StoryBoard using the Object Library
* Students will be able to make UI look clean on all device sizes using constraints
* Students will be able to add a home screen icon into the project

---

# Technical Vocabulary

* StoryBoard
* UI
* Constraints

---

# Xcode Projects

* A place for building entire iOS projects
* A lot more than writing code goes into building an iOS app, but we do it all in Xcode!
* A LOT of tools - we will take it one step at a time

---

# Navigating Xcode Projects

![inline](slide_images/xcode-project-nav.png)

^ MODEL: Open up a new project, walk through every step of setup. Show each pane and the buttons to expand/collapse panes. Show file tree and point out storyboard. Model resizing and moving the storyboard. Show simulator, build status bar, and different device views.

---

# StoryBoard & Object Library

* Before we write all the Swift code we've been learning to make our app DO something, we want to completely set up the UI (user interface)
* We will drag and drop components of the UI from the _Object Library_

^ MODEL: Go back to Xcode, model dragging and dropping in (in this order):
- View - Recommended to change color so it's clear what you did.
- Label - Show both ways that text can be changed
- Image
- Recommended to scroll through and show them buttons. sliders, date picker, etc. - just to get them excited about what is available!

---

# Constraints

* Everything looks great on my screen, but in the simulator... not so much.
* We will not use constraints - settings on UI Objects that make them appear the way we expect on ever device

^ MODEL: Go back to Xcode, select one UI Object at a time, then apply the following constraints:
- View - 0 on all sides
- Label - set a width, distance from top of screen, horizontally center
- Image - set a width and height, distance from label, horizontally center

---

# Home Screen Icon

* On the simulator, click the 'Home' button, and notice our app icon is pretty boring.
* To add an icon for iPad, it must be exactly 152x152
* Drag and drop the image from your finder, into the '2x' box right above 'iPad App, iOS 7 - 11 76pt'

^ MODEL: Go to google, image search for a 152x152 image (select tools, then exact size to set this preference) Select and save an image to desktop. In Xcode, click on `Assets.xcassets`, then `AppIcon`. With both Xcode and Finder windows visible, drag image file from Finder into the 2x box above 'iPad App, iOS 7 - 11 76pt'. To make sure it works on all iPads, we should really do the right thing and also drop a 76x76 image in the 1x box.

---

# Aviatrix I0: Up & Running

## Getting the Code

For this project you're going to work within some code we've already built. Follow the following steps to get it up and running on your computer:

1. Visit `https://github.com/turingschool-projects/aviatrix_swift`
2. Click the green `Clone or Download` button
3. Click `Download ZIP`
4. Open in Finder, rename if you'd like
5. Drag to Desktop (so you can easily find it!)
6. Open the folder, double-click the file that ends in `.xcodeproj`
7. A box will appear that says something like: “AviatrixApp” is a project downloaded from the Internet. Are you sure you want to open it? Click `Open`.

## Exploring the Code Base

You'll find that there are a couple code files that you'll work with:

### `Aviatrix.swift`

This is the main file where we'll be doing work. There are several functions in here, but the code/instructions to make it work has been removed.

### `AviatrixData.swift`

Our program is going to need a bunch of data like city names, distances between cities, and fuel prices. This file holds all that data. We won't need to change anything in this file for the main project. (As an extension, you'll have the chance to add cities/distances.)

### `main.swift`

This is the file that we'll use to try out our code and talk to our console in the debugger area. This has a lot of code in it. You shouldn't *need* to change much in this file - later we will uncomment some code that would currently throw errors.

## A First Run

Click the play button in the top left hand corner, or `cmd + r` to run your code. It will run in your console so make sure that drawer is showing. Make sure your console area is open so you can see what the program does (you may see some build-time warnings show up - don't worry about those for now.)

Once the program is running you'll see that it doesn't really do much. This is because we've got all those empty functions. We'll slowly bring it to life.

## Adding our First Functionality

Let's start by making some small changes.

### `start`

You'll see that there's a function named `start` which currently always returns `true`. We'll later use this to make sure that the plane is running before we fly anywhere.

Add the `running` instance variable so it defaults to false, then changes to true when the `start` function is called. Return that boolean out of the function.

```
var running = false

fun start() -> Bool {
  running = true
  return running
}
```

That way our method will return the value of the `running` variable.

### `author`

To make sure other know who build this program, we want to be able to display your name! In your `Aviatrix` class, create an author instance variable (data type: String, value: none, yet), and write an `init` function to pass an argument in when you create an Aviatrix object.

In `main.swift` there is a line that prints to the console: print("Welcome to the Aviatrix Flight System by _ _ _ _ _ _ _ _ _ " ) - change that so your author variable is interpolated.

### Run It

Run the program and observe the `author` output in the first line of the program.

Let's keep going! [Move on to Iteration 1](./i1_destinations.markdown)

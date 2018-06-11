# Aviatrix I0: Up & Running

## Getting the Code

For this project you're going to work within some code we've already built. Follow the following steps to get it up and running on your computer:

1. <TODO: steps>
2. <TODO: steps>
3. <TODO: Steps>

## Exploring the Code Base

You'll find that there are a couple code files that you'll work with:

### `Aviatrix.swift`

This is the main file where we'll be doing work. There are several functions in here, but the instructions to make it work have been removed. You can see we have several empty functions to start off with.

### `AviatrixData.swift`

Our program is going to need a bunch of data like city names, distances between cities, and fuel prices. This file holds all that data. We won't need to change anything in this file.

### `main.swift`

This is the simulator that we'll use to try out our code. This has a lot of code in it. You shouldn't *need* to change much in this file - just uncommenting some code that would currently throw errors.

## A First Run

Click the play button in the top ledt hand corner, or `cmd + r` to run your code. It will run in your console so make sure that drawer is showing.

Once the program is running you'll see that it doesn't really do much. This is because we've got all those empty functions. We'll slowly bring it to life.

## Adding our First Functionality

Let's start with making some small changes.

### `start`

You'll see that there's a function named `start` which currently always returns `true`. We'll later use this to make sure that the plane is running before we fly anywhere.

Replace the stub in this function, and add the `running` instance variable so it looks like this:

```
var running = false

fun start() {
  running = true
}
```

That way our method will return the value of the `running` variable.

### `author`

To make sure other know who build this program, we want to be able to display your name! In your `Aviatrix` class, Create an author instance variable, and use the `init` function to pass an argument in when you create an Aviatrix object. In `main.swift` there is a line that prints to the console: print("Welcome to the Aviatrix Flight System by _ _ _ _ _ _ _ _ _ " ) - change that so your author variable is interpolated.

### Run It

Run the program and observe the Author output in the first line of the program.

Now it's time to start the real work. [Move on to Iteration 1](./i1_destinations.markdown)

# Aviatrix I0: Up & Running

## Getting the Code

For this project you're going to work within some code we've already built. Follow the following steps to get it up and running on your computer:

1. <TODO: steps>
2. <TODO: steps>
3. <TODO: Steps>

## Exploring the Code Base

You'll find that there are a couple code files that you'll work with:

### `aviatrix.rb` <TODO: fix filename>

This is the main file where we'll be doing work. There are several methods in here, but the instructions to make it work have been removed. We've put comments that say `#stub` in places where there's fake data or instructions. Eventually you'll be replacing every `#stub` with your own code.

### `aviatrix_data.rb` <TODO: fix filename>

Our program is going to need a bunch of data like city names, distances between cities, and fuel prices. This file holds all that data.

### `simulator.rb` <TODO: fix filename>

This is the simulator that we'll use to try out our code. This has a lot of code in it. You shouldn't *need* to change anything in this file, but you'll be invited to make changes later in the project.

## A First Run

<TODO: instructions about how to run the starter code in Xcode>

Once the program is running you'll see that it doesn't really do much. This is because we've got all those `#stub` instructions in place of the code we really want to write. We'll slowly bring it to life.

## Adding our First Functionality

Let's start with making some small changes.

### `running?`

You'll see that there's a method named `running?` which currently always returns `true`. We'll later use this to make sure that the plane is running before we fly anywhere.

Replace the stub in this method so it looks like this:

```
def running?
  @running
end
```

That way our method will return the value of the `@running` variable.

### `author`

There's an `author` method that returns the name of the program's author. Put your name in there.

### Run It

Run the simulator and observe the Author output in the first line of the program.

Now it's time to start the real work. [Move on to Iteration 1](./i1_destinations.markdown)

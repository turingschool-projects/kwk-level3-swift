footer: KWK Swift/iOS: Functions
slidenumbers: true

# Functions

---

# Learning Goals

* Students will be able to use function syntax to package a set of commands, including arguments and return values
* Students will be able to follow the flow of arguments throughout a function

---

# Technical Vocabulary

* Function
* Argument
* Return Value
* Call (a function)

---

# What is a function?

* An action in our code
* A function has a specific job, and it sits around waiting to be asked to to it's job
* It can have a very small (add two numbers) or very big job (find the standard deviation of 1 million numbers)
* We get to write them so we have control over what their jobs are

^ You've seen these before - in JavaScript they are also called functions; in Ruby they are called methods. This is the meat of a program - without functions we can't do much.
In just a minute, we will go through the syntax of functions in Swift, and make sure you have everything you need to start writing them!
Let's pretend we have a robot who is going to help us run a dog walking service.

---

# Functions

func walkDog() {  
  // put on leash
  // open door
  // leave house
  // walk
  // walk back to house
  // etc.
}

^ Some people describe functions as 'packages of commands' - we usually group a few commands into one function. The function name should describe what it's job is.
Today, we are going to write a walkDog function, which will give a set of commands to the robot to walk a dog.
Discussion: What are the steps in walking a dog? (Solicit input from students whole group - put on leash, maybe harness, make sure you have poop bags, open door, walk outside, walk forward, turn around, walk back, throw bag in trash, open door, take off leash, give treat, etc. - make sure you have at least four)
Take notes on whiteboard of the list students create. Explain that those are all the small commands that will make up our walkDog function.

---

# Syntax - Declaring

func walkDog() {
  // code
  // goes
  // here
}

^ Switch over to a Swift playground and live code this (since you want to use the student generated list of commands)
Start with function declaration: func walkDog() { }
Write in print() statement with all the commands listed on whiteboard (make sure they are wrapped in quotes!)

---

# Syntax - Calling

* This code doesn't currently do much - why not?
* Functions don't do their job until they are told to
* Telling a function to do it's job is called 'calling a function'
* `walkDog()`

^ MODEL:
No need to use this slide unless you want to - you can just continue with live code.
We want to re-iterate the fact that functions alone are just that - sitting there alone, doing nothing. They wait on US to CALL them.
Make sure you go back into the Playground to call the function (with walkDog(), below the declaration) - students should see all the print statements in the console.

---

# Arguments (Inputs)

If we are really going to have this robot help out, we need it to be a little 'smarter'. We need it to know that if there are two dogs, it needs to put two leashes on, bring two poops bags, etc.

We can make functions a little 'smarter' with something called 'arguments'

---

# Arguments - Syntax

func walkDog(numberOfDogs : Int) {
  print("There are \(numberOfDogs) dogs in the house")
}


func walkDog(numberOfDogs : 4)

^ Show this slide, explain that the 4 that is passed into the function call is substituted into the function, so anytime the function sees the variable `numberOfDogs` - it will substitute 4 in for that variable.
Be careful - the spaces surrounding the ":" in the function declaration's () DO matter - (numberOfDogs : Int) works and (numberOfDogs:Int) work buts (numberOfDogs :Int) or (numberOfDogs: Int) do NOT work.
<Move to Xcode to model>
MODEL: it's recommended to copy and paste then comment out the first function. That way you have something to start with but don't have naming conflicts.
Add an argument into the function declarations ()
If you already have a function call below, it should be throwing an error. Delete it, re-type, and as you type the function name it will pre-populate the argument name and data type.
Pass an argument in, replacing "Int"
Use string interpolation, seen on the previous slide, to make one of the commands dynamic based on the argument passed in.

---

# Return Values

We won't always just use functions to print things to the console - we'll have many functions that have different jobs, all working together to create one big program.

Part of the way they do this is by 'returning' a value. Return values can be any data type - strings, integers, arrays, and more.

---

# Return Values - Syntax

func walkDogs(numberOfDogs : Int) -> Int {

  return 3
}

walkDogs(numberOfDogs : 3)

^ Point out the "-> Int" and "return 3" pieces. Explain that the "->" tells the computer to expect a return value out of this function, and "Int" means that the return value must be an integer.
Because it's expecting an integer to be returned, we use the "Return" keyword on the last line of the function. We can return an integer like 3; OR, and more commonly, return a variable with an integer value. That way, depending on what happens in our function, we may return something unique.
<Move to Xcode to model>
MODEL: again copy/paste and comment out previous code. Model for the students - adding in the "-> Int", and the return keyword.
Possible calculation to make/return:
var lengthOfWalk = numberOfDogs * 15 (make the walk 15 minutes long for each dog)
return lengthOfWalk (return the number of minutes out of this function)

---

# How to use Return Values

This is all great - but where did that return value GO? Who sees it? What can we do with it?

^ MODEL
Feel free to put this code on a slide or just continue modeling in the playground.
let minutesToWalk = walkDogs(numberOfDogs : 3)
print("Please walk the dogs. I will expect to see you complete that task in \(minutesToWalk) minutes!")
The "let" was used because minutes to walk is not changed. If you are curious, try starting with var then noticing the warning Xcode throws.

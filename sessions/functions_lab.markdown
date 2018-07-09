# Lab Notes: Functions

## Learning Goals

* Students will be able to use function syntax to package a set of commands, including arguments and return values
* Students will be able to follow the flow of arguments throughout a function
* Students will be able to predict the return value of a function based on syntax and calculations

## Plan

You will go through a set of activities building a function, then a function that takes arguments, then one that returns a value.

### Getting Started

* On your laptop, start the Xcode application by pressing `cmd + space` to bring up the spotlight window, typing in `xcode`, and then pressing return
* Click `Get started with a playground`
* Select 'blank', then click the blue `Next` in the bottom right corner
* You will be prompted to save this file. The default name is `MyPlayground` - let's change that to "Functions", then click the blue `Create` button in the bottom right corner

### Functions

Functions are chunks of code that have a specific job in helping our program. Remember, functions don't do their job unless they are **told to**.

#### Expected

* With your partner, brainstorm another task you'd like to have this robot complete. You should agree on using the same task that way you can check in with each other throughout the lab. Once you've decided on it, share with an instructor to make sure it will work for all activities, then go to the next step
* In your notebook, write out the small steps that your robot needs to take in order to complete the task
* In your playground declare and call the function - the code block should be empty
* To make 100% sure you are calling it correctly, write a print statement into the code block and make sure that appears in your console
* Now, write a print statement for each of the commands you wrote down in your notebook. Are they all printing out as expected?

### Functions - Arguments

Arguments are a very important part of functions - they allow functions to be dynamic - or change based on the situation. My robot would have a very different experience walking 1 dog versus walking 18 dogs, and that should be reflected by it's actions. That means, I need to tell my robot to take different actions. Arguments are the tool for that.

#### Expected

* Building off of your function already written - what information could you give this function to show different situations?
* Comment out your first function, and start over. This time, your function declaration should ask for an argument. It doesn't necessarily have to be an integer like the class example!
* Finish writing your function
* Call your function - a few times, passing in different arguments each time

### Functions - Return Values

Without return values, our functions can't really send their results anywhere. Swift is very picky - it wants to know if you plan on returning a value from the get-go, and will be looking for a return statement on the last line of the function.

#### Expected

* With your partner, decide what information you want to return out of your function. What data type is most appropriate (string, integer, etc.)?
* In the declaration, tell your function you plan to return a value
* Use the return keyword to return the desired value
* Check yourself: did you return a number like "4" or a string like "Good job!"? To make this function dynamic, we should probably be returning a _variable_ that is storing something your calculated based on the argument passed in. Look back at the class example if you are stuck on this part!
* Call your function - a few times, passing in different arguments each time. STOP!
* Before you run your code, talk with your partner - what is the expected output/return value?

#### Extension

* What is another argument that could be passed in your function? Try it out! Not sure what the syntax looks like? You got this. Remember, strong developers are strong googlers, so feel free to look for examples online.
* Can you have more than 1 return value? How do you know?

## Circle Back

As we close our tutorial time, we'll either write in our journals or discuss as a group:

- When does a function do it's job? What does the syntax look like to tell a function to do it's job?
- For the following function, what would print to the console? Why? Feel free to explain in words or with a diagram.
```
func drinkWater(amount : Int) {
  print(amount)
}

drinkWater(amount : 10)
```

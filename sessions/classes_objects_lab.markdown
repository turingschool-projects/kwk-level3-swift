# Lab Notes: Classes and Objects

## Learning Goals

* Students will use correct syntax to create classes, variables, and init functions
* Students will be able to access property information from an object
* Students will be able to explain how objects created from the same class can have different values stored in the properties

## Plan

You will have some time to create your own class and some objects from it! You will have plenty of partner time to brainstorm and really plan out your code before you start coding.

### Getting Started

* On your laptop, start the Xcode application by pressing `cmd + space` to bring up the spotlight window, typing in `xcode`, and then pressing return
* Click `Create a new Xcode project`
* Under `Choose a template for your new project`, select `macOS`
* Under `Application`, select `Command Line Tool`
* Click the blue `Next` button in the bottom right corner
* You will be prompted to save this file. For `Product Name`, type in "ClassesAndObjects", then click the blue `Create` button in the bottom right corner

### Classes

In programming, we think of `classes` as blueprints or cookie cutters. They give us the framework for an object, when a lot of objects may have something (or many things!) in common.

#### Expected

* With your partner, brainstorm another class. Remember, we used Student because all students share some things, and also had some unique things about them. If you are struggling for an idea, Car and Dog are both commonly used to practice work with classes 🚗 🐶
* With your partner, write a list of properties your class should have. What is true about every ____? (If you are talking about a car, every car has wheels...)
* What function, or action, do you want your _____ to take? (If it's a dog, I would want it to bark, sit, fetch...) Come up with at least 2 actions!
* Create a new (macOS, Swift) file inside of the ClassesAndObjects folder, name it the same thing you will name your class
* Write your class
* Create variables for the properties your class needs
* Write the actions for your class
* In main.swift, create at least one object with this class and do some printing to make sure your class is behaving as expected
* Add in an `init` function so you can pass your class something specific to the object you are creating. (For a car, I would definitely want to make sure the color could change!)

#### Extension

* Read this [blog post](https://www.weheartswift.com/swift-classes-part-2/)
* What is a scenario where you could use a superclass and subclass?
* If you still have time, try to build the superclass and subclass you brainstormed. You can just create a new file in the project you've been working in.

## Circle Back

As we close our tutorial time, we'll either write in our journals or discuss as a group:

- Why do you think the instructors had you spend so much time brainstorming and writing in your notebooks before coding? What about that process was helpful?
- What is the difference between a class and an object?
- What is a NEW example of something that would make a good class? Explain why this would make a good class.
- What are properties? How do we _access_ the properties of an object (in other words, how do I check what the values of an objects' properties are)?
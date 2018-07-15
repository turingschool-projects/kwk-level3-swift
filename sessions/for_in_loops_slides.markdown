footer: KWK Swift/iOS: For-In Loops
slidenumbers: true

# For-In Loops

---

# Learning Goals

* Students will understand what a for-in loop is and why they are useful
* Students will learn how to create a for-in loop to accomplish repetitive code
* Students will learn how to use for-in loops to iterate over arrays

---

# Technical Vocabulary

* For-In Loop
* Array
* Index
* Element
* String
* Iterate

---

# What is a for-in loop?

* A `for-in` loop is a block that will run code a specific number of times
* A `for-in` loop can iterate through an array and do something with each element

^ Loops are VERY common and necessary parts of a programming language - every language has their version of getting this some.

---

# When would we use them?

`For-in` loops are useful whenever you want to repeat a bit of code a specified number of times. We can also use them to iterate over arrays and dictionaries.

---

# Creating a For-In Loop

Let's learn how to create `for-in` loops. We will specify what we are working with, how many times the loop will run, and what the code will do each time.

---

# Creating a For-In Loop

A for-in loop has a few parts:

* The keyword `for` which begins the loop
* A name for the data we're working with - in the loop below, we use an underscore because we're not really using any data
* The keyword `in`
* The number of times the loop will run
  - The first number is the low point
  - The second number is the high point

---

# Creating a For-In Loop

```swift
for _ in 1...4 {
  print("Hello!")
}
```

^ Why didn't we use a variable here? We didn't _need_ one. We weren't iterating over an array and trying to do something with each element.

---

# Turn and Talk

* Turn to a new best friend and explain the following:
  - What is a `for-in` loop? Why are they useful?
  - How many times do you think that loop will print "Hello" to the console?

---

# For-In Loops and Arrays

We can use `for-in` loops to use data from an array. If we created an array of cute animals, say something like this:

```swift
var animals = ["red pandas", "giraffes", "sea turtles"]
```

We could write a for-in loop to do the same thing with each of the strings in our array.

---

# For-In Loops and Arrays

Unlike the first for-in loop we saw, which used an underscore and two numbers to indicate how many times the loop will run, we can write a `for-in` loop that will work with this array no matter how many elements it has.

```swift
for animal in animals {
  print("I love \(animal)!")"
}
```

^ What do you think will happen? What if we add another animal to our array? Why do you think we used the words "animal" and "animals" in our for-in loop?
---

# For-In Loops and Arrays

Let's try to understand what's going on here.

```
for animal in animals {
  print("I love " + animal)
}

=> I love red pandas
=> I love giraffes
=> I love sea turtles
```

^ The first `animal` right after the keyword `for` refers to each element of our array, and the `animals` after the `in` keyword is the name of our array.
We've told our loop to run the same number of times as there are elements in the array. If we added another animal to our array, the loop would run four times.
By using the word `animal` after the `for` keyword, we're telling our code that we can use `animal` like a variable, and its value for each iteration of the loop will be whatever element of the array it's currently on.

---

# For-In Loops and Arrays

What if we wanted to use the for-in loop to edit the contents of an array? Let's say, for example, that instead of printing `"I love " + animal` to the console, we wanted to update each element to be that string!

We'd have to do something like this.

```
for index in 0..<animals.count {
  animals[index] = "I love " + animals[index]
}
```

---

# For-In loops and Arrays

What's going on in this code?

```
for index in 0..<animals.count {
  animals[index] = "I love " + animals[index]
}
```

^ Think about the lesson on arrays - how did we access information? What do you think `index` stands for in our code? Can you figure out what is happening after the `in` keyword?
Take a few minutes to journal your thoughts and guesses! Then turn and talk with your neighbor - do you have different ideas?

---

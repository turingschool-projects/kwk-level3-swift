footer: KWK Swift/iOS: Conditionals
slidenumbers: true

# Conditionals

---

# Learning Goals

* Students will use if/else if statements to control flow of an application
* Students will use comparison operators

---

# Technical Vocabulary

* Condition
* Comparison Operator
* Evaluate

---

# Flow Control - IRL

* In life, we make decisions based on our current situation:
  * If I'm hungry, I'll eat
  * If I'm tired, I'll take a nap

^ Turn and Talk - what are some other examples where we make decisions in real life? How about in apps or programs? (GET THEM THINKING ABOUT IT BEFORE WE GIVE EXAMPLES)

---

# Flow Control

* We do the same thing in programming:
  * If a user is signed in, they see their account
  * If no one is signed in, the user is prompted to do so

^ The idea of an application doing different things, going in different directions based on what the user wants is called FLOW CONTROL. It's a very important concept because it is constantly being used - no matter what language you work in!

---

# Comparison Operators

* Compare Integers with <, >, <=, >=, ==, !=
* Compare Strings with ==, !=
* Compare variables
* Every comparison evaluates to either `true` or `false`

^ Before we get into flow control, we need to be able to use what are called COMPARISON OPERATORS. Similar to how they sound, they compare things.
You have seen < and > in math class, right? We use those in code too! We can compare integers using < > <= >=. We can compare strings with ==.

---

# IF Syntax

```swift
dogAge = 1

if dogAge < 2 {
  print("You are a puppy 🐶")
}
```

^ Now that we know how to compare things, we can tell our program to take a different path based on what a certain variable may or may not be! We use this by writing an IF statement. Essentially, it says, "If <my situation is equal to true>, then do this thing!"
Let's look at this example. We have a variable `dogAge` assigned to the integer of 1. Next we see the `if` keyword - this tells the computer, please wait and listen for what I'm about to give you - I'll need you to check if it is true or false. Then we provide what is called a condition. If the condition is TRUE, the computer looks inside the curly braces and executes any code it finds there.
In this situation, `dogAge` == 1, which IS less than 2, so this condition evaluates to TRUE. The computer then reads the code inside the curly braces, and prints out, "You are a puppy 🐶"
DISCUSS: What will happen if we changed dogAge to 4?

---

# What if we want several options?

```swift
if dogAge < 2 {
  print("You are a puppy 🐶")
}

if dogAge > 12 {
  print("You are elderly 💗")
}

etc...
```
^ Instead of just telling puppies that they are puppies, I'd like to tell dogs over the age of 12 that they are elderly, and all the dogs in between puppies and elderlies that they are also awesome. I could write out several IF statements, but that seems kind of tedious...

---

# else if and else

```swift
if dogAge < 2 {
  print("You are a puppy 🐶")
}
else if dogAge > 12 {
  print("You are elderly 💗")
}
else {
  print("You are also awesome 🐾")
}

etc...
```
^ The Swift language also gives us this keyword/phrase - `else if`. It works JUST like IF - takes a condition to evaluate, then runs a code block if the condition is met. We also get this ELSE statement, which 'catches' any other situation. If the dog is not less than 2 or greater than 12, the else code will be executed.

---

# Vocabulary Reflection

* Condition
* Comparison Operator
* Evaluate

---

# Conditionals - Lab

Practice some flow control with your favorite food!

^ Circulate and make sure students are on the right track with setup. Make sure they have declared a favoriteFood variable and assigned it.
Ask, "why is favoriteFood == "Chipotle" your first condition?"
"Why do we have to give 'else if' statements a condition?"
"Why don't we have to give 'else' statements a condition?"

---

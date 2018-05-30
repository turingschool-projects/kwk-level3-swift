footer: KWK Swift/iOS: Conditionals
slidenumbers: true

# Conditionals

---

# Learning Goals

* Students will use if/else if statements to control flow of an application
* Students will use comparison operators

---

# Flow Control

* In life, we make decisions based on our current situation:
  * If I'm hungry, I'll eat
  * If I'm tired, I'll take a nap

* We do the same thing in programming:
  * If a user is signed in, they see their account
  * If no one is signed in, the user is prompted to do to

^ Turn and Talk - what are some other examples where we make decisions in real life? How about in apps or programs - besides being logged in/out, where else do we see different things happening?

^ The idea of an application doing different things, going in different directions based on what the user wants is called FLOW CONTROL. It's a very important concept because it is constantly being used - no matter what language you work in!
---

# Comparison Operators

* Compare Integers with <, >, <=, >=, ==, !=
* Compare Strings with ==, !=
* Compare variables
* Each comparison evaluates to either `true` or `false`

^ Before we get into flow control, we need to be able to use what are called COMPARISON OPERATORS. Similar to how they sound, they compare things.

^ Surely you have seen < and > in math class, right? We use those in code too! We can compare integers using < > <= >=. We can compare strings with ==.

---

# IF Syntax

```
dogAge = 1

if dogAge < 2 {
  print("You are a puppy 🐶")
}
```

^ Now that we know how to compare things, we can tell our program to take a different path based on what a certain variable is! We use this by writing an IF statement. Essentially, it says, "If <my situation evaluates to true>, then do this thing!"

^ Let's look at this example. We have a variable `dogAge` assigned to the integer of 1. Next we see the `if` keyword - this tells the computer, please wait and listen for what I'm about to give you - I'll need you to check if it is true or false. The we provide what is called a condition. If the condition is TRUE, the computer looks inside the curly braces and executes any code it finds.

^ In this situation, `dogAge` == 1, which IS less than 2, so this condition evaluates to TRUE. So the computer reads the code inside the curly braces, and prints out this sentence.

^ DISCUSS: What will happen if we changed dogAge to 4?

---

# What if we want several options?

```
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

```
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
^ The Swift language also gives us a keyword/phrase - `else if`. It works JUST like IF - takes a condition to evaluate, then reads a code block if the condition is met. We also get this ELSE statement, which 'catches' any other situation. If the dog is not less than 2 or greater than 12, the else code will be executed.

---

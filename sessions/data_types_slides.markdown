footer: KWK Swift/iOS: Data Types and Variables
slidenumbers: true

# Data Types and Variables

---

# Learning Goals

* Students will be able to differentiate strings, integers, floats and doubles
* Students will be able to create and modify variables
* Students will be able to use string interpolation to write a sentence using variables

---

## Technical Vocabulary

* String
* Integer
* Interpolation
* Variable
* Keyword

---

# Strings

* A string is a series of characters

* This includes letters, numbers, and symbols. We are able to tell when something is a string because it's in between two quotation marks

* For example, `"Hello, world."` is a string. `"puppies"`. is also a string. And so is `"1234"`

---

# Numbers

* In the most simple terms possible, we have two kinds of numbers, Integers and Doubles
* The math operations we use all the time can be used on both of these

^ Lead a quick discussion and write outcomes on whiteboard - what math operations do we have?
Addition, subtraction, multiplication, division, parenthesis, (if it doesn't come up, I would point out that order of operations is the same as it is in math class.)
---

# Integers

Integers are what we would think of as whole numbers. They can be positive or negative or zero. So, 1, 3, 4, -56 and 0 are all integers. The official definition of an integer is that it is a whole number that has **no** fractional component.

---

# Float and Double

* Swift gives you two data types with which to store numbers that have a fractional component, which we can refer to as numbers with decimals. They can be positive or negative

* Examples would be 1.1, 42.45, 3.14, -123786234.64 and so forth

* The TL;DR is that Doubles have more accuracy than Floats, and you get to choose how much accuracy you want - how many decimal places you can use if you want

* If you ever need a decimal, **use a Double** because you'll get more accuracy that way

---

# Turn and Talk

* Turn to a new best friend and explain the difference between an Integer and a Double

---

# Variables

* So now that we know a few data types, we want to talk about how we can work with them. And we use variables for that.

* Variables are these things that we use in order to reference and label information that we're going to use in our programs.

* But why should we use variables? They're kind of a shortcut. Let's say we were working with our address and it's a string, "1313 Mockingbird Lane" it would be annoying to have to type that in every time we wanted to use it.

---

# Variables - Syntax

```
var address = "1313 Mockingbird Lane"
```

* What we've done in that line of code above is we told the computer, "Hey, I want you to create a variable called address, and I want you to store in it the string, "1313 Mockingbird Lane".
* Every time I need to use my address, I only have to type the word `address`!

---

# Variables

```
var address = "1313 Mockingbird Lane"
```

* We use the `var` keyword here to tell the computer that in this following bit of code, we are going to declare a variable. We have to declare variables before we use them

^ KEYWORDS are special, reserved words in the language. Every programming language has them. We can't use them for any other purpose (variable or function or class name), only if it's in a string.
Xcode is helpful because it shows all keywords in pink.
If you tried to write this without the keyword `var` Xcode will throw an error!

---

# Variables

* After we declare a variable, we can change the contents of the variable at will. If we were to move from 1313 Mockingbird Lane to 254 Ocean Avenue, we would do this:

```
address = "254 Ocean Avenue"
```
* Notice we did NOT use the keyword `var` this time - that's because we REassigned the variable

---

# Turn and Talk

With your new best friend, can you come up with some other variables and the sorts of things they might hold? Try to come up with variables that would be both numbers and text!

^ Circulate and listen in, have a short discussion afterwards.
BOOLEANS might come up - it is simply true or false - they are an important concept in programming!

---

# String Interpolation

* Interpolation allows us to put variables and strings together
* "\(VARIABLE NAME HERE) any other words here"
* I'd like to write a sentence that says "I am 15 years old", but using the age variable: `var age = 15`

* Solution: "I am \(age) years old"

---

# Data Types Lab

* Students will assign values to variables
* Students will use string interpolation to write sentences
* Students will use math operations to manipulate variables assigned to integers

^ The first three challenges are completely aligned with info in slides and students should be able to complete independently; the last challenge is quite difficult so they may need a nudge.

---

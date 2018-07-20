footer: KWK Swift/iOS: Arrays
slidenumbers: true

# Arrays

---

# Learning Goals

* Students will understand what an array is and why they are useful
* Students will learn how to create an array and modify values within an array
* Students will learn how to iterate over arrays

---

# Technical Vocabulary

* Array
* Index
* Element
* Initialize
* Iterate

---

# What is an Array?

* An array is an _ordered_ collection that stores multiple values of the same type
* An array can store any kind of element - from integers to strings to objects
* Elements inside an array are separated by a comma

---

# When would we use them?

Arrays are useful whenever you need to keep track of an ordered list of things. This is similar to how we keep track of lists in the real world. When we write out a grocery shopping list, we use _one_ piece of paper to keep track of all the items we need.

---

# Creating an Array

Now that we know a bit about arrays, we want to talk about how to create them. We can initialize them in 1 of 2 ways:

- Empty
- With data 

---

# Creating an Array

```swift
var arrayOfStrings = [String]()

var arrayOfIntegers = [Int]()
```

^ It's worth to point out - every element of an array in Swift MUST be the same data type. In JavaScript and Ruby, the students may have seen that arrays can hold anything, for example [1, "hello", true] could be a valid array. Swift is more strict and does NOT allow that.
These examples initialize empty arrays.

---

# Creating an Array

Starting with Data: Instead of declaring an empty array, we can also declare an array that starts with data, like this:

```swift
var shoppingList = ["Bread", "Cheese", "Milk", "Bacon"]
```

---

# Turn and Talk

* Turn to a new best friend and explain the following:
  - What is an array? 
  - Why are they useful?
  - How do you declare an array?

---

# Accessing Information

Each element in an array is automatically assigned a number called an **index**. This index can be used to access a specific element inside the array.

Indices begin at 0 and count up. 

---

# Accessing Information - cont

Indices begin at 0 and count up. If we look back at our `shoppingList` array, the following would be true:

* "Bread" has an index of 0
* "Cheese" has an index of 1
* "Milk" has an index of 2
* "Bacon" has an index of 3  

---

# Accessing Information

By using the square brackets, we can use the index to access a specific value in an array.

```swift
var shoppingList = ["Bread", "Cheese", "Milk", "Bacon"]

shoppingList[2]
=> "Milk"

shoppingList[0]
=> "Bread"
```
^ You may want/need to explain that these lines `=> "Milk"` and `=> "Bread"` are indicating the return value of the previous code; it's just a way to notate what happens after writing some code.

---

# Updating Information

We can also update elements with the square bracket syntax we looked at earlier. We access the index value that we would like to change, and then reassign a new value for that index with a  `=`

```swift
shoppingList[2] = "Candy"

=> ["Bread", "Cheese", "Candy", "Bacon"]
```

---

# Adding Information

A common way to add something to an already existing array is to use the append() method - which will add an element to the end of the array

```swift
shoppingList.append("Pasta")

=> ["Bread", "Cheese", "Candy", "Bacon", "Pasta"]

```

---

# Removing Information

A common way of removing elements is to use the remove(at:) method - which will remove an element at whatever index you type in after the `at:`

```swift
shoppingList.remove(at: 0)

=> ["Cheese", "Candy", "Bacon", "Pasta"]

```

---

# Iterating Over Elements in an Array

When you need to perform an operation on all of an array's elements, you can **iterate** over the array.  The most common way to do this is to use a `for-in` loop.

Looking back at our shopping list from earlier, we can use a `for-in` loop to print every value in the array.

---

# Iterating Over Elements in an Array

```swift
for item in shoppingList {
  print(item)
}

=> "Cheese"
=> "Milk"
=> "Candy"
=> "Pasta"
```

^ We will go into more detail on loops tomorrow - the focus here should be more on the CONCEPT of iterating through a collection.
Discussion - let's think about Instagram - where might that application use arrays? (list of followers, list of images to show on screen, list of people who liked a photo, etc.) <Pick one strong example to continue with> Why might the Instagram application need to iterate over it's array of ___________? (most likely this will be around 'rendering' or showing the data on the screen. We would iterate over the list of followers and for each one, render a template with that followers specific info.)
  
---

# Vocabulary Reflection

* Array
* Index
* Element
* Initialize
* Iterate

---

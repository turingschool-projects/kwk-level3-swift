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
* An array can store any kind of elements - from integers to strings to objects
* Elements inside an array are separated by a comma
* The same value can appear in an array at multiple positions

---

# When would we use them?

Arrays are useful whenever you need to keep track of an ordered list of items. This is similar to how we keep track of lists in the real world. When we write out a grocery shopping list, we use _one_ piece of paper to keep track of all the items we are looking to purchase. Arrays are a way to keep track of a collection of data.

---

# Creating an Array

Now that we know a bit about arrays, we want to talk about how to create them. We will start by initializing an empty array - which is generally done in 1 of 2 ways:

* Shorthand Syntax
- With this syntax, we have to declare the data type of the array elements. Below we are declaring an empty array and specifying that we will be storing strings.

```
var arrayOfStrings = [String]()
var arrayOfIntegers = [Int]()
```

^ It's worth to point out - every element of an array in Swift MUST be the same data type. In JavaScript and Ruby, the girls may have seen that arrays can hold anything, for example [1, "hello", true] could be a valid array. Swift is more strict and does NOT allow that.

---

# Creating an Array

* Starting with Data
Instead of declaring an empty array, we can also declare an array that starts with data, like below:

```
var shoppingList = ["Bread", "Cheese", "Milk", "Cheese"]
```

---

# Turn and Talk

* Turn to a new best friend and explain the following:
- What is an array? Why are they useful?
- How do you declare an array?

---

# Accessing Information

Each element in an array is automatically assigned a number called an **index**. This index can be used to access a specific element inside the array.

Indices begin at 0 and order up incrementally. If we look back at our `shoppingList` array, the following would be true:

* "Bread" has an index of 0
* "Cheese" has an index of 1
* "Milk" has an index of 2
* "Cheese" has an index of 3  

---

# Accessing Information

By using the square brackets, we can use the index to access a particular value in an array.

```
var shoppingList = ["Bread", "Cheese", "Milk", "Cheese"]

shoppingList[2]

=> "Milk"

shoppingList[0]

=> "Bread"
```

---

# Updating Information

We can also update elements with the square bracket syntax we looked at earlier. We access the index value that we would like to change, and then reassign a new value for that index on the right-hand side of the assignment operator `=`

```
shoppingList[2] = "Candy"

=> ["Cheese", "Milk", "Candy", "Pasta"]
```

---

# Adding Information

A common way to add something to an already existing array is to use the append() method - which will add an element to the end of the array

```

shoppingList.append("Pasta")

=> ["Bread", "Cheese", "Milk", "Cheese", "Pasta"]

```

---

# Removing Information

A common way of removing elements is to use the remove(at:) method - which will remove an element at whatever index is given

```
shoppingList.remove(at: 0)

=> ["Cheese", "Milk", "Cheese", "Pasta"]

```

---

# Iterating Over Elements in an Array

When you need to perform an operation on all of an array's elements, you can **iterate** over the entire set of values in an array.  The most common way to iterate over values in an array is to use a `for-in` loop.

Looking back at our shopping list from earlier, we can utilize a `for in` loop to print every value in the array at every index, from 0 to the last element

```
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

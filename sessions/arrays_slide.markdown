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
* Initialize
* Iteration/Enumeration
---

# What is an Array?

* An array is an _ordered_ collection that stores multiple values of the same type
* An array can store any kind of elements - from integers to strings to classes
* Elements within an array are comma separated
* The same value can appear in an array at multiple positions


# When would we use them?

Arrays are useful whenever you need to keep track of an ordered list of items. At a high level, this is similar to how we keep track of lists in the real world. When we write out a grocery shopping list, we use _one_ piece of paper to keep track of all the items we are looking to purchase. Arrays are a way to keep track of a collection of data.


# Create an Array

Now that we know a bit about arrays, we want to talk about how to initialize them. We will start by initializing an empty array - which is generally done in 1 of 2 ways:

* Shorthand Syntax
- With this syntax, we want to specify the element type of our Array in the declaration. Below we are declaring an empty array tand specifying that we will be storing strings

```
var arrayOfStrings = [String]()
```

* Array literal
- This syntax allows us to initialize an empty array just like we did in the example above.

```
var arrayOfStrings:[String] = []
```

Instead of declaring an empty array, we can also declare an array that starts with data, like below:

```
var shoppingList = ["Bread", "Cheese", "Milk", "Cheese"]
```

# Turn and Talk

* Turn to a new best friend and explain the following:
- What is an array? Why are they useful?
- How do you declare an array?

# Access Information

Each value in an array is automatically assigned a number called an index. This index can be utilized to access a particular value within the array.

Indices begin at 0 and order up incrementally. If we look back at our `shoppingList` array, the following would be true:

* "Bread" has an index of 0
* "Cheese" has an index of 1
* "Milk" has an index of 2
* "Cheese" has an index of 3  

By using subscripting square brackets, we can use the index to access a particular value in an array.

```
var shoppingList = ["Bread", "Cheese", "Milk", "Cheese"]

shoppingList[2]

=> "Milk"

shoppingList[0]

=> "Bread"
```

# Updating, Adding, and Removing Information

A common way to add something to an already existing array is to use the append(\_:) method - which will add an element to the end of the array

```

shoppingList.append("Pasta")

=> ["Bread", "Cheese", "Milk", "Cheese", "Pasta"]

```

A common way of removing elements is to use the remove(at:) method - which will remove an element at whatever index is given

```
shoppingList.remove(at: 0)

=> ["Cheese", "Milk", "Cheese", "Pasta"]

``` 

We can also update elements with the subscripting syntax we looked at earlier. We access the index value that we would like to change with subscripting and reassign a new value for that index on the right-hand side of the assignment operator `(=)`

```
shoppingList[2] = "Candy"

=> ["Cheese", "Milk", "Candy", "Pasta"]
```

# Iterating Over Elements in an Array

When you need to perform an operation on all of an array's elements, you can iterate over the entire set of values in an array.  The most common way to iterate over values in an array is to use a `for-in` loop. 

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


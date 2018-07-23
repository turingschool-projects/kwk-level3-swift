footer: KWK Swift/iOS: Dictionaries
slidenumbers: true

# Dictionaries

---

# Learning Goals

* Students will understand the difference between dictionaries and arrays
* Students will know why we sometimes choose to use dictionaries over arrays
* Students will know syntax to create dictionaries and access information from them

---

# Technical Vocabulary

* Dictionary
* Key/Value pair

---

# What are they?

* Another way to hold multiple pieces of data (collection)
* Has key/value pairs, not ordered
* The key can be thought of as a title
* The value is usually the meat of the data we care about

---

# When would we use them?

* When we want to hold multiple pieces of data in one place
* When we don't care about the order of items (array)
* When we need an _associative_ relationship (title for some info)

^ Provide one example and non-example - example: list of human names and their pets. non-example (better for array) - list of all the dogs in my building. 

---

# Vocabulary Reflection

* Dictionary
* Key/Value pair

---
# Array or Dictionary

Turn and Talk: For each set of data, would an array or dictionary be better to store it? Why?

- List of all of the students in class
- List of states and their capitals
- List of things to pack for vacation
- Names of all the Instagram accounts I follow
- List of students and their birthdays

^ Students - array, State/Capitals - dictionary, Packing - dictionary, Instagram - array, Students/Birthdays - dictionary
Lead a discussion on why each data type is better for the given list

---

# Create a Dictionary

```swift
var phones : [String : String] = [:]

print(phones)
=> [:]
```

^ Next slide has an explanation

---

# Create a Dictionary

```swift
var phones : [String : String] = [:]
```
I have a variable called `phones`, which is currently an empty dictionary which will hold a String in the key and a String in the value.

---

# Add key/value pairs

```swift
phones["apple"] = "iPhone"
phones["google"] = "Pixel 2"

print(phones)
=> ["apple": "iPhone", "google": "Pixel 2"]
```

^ the first line is adding a key of "apple" that points to the value of "iPhone", etc.

---

# Access Information

Since we access values with the key, keys must be unique, meaning you can't have two things with the same key:

```swift
print(phones["apple"])

=> Optional("iPhone")
```

^ Make sure to point this out: the way we access values from a dictionary is by using the key - this means that we can't re-use keys. If you have multiple things with a similar title, you'll see programmers use key_1, key_2, etc.
Notice that `Optional("iPhone")` was printed - not just the string "iPhone", like you probably expected. Swift is very specific and wants to make sure that there IS DATA stored in the dictionary (in this case, phones["apple"]) before doing anything with the data; if it were `nil` it could cause problems in bigger programs. 
To tell Swift we are sure there is data, we do something called 'unwrapping' - by typing an exclamation point after the closing bracket. <MODEL in Playground>

---

# Remove key/value pairs

```swift
phones["apple"] = nil
```
^ Print a before and after to show what happens after this line of code

---

# Start a dictionary with data

```swift
var phones = [
  "apple": "iPhone",
  "google": "Pixel 2"
  ]
```

^ Remember, earlier we started a dictionary that started empty. This strategy allows us to initialize a dictionary WITH data. 

---

# **JUST** get the keys

Let's say we want a list of all the companies that make the phones, but we _don't_ want to have to look at the phone names.

```
phones.keys
Array(phones.keys)
```

^ `phones.keys` gives us a KEYS object with "apple", and "google" but is difficult to USE because KEYS is not a commonly used data type. Show this to the students by typing in:
print(phones.keys)
print(type(of: phones.keys))
print(Array(phones.keys))
print(type(of: Array(phones.keys)))
Typically, you'll see iOS developers wrap `Array()` around, in this case, the `phones.keys` so that KEYS objects can be converted into an ARRAY, which is much more friendly!

---

# Whiteboards

Create a dictionary with a list of 3 people (yourself, family, friends, or other students here!) and their birthdays

^ Give students ~5 minutes to white board, have partners give feedback, and then lead a debrief on how everyone did it (there should be little variation)

---

# Dictionaries - Lab

Create your friend or family tree - see the Lab markdown for details!

^ As you circulate, make sure students are using strings for both key and value pairs for the 'expected' portion. They will hopefully run into the issue of "keys must be unique"= - if you have three brothers they can't all have the key of "brother" (which is solved in the extension). You can advise the to use youngest/oldest, brother1, brother 2, etc.

---

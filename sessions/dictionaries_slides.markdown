footer: KWK Swift/iOS: Dictionaries
slidenumbers: true

# Dictionaries

---

# Learning Goals

* Students will understand the difference between dictionaries and arrays
* Students will know why we sometimes choose to use dictionaries over arrays
* Students will know syntax to create dictionaries and access information from them
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
* When we need an associative relationship (title for some info)

---

# Array or Dictionary

Turn and Talk: For each set of data, would an array or dictionary be better to store it? Why?

- List of things to pack for vacation
- List of all of the students in class
- List of states and their capitals
- Names of all the Instagram accounts I follow
- List of students and their birthdays

^ Packing - dictionary, Students - array, State/Capitals - dictionary, Instagram - array, Students/Birthdays - dictionary
Lead a discussion on why each data type is better for the given list

---

# Create a Dictionary

```
var phones = [String, String]()

print(phones)
=> [:]
```

---

# Create a Dictionary

```
var phones = [String, String]()
```
I have a variables called phones, which is currently an empty dictionary which will hold a String in the key and a String in the value.

---

# Add key/value pairs

```
phones["apple"] = "iPhone"
phones["google"] = "Pixel 2"

print(phones)
=> ["apple": "iPhone", "google": "Pixel 2"]
```

---

# Access information

Since we access values with the key, keys must be unique
```
phones["apple"]

=> Optional("iPhone")
```
^ Make sure to point this out: the way we access values from a dictionary is by using the key - this means that we can't re-use keys. If you have multiple things with a similar title, you'll see programmers use key_1, key_2, etc.

---

# Remove key/value pairs

```
phones["apple"] = nil
```

---

# Start a dictionary with data

```
var phones = [
  "apple": "iPhone",
  "google": "Pixel 2"
  ]
```

---

# Whiteboards

Create a dictionary with a list of 3 people (yourself, family, friends, or other students here!) and their birthdays

^ Give students ~5 minutes to white board, have partners give feedback, and then lead a debrief on how everyone did it (there should be little variation)

---

# Dictionaries - Lab

Create a dictionary with a list of 3 people (yourself, family, friends, or other students here!) and their birthdays

^ As you circulate, make sure students are using strings for both key and value pairs for the 'expected' portion. They will hopefully run into the issue of "keys must be unique"= - if you have three brothers they can't all have the key of "brother" (which is solved in the extension). You can advise the to use youngest/oldest, brother1, brother 2, etc.

---

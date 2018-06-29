#### Expected

* Hobbies array
- Create an array of your top five favorite hobbies
- Change at least one of the values in the array
- Add a new hobby to the array
- Remove the second hobby from the array
- Print the value of the third element of the array
- You should have five hobbies in your array. Using a `for in` loop and string interpolation, iterate over the values in your array in order to print five strings that say "I love ______!"

```
var myHobbies = ["coding", "drinking coffee", "hanging out with friends", "playing with my dogs", "working out"]
// change a value
myHobbies[1] = "swimming"

// remove 2nd - when I hear 2nd I think the second element I see, NOT the index 2. Some may interpret this different, it's not the biggest deal if so.
myHobbies.remove(at: 1)

// print 3rd
print(myHobbies[2])

// loop to create sentence
for hobby in myHobbies {
  print("I love \(hobby)!")
}

```

#### Extension

There are several ways to add, remove, and modify values in an array. There is also a variety of other ways to iterate over arrays. Using Google/Swift documentation, find a different way to do each of the following:

- add an element
  The insert method allows you to specify why index to insert a new element.
  `myHobbies.insert("running", at: 3)` would insert "running" at index 3 and push all the the following hobbies back one index
- remove an element
  The removeLast method removes the last index
  `myHobbies.removeLast()` - it does not take an argument since it will automatically remove the last index.
- modify an element
  `myHobbies[0].value` - can't find an advantage/use case for why I'd ever want this over just the index...🤷🏼‍
- iterate
  The forEach method does the same thing as a for...in loop (the are some differences, but for more advanced concepts that we won't go into at this camp)
  
  ```
  myHobbies.forEach { hobby in
    print("I love \(hobby)!")
  }
  ```

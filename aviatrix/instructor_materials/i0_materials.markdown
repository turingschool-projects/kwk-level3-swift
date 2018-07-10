# Aviatrix I0: Up & Running

### `start`

You'll see that there's a function named `start` which currently always returns `true`. We'll later use this to make sure that the plane is running before we fly anywhere.

Add the `running` instance variable so it defaults to false, then changes to true when the `start` function is called. Return that boolean out of the function.

```
var running = false

fun start() -> Bool {
  running = true
  return running
}
```

That way our method will return the value of the `running` variable.

### `author`

To make sure other know who build this program, we want to be able to display your name! In your `Aviatrix` class, create an author instance variable (data type: String, value: none, yet), and write an `init` function to pass an argument in when you create an Aviatrix object.

```swift
class Aviatrix {

  var running = false
  var author : String

  init(studentName : String) {
      author = studentName
  }

  // more code below
}
```

In `main.swift` there is a line that prints to the console: print("Welcome to the Aviatrix Flight System by _ _ _ _ _ _ _ _ _ " ) - change that so your author variable is interpolated.


```swift
var av = Aviatrix(studentName: "Amy")
print("Welcome to the Aviatrix Flight System by \(av.author)")
```

```swift
print("Thanks for flying with \(av.author)'s airline!")
```

### Run It

Run the program and observe the `author` output in the first line of the program.

Let's keep going! [Move on to Iteration 1](./i1_destinations.markdown)

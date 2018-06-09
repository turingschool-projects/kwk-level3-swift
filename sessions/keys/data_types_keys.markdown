### String Interpolation

If you have the strings `"First"` and `"Last"` in the following variables:

```
var f = "First"
var l = "Last"
```

Use *only* the "string interpolation" technique to complete the following:

1. What code can you write to output the string `"FirstLast"`?

  `"\(f)\(l)"`

2. What code can you write to output the string `"LastFirst"`?

  `"\(l)\(f)"`

3. What code can you write to output the string `"First Last"`?

  `"\(f) \(l)"` (notice the space between `)` and `\`)

4. What code can you write to output the string `"Last First Last First"`?

  `"\(l) \(f) \(l) \(f)"`

### Integers

Start with these numbers:

```
var a = 12
var b = 65
var c = 31
var d = 98
```

1. Write code to find the average of these four numbers.

  ```
  var sum = a + b + c + d
  var average = sum / 4
  ```

  OR

  ```
  var average = (a + b + c + d) / 4
  ```

2. Find the average yourself using paper or a calculator. Is your answer different than you found in A? Why?

  Answers will vary

3. Say you have the operation `a + b * c / d`. What result do you get out from Swift? What other outputs can you get out by adding one or more pairs of parentheses to the equation?

  `32` - because we input integers, we get back integers. Actual answer is 32.56...
  Order of Operations - Multiplication, Division, then Addition
  Any operation that parentheses is wrapped around will take precendence in OofO

### Happy Birthday

Let's sing Happy Birthday to our favorite celebrity. Their name should be stored in a variable, just in case you want to sing to someone else.

  ```
  var name = "Selena Gomez"
  "Happy birthday to you, happy birthday to you, happy birthday to \(name), happy birthday to you!"
  ```


### String Compression

There's a silly compression algorithm that outputs the first letter, the number of letters in the middle,
and the last letter. So for the string `"Kalamazoo"` it'd output `"K7o"` or `"Denver"` would be `"D4r"`.
Can you write code to implement that?

  If they get to this point, they will likely need to google!
  Some prompts if they are stuck:
    - Google for how to find the length of a string in Swift
    - Google for how to access the first and/or last character in a string

  One solution:  
  ```
  var name = "Kalamazoo"
  var middleLength = name.count - 2
  print("\(name.first!)\(middleLength)\(name.last!)")
  ```

  Another way to access the "K" is: `name[name.startIndex]`, and "o" name[name.endIndex]

  There are _multiple_ ways to solve this one!

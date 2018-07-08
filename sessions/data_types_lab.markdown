# Lab Notes: Data Types and Variables

## Learning Goals

* Students will assign values to variables
* Students will use string interpolation to write sentences
* Students will use math operations to manipulate variables assigned to integers

### String Interpolation

String values can be added together (or concatenated) with the addition operator (+) to create a new String value:

```
let string1 = "hello"
let string2 = " there"
var welcome = "\(string1) \(string2)"
// welcome now equals "hello there
```

If you have the strings `"Beyonce"` and `"Knowles"` in the following variables:

```
var first = "First"
var last = "Last"
```

Use *only* the "string interpolation" technique to complete the following:

1. What code can you write to output the string `"BeyonceKnowles"`?
2. What code can you write to output the string `"KnowlesBeyonce"`?
3. What code can you write to output the string `"Beyonce Last"`?
4. What code can you write to output the string `"Knowles Beyonce Knowles Beyonce"`?


### Integers

Start with these numbers:

```
var a = 12
var b = 65
var c = 31
var d = 98
```

1. Write code to find the average of these four numbers.
2. Find the average yourself using paper or a calculator. Is your answer different than you found in A? Why?
3. Say you have the operation `a + b * c / d`. What result do you get out from Ruby? What other outputs can you get out by adding one or more pairs of parentheses to the equation?

### Happy Birthday

Let's sing Happy Birthday to our favorite celebrity. Their name should be stored in a variable, just in case you want to sing to someone else.

### String Compression

There's a silly compression algorithm that outputs the first letter, the number of letters in the middle, and the last letter. So for the string `"Kalamazoo"` it'd output `"K7o"` or `"Denver"` would be `"D4r"`.

Can you write code to implement that?

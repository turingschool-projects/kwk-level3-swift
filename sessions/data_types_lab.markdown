# Lab Notes: Data Types and Variables

## Learning Goals

* Students will identify valid data types.
* Students will assign things to variables.


## Plan

### String Concatenation

String values can be added together (or concatenated) with the addition operator (+) to create a new String value:

let string1 = "hello"
let string2 = " there"
var welcome = string1 + string2
// welcome now equals "hello there

If you have the strings `"First"` and `"Last"` in the following variables:

```
var f = "First"
var l = "Last"
```

Use *only* the "string concatenation" technique to complete the following:

1. What code can you write to output the string `"FirstLast"`?
2. What code can you write to output the string `"LastFirst"`?
3. What code can you write to output the string `"First Last"`?
4. What code can you write to output the string `"Last First Last First"`?


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
3. Say you have the operation `a + b * c / d`. What result do you get out from Ruby? What other outputs can you
get out by adding one or more pairs of parentheses to the equation?

### Happy Birthday

In our family we like to say "Happy" once for every year of your age when we say "Happy birthday!". So when you turn
four we'd say "Happy happy happy happy birthday!" Note the capitalization.

Say you have an `age` variable that holds the person's age. Write code to output the appropriate greeting.

### String Compression

There's a silly compression algorithm that outputs the first letter, the number of letters in the middle,
and the last letter. So for the string `"Kalamazoo"` it'd output `"K7o"` or `"Denver"` would be `"D4r"`.
Can you write code to implement that?
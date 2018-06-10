#### Expected - FavoriteFoods

```
var favoriteFood = "Mac N Cheese"

if favoriteFood == "Chipotle" {
  print("Chipotle is my favorite, too 🌯")
}
else if favoriteFood == "Frappuccino" {
  print ("My favorite flavor is Chocolate 🍫 ")
}
else {
  print("I need to try that one!")
}
```
^ Here, we should see "I need to try that one!" print out to the terminal


```
var favoriteFood = "Chipotle"

if favoriteFood == "Chipotle" {
  print("Chipotle is my favorite, too 🌯")
}
else if favoriteFood == "Frappuccino" {
  print ("My favorite flavor is Chocolate 🍫 ")
}
else {
  print("I need to try that one!")
}
```
^ Here, we should see "Chipotle is my favorite, too 🌯" print out to the terminal


#### Extension
* Write a conditional that tells a student if they are in elementary, middle, or high school based on their grade level.

```
gradeLevel = 8

if gradeLevel <= 5
  print("you are in elementary school!")
else if gradeLevel <= 8
  print("you are in middle school")
else                                    // this could also be: else if gradeLevel > 8
  print("you are in high school!")
```

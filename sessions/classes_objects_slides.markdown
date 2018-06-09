footer: KWK Swift/iOS: Classes and Objects
slidenumbers: true

# Classes and Objects

---

# Learning Goals

* Students will

- command line tool, --> macOS project
- maybe i'll just have a starter repo for them to download?? how does that wokr??

---

# Technical Vocabulary

* class
* object
* property
* initializer
* actions

---

# Class == Blueprint

* In programming, 'class' is a special word
* A class is like a blueprint, or a cookie cutter
* We have one class that has all the basics, then we create objects based on a class

^ Walk through talking points
It makes a lot more sense with an example, so let's talk about a STUDENT. (You might want to whiteboard this out as you walk)
We can have a student class/blueprint. What are things that all students HAVE? (Solicit answers - name, age, grade, favorite XYZ, etc.)
Great, every student has _______, but the details of those things will vary from student to student. We don't want to say that every student is named _______, but we do want to know every student's name.
A class sets the framework for us - it says that objects can have certain pieces of info and can do certain things, but it doesn't deal with the details. We'll get to that soon!
Let's actually LOOK at a class

---

# Class syntax

* start with keyword `class`, lowercased
* class name is next, capitalized
* open code block with curly brackets

```
class Student {

}
```

---

# Working with Classes in Xcode, Properties

* create project --> macOd --> Terminal App
* create new file in main directory - in that file:


```
class Student {

}
```

^ Instructor should model going through the process of creating a Terminal app in Xcode and creating new file.
Model writing the class syntax - THEN:
- add inside of the class code block:     
var grade = 10
var studying = "Swift"
var name = "pick a name!"
Explain that "grade" and "studying" and "name" are PROPERTIES of this class
One problem - the name is going to be the same for every student. Next slide explains.

---

# Creating an Object

* go back to main.swift file
* create a variable, assigned to Student()
```
var newStudents = Student()
print(newStudent)
```


^ FIRST: Explain that newStudent is a variable which stores a student object. Back to cookie cutter reference, it is a cookie that was created by the Student cookie cutter.
SECOND: Instructor should model putting this code into their project's main.swift. Be careful - to run the code, you have to click the play button in top left-ish, OR `cmd + r `. ALSO, you have to open up the console drawer - click the center of the three icons in top right corner of Xcode.
Notice that when you print(newStudent) - we get `ClassesObjects.Student` - that tells me this is an object from the class of 'Student'. Cool, but I wanted to the information - grade and studying - to show up.
Change your print statement to print(newStudent.grade) and add in print(newStudent.studying) and print(newStudent.name) - run `cmd + r` again, and you should see `10`, then `Swift`, then `the name you typed in` printed out to the console.
Explain to the students that by calling "dot then a property" we are accessing a specific property of this OBJECT.

---

# Initializer

* init (Initializer Declaration)
* It runs once and only once - when we create a new object from the class
* It is written inside the class, below any property variables we declare

^ INIT - the initializer is a special function inside of a class. "init" is a keyword, if you write a function called "init", it will be called when you create an object from that class.
It can take arguments, which can help make our class dynamic, in this case, give each student their own name.

---

# Initializer

```
var grade = 10
var studying = "Swift"
var name = ""     // default this to an empty string!

init(studentName : String) {
  name = studentName
}
```
^ Let's add this init function into our class, giving it an argument of studentName, which is a string.
Inside of init, let's re-assign `name` to whatever studentName was passed in.
This won't work quite yet - we need to hop back over to main.swift - if we try to run this, we will see an error because Student() is now expecting an argument (it is recommended you SHOW this error to this students!)
let's pass it Student(studentName : "Pick another name") and re-run.
You should now see the print statement reflecting the new name that was passed in.
** If time permits, make the grade dynamic!

---

# Actions

* Classes can have properties AND actions!
* Actions are simply functions that are associated with a class.


^ Inside the code block of the class, we can add functions!
This means that every object created from a class, will have access to this function. Let's write one so we can see it in action.
<Move to Xcode to model>
write a function `writeCode() { }` inside the code block, print a string of "\(name) is busy writing code!"
Go back to main.swift, call newStudent.writeCode() and `cmd + r`! You should see a sentence printed to the console.
Re-iterate that `writeCode()` is a function, but more specifically an ACTION for this class, and this class only. You can even try calling it in main.swift withOUT the newStudent, preceding it, and see an error!

---

#### Class - Student

```
// Student.swift
var Student {

  var grade = 10
  var studying = "Swift"
  var name = ""

  init(studentName : String) {
    name = studentName
  }

  func writeCode() {
    print("\(studentName) is busy coding...")
  }
}
```

```
// main.swift
let student1 = Student(studentName : "Christie")
let student2 = Student(studentName : "Leta")

print(student1.name)
print(student1.grade)
print(student1.studying)
student1.writeCode()
print("\(student2.name) is in grade \(student2.grade) and studying \(student2.studying)!")
```
#### Expected

* With your partner, brainstorm another class. Remember, we used Student because all students share some things, and also had some unique things about them. If you are struggling for an idea, Car and Dog are both commonly used to practice work with classes 🚗 🐶
* With your partner, write a list of properties your class should have. What is true about every ____? (If you are talking about a car, every car has wheels...)
* What function, or action, do you want your _____ to take? (If it's a car, I would want it to drive forward, reverse, stop...) Come up with at least 2 actions!
* Create a new (macOS, Swift) file inside of the ClassesAndObjects folder, name it the same thing you will name your class
* Write your class
* Create variables for the properties your class needs
* Write the actions for your class
* In main.swift, create at least one object with this class and do some printing to make sure your class is behaving as expected
* Add in an `init` function so you can pass your class something specific to the object you are creating. (For a car, I would definitely want to make sure the color could change!)

  Notes:
    - Class - DOG!
    - Properties: name, breed, floppy ears (true or false), age
    - Functions: bark, eat, play

  ```
  // Dog.swift
  class Dog {

    var name = ""
    var breed = ""
    var age = 0
    var floppyEars = true

    init(dogName : String, breedType : String, ears : Bool, dogAge : Int) {
      name = dogName
      breed = breedType
      floppyEars = ears
      age = dogAge
    }

    func bark() {
      print("Woof!")
    }

    func play() {
      print("My name is \(name) and I'm ready to play!!")
    }
  }
  ```

  ```
  // main.swift
  let oscar = Dog(dogName : "Oscar", breedType : "Shih=Tzu", ears : true, dogAge : 6)
  ```

#### Extension

* Read this [blog post](https://www.weheartswift.com/swift-classes-part-2/)
* What is a scenario where you could use a superclass and subclass?
* If you still have time, try to build the superclass and subclass you brainstormed. You can just create a new file in the project you've been working in.

  Notes:
    - Pet could be a superclass, dog and cat could be subclasses. The both have names, ages, and colors of fur. They both play and eat.

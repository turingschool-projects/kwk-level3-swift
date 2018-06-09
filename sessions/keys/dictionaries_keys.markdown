## Whiteboards KEY

Create a dictionary with a list of 3 people (yourself, family, friends, or other students here!) and their birthdays

  ```
  var birthdays = [String : String]()

  birthdays["Amy"] = "September 15"
  birthdays["Christie"] = "December 29"
  birthdays["Brittany"] = "September 9"
  ```

  OR, (and truly, preferred):

  ```
  var birthdays = [
    "Amy": "September 15",
    "Christie": "December 29",
    "Brittany": "September 9"
  ]
  ```

## Lab:

#### Expected

* Friend/Family Tree
  - Create a dictionary with keys that are family or friend titles (i.e. "sister", "bestFriend") and values that are the name of that family member or friend. Pets are family, too!
  - Aim to have at least 10 family members of friends in your 'tree'
  - Print to the console the entire dictionary
  - Print to the console 3 individual names
  - Remove someone from your tree  😔 (You can add them back if you want!)

  ```
  var familyTree = [
    "sister": "Megan",
    "other sister": "Juliana",
    "another sister": "Kate",
    "cousin": "Carrie",
    "cousin": "Lindsay",
    "niece": "Riley",
    "nephew": "Parker",
    "best friend": "Lindsey",
    "dog": "Sodie",
    "other dog": "Oscar",
  ]

  print(familyTree)
  print(familyTree["sister"])
  print(familyTree["niece"])
  print(familyTree["dog"])

  familyTree["sister"] = nil
  ```

#### Extension

* Create a dictionary in which the values are arrays of strings. This is called a _nested_ collection, because it has collections inside of a collection.

  ```
    var familyTree = [
      "sisters": ["Megan", "Juliana", "Kate"],
      "cousins": ["Carrie", "Lindsay"],
      "nieces": ["Riley"],
      "nephews": ["Parker"],
      "friends": ["Lindsey"],
      "dogs": ["Sodie", "Oscar"]
    ]
  ```
  A common mistake is NOT putting the 'singles' in an array (Riley, Parker, Lindsey). This is an issue because all keys must be of the same data type and all of the values must be of the same data type, since the first key/value pair was String/Array, all others must be.

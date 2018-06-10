### Functions

#### Expected

* With your partner, brainstorm another task you'd like to have this robot complete. You should agree on using the same task that way you can check in with each other throughout the lab. Once you've decided on it, share with an instructor to make sure it will work for all activities, then go to the next step
* In your notebook, write out the small steps that your robot needs to take in order to complete the task
* In your playground declare and call the function - the code block should be empty
* To make 100% sure you are calling it correctly, write a print statement into the code block and make sure that appears in your console
* Now, write a print statement for each of the commands you wrote down in your notebook. Are they all printing out as expected?

  Notes (some ideas...):
    - Take out trash
    - Feed the dog
    - Wash the dishes

  Feed the Dog:
    - pick up bowl
    - put bowl on counter
    - scoop 1 cup of food
    - dump food into bowl
    - put bowl on placemat

  ```
  func feedDog() {
    print("pick up bowl")
    print("put bowl on counter")
    // etc.
  }

  feedDog()
  ```

### Functions - Arguments

#### Expected

* Building off of your function already written - what information could you give this function to show different situations?
* Comment out your first function, and start over. This time, your function declaration should ask for an argument. It doesn't necessarily have to be an integer like the class example!
* Finish writing your function
* Call your function - a few times, passing in different arguments each time


  Notes:
    - Amount of food/size of scoop (in cups) *
    - Number of dogs to feed?

  ```
  func feedDog(amountOfFood : Int) {
    // possibly some of the previous statements...
    print("Scoop out \(amountOfFood) cups of food")
  }

  feedDog(amountOfFood : 2)
  feedDog(amountOfFood : 1)
  feedDog(amountOfFood : 5)
  ```

### Functions - Return Values

#### Expected

* With your partner, decide what information you want to return out of your function. What data type is most appropriate (string, integer, etc.)?
* In the declaration, tell your function you plan to return a value
* Use the return keyword to return the desired value
* Check yourself: did you return a number like "4" or a string like "Good job!"? To make this function dynamic, we should probably be returning a _variable_ that is storing something your calculated based on the argument passed in. Look back at the class example if you are stuck on this part!
* Call your function - a few times, passing in different arguments each time. STOP!
* Before you run your code, talk with your partner - what is the expected output/return value?


  Notes:
    - We could return the amount of time it took the dog to eat - average is 3 minutes per cup. (I pretty much made that up)
    - This would be an Integer, then we will use string interpolation to write a sentence.
    - OR we could return a string, with this integer interpolated ... let's do the string to challenge ourselves since our teacher showed us with an integer!


    ```
    func feedDog(amountOfFood : Int) -> String {
      // possibly some other code here...
      var timeToEat = amountOfFood * 3
      return "It took the dog \(timeToEat) minutes to finish the meal."
    }

    feedDog(amountOfFood : 3) // returns "It took the dog 9 minutes to finish the meal."
    feedDog(amountOfFood : 2) // returns "It took the dog 9 minutes to finish the meal."
    ```

#### Extension

* What is another argument that could be passed in your function? Try it out! Not sure what the syntax looks like? You got this. Remember, strong developers are strong googlers, so feel free to look for examples online.
* Can you have more than 1 return value? How do you know?

  Notes:
    - We could also pass in the dog's name, which would be interpolated into the return string!
    ```
    func feedDog(amountOfFood : Int, name : String ) -> String {
      // possibly some other code here...
      var timeToEat = amountOfFood * 3
      return "It took \(name) \(timeToEat) minutes to finish the meal."
    }

    feedDog(amountOfFood : 3, name : "Sodie") // "It took Sodie 9 minutes to finish the meal."
    ```
    - NO, you can have one and only one return value. If you try to separate two values with a comma, you get an error. If you write two return statements, the first one is read and the second is ignored. 

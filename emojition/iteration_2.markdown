# Iteration 2

This iteration of work will help set you up to complete the project. You will also get some great debugging practice (which hopefully by now you believe me it's a good thing to be good at🤓)

- Create another instance variable. This will be a dictionary with keys (the word version of each emoji) and values (an array of messages, one will be displayed to the user)

Sample:
```swift
let customMessages = [
     "ugly crying": ["cheer up buttercup", "take a deep breathe"],
     "happy": ["heck yeah!", "love that smile!"]
 ]
```

- Our next goal is to not just show the emotion to our user but _randomly_ pick `one` of those messages to them! That way, each time they click it, they will get a different message (to an extent; we can't have infinite messages... you get the point though).

- Inside your `showMessage` function, below the variable that stores the info that the user clicked on, we need another variable. Inside that, access and store the _word_ that represents the emoji that was clicked on. HINT: In the previous iteration, this is the code that was creating the `message` in the `alertController`.

- Now that you have that word (I called it `emotionText`), we need to access the array of messages that go with it. Create another variable (maybe called `messageArray`?) that will hold the array of messages for a specific emotion.

- 🛑 STOP and check yourself! 🛑
    * Write a print statement and print out the last variable you created.
    * THINK - _when_ do you expect to see this print statement appear?
    * Pick one button you will click on - _what_ do you expect to see printed out?

- What you just did above is a `debugging` technique - even though you may not have had a bug yet. It's a good practice to stop and check in every few minutes to make sure you have the data you think you have. In Swift, `print` statements are a tool for that.

- Now that we have this array, we need to randomly select _one_ message from it! Go get your google on and research how to generate a random number in Swift. Try to generate one and store it in a variable (right above your `alertController`). When you think you have it, check in with an instructor.

**Commit and push your code,** and then move on to [Iteration 3](./iteration_3.markdown)!

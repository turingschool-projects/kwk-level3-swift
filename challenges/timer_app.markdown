# Timer App

To create a timer app (detail below), you will need to use the [Timer Class](https://developer.apple.com/documentation/foundation/timer?changes=_3) and the [scheduledTimer() method](https://developer.apple.com/documentation/foundation/timer/1415941-scheduledtimer?changes=_3).

In your ViewController, create an instance variable that references an instance of `Timer`.

```swift
var timer = Timer()
```

You will also want an outlet that connects to a label on your StoryBoard. This label will hold a string with a number representing the time left. 

To start the timer, use the `scheduledTimer()` method. Reassign your `timer` instance variable to this function so it updates the whole application.

```swift
timer = Timer.scheduledTimer(timeInterval: 1, target: self, selector: #selector(ViewController.decreaseTimer), userInfo: nil, repeats: true)
```
You should have an error - `decreaseTimer()` is not a function - write one! Inside the code block, you need to decrease the time left (the variable that is an outlet).

To pause your timer, call the `invalidate()` function on the timer instance variable.

```swift
timer.invalidate()
```

Build a timer application that has the following functionality:
- Starts with a certain number of seconds (displayed)
- Counts down by second (every second is shown as the countdown is taking place)
- Has a start and stop button
- Can add or subtract X seconds from the current time left
- Has a reset button - when clicked, will start back at the number of seconds the app originally started with

Below is an example of what it _could_ look like. It is recommend that you use the `Navigation Bar` and `Tool Bar` as they are displayed in a way that iOS users are used to using. You can definitely still add in your own style!


![inline](../slide_images/timer.png)

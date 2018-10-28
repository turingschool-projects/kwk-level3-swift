# Iteration 3

## Where we left off
Your last challenge was to generate a random number. You have have something like this...

```swift
let randomNum = Int(arc4random_uniform(100))
```

... which is a great start! This will randomly generate a number between 1-100 each time the function runs. But WAIT, we don't have 100 messages in each array, and if we really think about it, each array might have a different number of messages in it.

### Keep Truckin' 🚚

- How can we get rid of that hard-coded `100` and make sure that we only generate numbers up until the number of elements in an array?

HINT: If you are getting a lot of red as you go - READ THOSE ERRORS! Most of them will have a `fix` option and it will just fix whatever you need fixed for you. Seriously. Stay calm.

- Now, instead of `emojitions[selectedEmotion!]` being your message, provide this a random message.

... are you stuck? Think back to how you access data from an array. What if you want the 1st item? 3rd? 5th? How can you use that random number to help you access a random element?

By the end of this, your app should look something like (but a lot better than 😜) this:

![inline](./3_emoji.gif)

Don't forget to commit and **push your code**!

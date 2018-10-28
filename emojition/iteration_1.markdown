# Iteration 1

By the end of this iteration, your app should have the following functionality:
  - When any emoji is clicked on, an alert will appear. The alert should inform the user of the emotion (in words) that the tapped-on emoji represents.

Sample:
![inline](./1_emoji.gif)

## Let's make it happen!

- Inside your class, create a instance variable (data type: dictionary) of emojis and the word that describes them. Example:

```swift
let emojis = ["😭": "ugly crying", "😁", "happy"]
```

- Right below that, create another constant that will store the information about _which_ button the user tapped.

```swift
let selectedEmotion = sender.titleLabel?.text
```

- Now, in your alertController, instead of hard-coding "message" or any other string, pull from your dictionary the _word_ that represents the emoji your user clicked on.

_HINT: Look back at that dictionary practice if you need to!_


## CHALLENGE:

- What if you wanted _two_ options on that alert - one that says "OK" and one that says "bye"? Make it happen. If you don't want both, delete the code afterwards. Practice if good for you😉

**Commit and push** your code, then move on to [Iteration 2](./iteration_2.markdown)!

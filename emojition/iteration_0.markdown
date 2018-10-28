# Iteration 0

By the end of this iteration, your app should:
  - have at least two buttons, each with an emoji
  - be completely styled (including constraints and home screen icon)

## Let's start this thing!

- Design the UI of you app on a wireframe page:
    * Decide which emojis you want to display for your user to pick from.
    * Decide on a color scheme (if you want the background of your buttons to have a color).
    * For now, this will _just be_ this one screen. When you make MVP, you can commit and push to GitHub, then decide if you have time if you have an idea for another screen.
    * Get your wireframe approved by an instructor.

- Create a new Xcode project. You do NOT need Core Data.

- Replicate your wireframes and make your StoryBoard scene look JUST like you dreamed of! ⚠️Do NOT create any actions yet⚠️

- **Run in simulator and make sure everything looks great!**

- **Create a Git and GitHub repository and push your code up!**

- Inside the `ViewController.swift` file, we will just add ONE function (now) and a couple of instance variables (later).

- This function is going to seem a little different from what you are used to. It will be an `@IBAction func ...` BUT you will not create the action like you normally do. This is because we have to set it up differently to get that alert box to show up.

- Write the skeleton of your function:

```swift
@IBAction func showMessage(sender: UIButton) {

}
```

- Now, let's add some pseudo-code so you can think through _what_ needs to happen in this function as well as keep organized.

```swift
@IBAction func showMessage(sender: UIButton) {

  // access the information from the send UIButton
  // so we know which emoji button was tapped

  // set up the alert using `alertController`

  // add an action to the alert so that the user
  // can go back to app when done reading it

  // present the alert
}
```

- Let's start accessing the information from the button. Just like we can grab the `.text` from a label hooked up to an outlet and `.image` from an image view, we can grab the `.titleLabel.text` from a UIButton. Let's store it in a variable since we will want to use it again:

```swift
let selectedEmotion = sender.titleLabel?.text
```

🛑STOP: Do not move on until you can explain where the variable `sender` came from, and what it sent. If you aren't sure, ask an instructor!🛑

- Now, let's set up the alert. Create a new constant (maybe called `alertController`? `alertManager`?) that is assigned to `UIAlertController()` - when you start typing, it will auto-populate. Select the option with the title, message, and preferredStyle parameters.

- We have an alert, but we need to give it an action so that the user can tap a button on it to make it go away when they are done reading. One the next line,

```swift
 alertController.addAction(UIAlertAction(title: "OK", style: UIAlertActionStyle.default, handler: nil))
```

⬆️ PLEASE NOTE: This worked for me because I used the constant name `alertController` from the step above.

- Last step for the code, let's use the `present` function to show our alert. You have used this in ViewFinder - go look up the syntax (it takes 3 arguments)!

- **Run in simulator and make sure everything looks great!** Nothing should be behaving differently than earlier - we haven't connected the UI to code.


## Get the StoryBoard and Code talking

We are so close!

- While you hold the `control` button down, click and drag from a button up to the little yellow circle at the top of your StoryBoard scene. When you release, you'll see a black box with options. Select `showMessageWithSender:` (or something close to that).

- Repeat for every button.

- **Run in simulator** - are you getting an alert on each button tap? Go back into your code and change the strings for title, message, and title (in `addAction`) to see what changes. If this all works, move on to [Iteration 1](./iteration_1.markdown).

- **Commit and push your code up to GitHub!**

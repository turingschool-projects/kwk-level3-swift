footer: KWK Swift/iOS: Actions & Outlets
slidenumbers: true

# Actions & Outlets

---

# Learning Goals

* Students will know how to create actions and outlets in Xcode
* Students will know the purpose of actions and outlets

---

# A slide

* Actions and Outlets are the way that our program lets the design files communicate with the code files. The connection allows us to refer to the objects in the design file, but inside of our code file.
* Outlet - when you want to change the appearance of something
* Actions - when you want the code to know that a user took an action


^ Have the students take note of the two - we will constantly be using these terms and having to decide whether a connection needs to be an action or an outlet.

---

# Setting up your work area

![inline](slide_images/storyboard.png)

^ Before you can start creating connections, your work space needs to be set up correctly.
Click on the small icon in the top right corner that has two intersecting circles - this will open the 'Assistant Editor'.

---

# Setting up your work area

![inline](slide_images/assistant-editor.png)

^ When you are in the 'Assistant Editor', you should see two panes in the Interface Builder - the storyboard on the left, the code on the right. (Sometimes it gets a little wonky and you have to change which is showing where - heads up)

---

# Outlet

Discuss: What information do we want to keep track of in this _really cool app_?

^ Have the students discuss - we want to get them to the idea of "we want to know what the user typed in, because anytime we type something into a form, that data has to go somewhere." Maybe that data logs us into an account, maybe it orders dinner, etc.
EXPLAIN: The goal of this really cool app is to have the user type something in the box, click submit, then they should see whatever they typed in appear as the app title.

---

# Establishing First Outlet

![inline](slide_images/outlet-giphy1.gif)

^ Press down the control button as you click the text field, then drag your mouse to the code, right in the first or second line of the class. A blue arrow should show what you are doing. When the little box pops up, you will need to type in a name - this will be a variable name that represents this data. You want to use something that describes the data.
We created this FIRST outlet so that we can control the text in this AppTitle Label. This means we can change it once we have whatever text the user typed in.
OPTIONAL MODEL: It may be more helpful for the students to see you do this a couple times, up to you.

---

# Establishing Second Outlet

![inline](slide_images/outlet-giphy2.gif)

^ We are creating this SECOND outlet to keep track of what the user types in. We will only do something with it once the user clicks "Submit"; however we have to set up the outlet from the get-go. That's why we drag outlets to the top of the class.

---

# Action

Discuss: What actions can our user take in this _really cool app_?

^ The main action here is clicking submit. Students may want to discuss the fact that typing in the text field is an action - it is. However, we don't want to create an ACTION for that user interaction because we want to wait until the user decides to tap submit until we take action.

---

# Establishing an Action

![inline](slide_images/action-giphy.gif)

^ Press down the control button as you click the submit button, then drag your mouse to the code, below the already written functions. A blue arrow should show what you are doing. When the little box appears, make sure to select "ACTION" in the drop down, then give it a name - this is a function so should follow naming conventions for functions. Under "Type" change "Any" to "UIButton".
OPTIONAL MODEL: It may be more helpful for the students to see you do this a couple times, up to you.

---

# Writing Code in the Action Function

```
@IBAction func submitButtonTapped(_ sender: UIButton) {
    if let newTitle = textField.text {
        appTitle.text = newTitle
    }
}
```

^ Let's talk about what is happening here.
FIRST - we have to unwrap the textField.text to make sure it is not nil.
We assign the textField.text value to a new constant called newTitle.
If we make it into that code block (if textField.text is not nil), then the appTitle.text is assigned to the newTitle.
Run in simulator - you should see it working!
Once explaining, have the students turn-and-talk about each outlet and action - what role did they play in making this app work?

---

footer: KWK Swift/iOS: Xcode & Swift Intro
slidenumbers: true

# Xcode & Swift Intro

---

# What is Swift?

* A programming language created by Apple

* Builds the front-end for macOS, iOS, tvOS, and watchOS applications

* Compiled language VS run-time

^ Swift builds the front-end, and these applications usually still have a backend in Ruby or Python, etc. just like web applications that have a front-end in JavaScript.
iOS and other OS applications can also be written in Objective C in Xcode; we will only focus on Swift here at KWK.
Swift is a compiled language, which means the whole application compiles and builds - if there are any errors, it simply won't build. A lot of developers prefer this over run-time languages (like Ruby and JavaScript) because even though it seems annoying seeing all the errors in your code, you don't have to waste time running the app, checking it in the browser or your terminal to find the error. It just won't run, and the error appears in your actual code! Examples on next slide:

---

# What does Swift look like?

![inline](slide_images/swift_language.png)

^ Swift has a lot of the keywords you've seen before, and some new ones. It uses curly braces and parenthesis. Syntax-wise, it looks more like JavaScript than Ruby. Camelcase is also a convention, just like in JS.
How are variables declared? `var` keyword
What do you think the `print` statements do (similar to `console.log` & `puts`)

---

# What are some of the big differences?

![inline](slide_images/arra_data_types.png)

^ While Swift looks a lot like JavaScript in ways, and also has a lot in common with Ruby (if statements, loops, variables, data types, etc), there are some major differences. We will go into the details as they come up in lessons, but just to give you a preview...
- This image shows an error we are getting because we tried to MIX data types in an array. You _can_ do it, but it is strongly discouraged, so you have to do some extra work to get around it.
- ALSO, notice this error message. This popped up in the code almost as soon as the code was typed. This is because Swift is **compiled**. It seems kind of annoying, but it's just trying to help you.
- FYI: If you see a red error - you must fix it. If you see a yellow warning - you probably want to check it out, but can still keep working and building your project.
- Last big difference - it's built for OS applications - as we get into building an app, you will see that Apple gives us so many tools to make our app really look and feel like it belongs on an iOS device!!

---

# What is Xcode?

* A software development tool created by Apple

* It is specifically for developers working on macOS, iOS, watchOS, and tvOS applications

* There are two main features - Playgrounds and Projects

---

# Playgrounds

* A safe place to play around with code and see what happens!
* Solve practice problems to learn the language
* Not for building projects

^ Model: Open up a playground (explicitly walk through every step of opening Xcode, selecting playground, giving it a name). Show the console drawer and emphasize the value shown on right-hand side at each line of code. Also show the top status bar (first place you want to work if you expect a change but aren't seeing it - most likely there will be a spinning wheel).

---

# Playgrounds Lab

Take ten minutes to practice creating a new playground, then:

* Create three variables - your name, age, and favorite thing to do during the summer
* Print to the console a sentence that uses all three of your variables

---

# Projects

* A place for building entire iOS projects
* A lot more than writing code goes into building an iOS app, but we do it all in Xcode!
* A LOT of tools - we will take it one step at a time

^ MODEL: Open up a new project, walk through every step of setup. Show each pane (see one pager) and the buttons to expand/collapse panes. Show file tree and point out storyboard. Model resizing and moving the storyboard. Show simulator, build status bar, and different device views. Add a couple UI Elements and run simulator. Change colors/fonts, then re-run.

---

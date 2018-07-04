footer: KWK Swift/iOS: Segues
slidenumbers: true

# Segues

---

# Learning Goals

* Students will understand why segues are a building block for iOS development
* Students will be able to create segues between views
* Students will practice reading a blog post to learn a new skill!

^ This lesson will feel more like a lab. You will will be given guidance on how to read a blog post, implement the skills taught in it, then reflect on what you've learned. This is something that software engineers do almost DAILY! Many time, engineers are asked to used technologies they don't know anything about - their company doesn't send them back to school; they expect them to use their resources to learn on the job. We've talked about our 'Googling' skills - this is the next level. Using the plethora of information out there to learn and implement technologies!

---

# Vocabulary

* Segues
* UX (User Experience)

^
---

# Different Views in an App

* Pick a driver and a note-taker
* When I say go ...
  - You will have exactly ONE minute to open up an iPad or iPhone app
  - The driver will tap around as much as possible
  - The note-taker will tally every time the app showed a completely different view

^ This is a warm up activity to get them to appreciate just how essential segues are in iOS apps. Feel free to make this dramatic as you'd like! After the timer is up, have each group share out. Discuss: What is the app you were on didn't have the capability to have different views? What was the transition like between views? (usually smooth, a page slide over, etc.)
---

# Segues

* Transitions for one view to another
* Have a smooth animation for a good UX

^ Those transitions - from view to view - are called Segues. We have created one with the navigation controller already, but that only works with the nav items. We also want to be able to show the user a different view when they click a part of the screen. For our project, we want the user to be able to click on a row in the table view, and be taken to a 'Photo Detail Page' where they can view the photo and caption at a larger scale.

---

# First Read

* Read and take notes (no following along, yet!)
  - Any words/terms you don't understand?
  - Do you feel like you have the tools to follow along in Xcode next time you read it?
  - In your own words, what is a segue?
  - List the basic steps (don't need details) of how to create a segue.

^ On the first read through of this blog, I'm going to ask you to ONLY read and take notes. The reason for this is: sometimes the title of a blog won't give the most accurate information, and halfway through reading it, a software engineer realizes it's not the thing they are looking for. The first read allows you to make sure this is the right thing, and that we have the tools/knowledge to start at this point (sometimes we need to learn some of the stepping stones first). Please do this independently!

---

# First Read Debrief

* From your first read through the blog:
  - Any words/terms you don't understand?
  - Do you feel like you have the tools to follow along in Xcode next time you read it?
  - In your own words, what is a segue?
  - List the basic steps (don't need details) of how to create a segue.

^ Open up a discussion, take note of terms students wanted to clarify (you may want to pull the blog up on the screen to read in the sentence/use context clues).
Do you have the tools?  They have Xcode, they know how to use the Object Library, ctrl + click to drag, etc. YES, we have the tools!
Basic Steps: project in Xcode, drag on another view, button to click on 1st view, ctrl + click and drag from that button to the other view, select "show".

---

# Second Read

* Now that we know this blog gives us the info we want and is on our level, we can go through the tutorial to practice!
* Open up a new Xcode project and follow along!

^ I would recommend doing this solo so each student has the practice. Instructors should be circulating to check in on how they are doing. When questions come up, really try to refer them to the blog to answer the questions for themselves rather than relying on you!

---

# Second Read Debrief

* What challenges came up in completing this?
* Did reading it one time through first seem to help? Why or why not?

^ Debrief in pairs or whole class - this is just to get them to reflect on their learning experience - bring it back to: THIS IS WHAT SOFTWARE ENGINEERS DO EVERY DAY! And you just did it! Being pushed out of your comfort zone is essential in learning, so if it felt challenging at times, that is ok and actually good!

---

# Segue Model

* Let's make 100% we all feel confident in creating segues and do one class example.


^ A couple idea on how you can lead this:
Instructor Models creating the segue to reinforce and make sure 100% students saw it. Ask a lot of CFUs as you go, or cold call and ask students what you should do next, etc.
Students plugs in their computer and shows the class (starting a new project).

---

# Build Photo Detail View

* Time to implement into our ViewFinder project!
* Some other steps will be involved

^ Release students to work on Build Photo Detail View Lab - let them know the segues are a _part_ of it; they can refer back to the blog post or their practice work as references!

---

footer: KWK Swift/iOS: Side Loading iPads
slidenumbers: true

# Side Loading iPads

---

# Learning Goals

* Students will side load iPads so they can see their app on a device throughout development

---

# Technical Vocabulary

* SideLoading
* Device

---

# Setup

* Plug your iPad into computer
* Open your project in Xcode
1. In the Navigator Pane, click on the root of the Project
2. Then click on the Project Name under TARGETS
3. Last, in the Interface Builder Pane, make sure you are on the 'General' Tab

---

# Setup

![inline](slide_images/side_loading_xcode_setup.png)


---

# Identity

1. Make sure your project name is typed in for 'Display Name'
2. For the 'Bundle Identifier' field, com.yourName.projectName

---

# Identity

![inline](slide_images/side_loading_xcode_identity.png)

---

# Signing

1. Click 'Add an Account'
2. Type in your iCloud credentials
3. Exit that window once you see your information
4. Back in the Interface Builder pane, select the team you just added

---

# Signing

![inline](slide_images/side_loading_xcode_signing.png)

---

# Run Application on iPad

1. Make sure the iPad is unlocked
2. Change the device to your physical iPad
3. Run application by clicking the play button or `cmd + r`

---

# Run Application on iPad

![inline](slide_images/side_loading_xcode_change_device.png)

---

# Run Application on iPad

![inline](slide_images/side_loading_xcode_select_device.png)

---

# Run Application on iPad

![inline](slide_images/side_loading_xcode_run_app.png)

---

# It might ask for a keychain password...

* Build fails - exit 1 signal 0
* Try to type in computer password
* If that doesn't work, click 'Deny'

---

# It should fail

![inline](slide_images/side_loading_ipad_untrusted_dev.jpg)

---

# How to solve that problem

* iPad Settings
* General
* Profiles & Device Management
* Click your email, click 'Trust' button to approve the application

---

# Run Application on iPad

* If your app is not running on your device in a minute or so, get help from a group nearby or your instructor

---

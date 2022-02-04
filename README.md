# Magic-8Ball-Swift 5.3

---
title: "Intro to Magic 8-Ball"
slug: intro-magic8
---

Welcome to the first of the Make School's iOS app tutorials series! This tutorial introduces you to the basics of building iOS apps by building your first app: a Magic 8-Ball!

## What's A Magic 8-Ball?
If you're not familiar with the Magic 8-Ball, it's an 8-Ball with _mysterious_ fortune-telling powers. You can use it by asking simple yes or no questions and shaking the 8-ball for an answer.

![Magic 8-Ball](assets/magic_8_ball.png)

For example:

Q: Will _insert your name here_ become an iOS developer?

_shakes 8-ball_

![Magic 8-Ball Answer](assets/signs_point.jpg)

Pretty useful huh? When you're finished with the tutorial, you'll be able to use your new Magic 8-Ball app to make all of life's important decisions!

## Who Is This For?

Beginners (little to no previous iOS experience) who want to get started by building their first iOS app.

## What You Should Already Know

Beginners are expected to have a basic understanding of the Swift programming language. If you haven't been introduced to Swift yet, or even need a refresher, it's recommend to check out Make School's _Getting Started With Swift_ tutorial first.

## Estimated Completion Time:

1 hour

# What We're Building

We'll start our journey into iOS by building a simple Magic 8-Ball app.

![Finished App Flow](assets/finished_app_flow.png)

You can see the app's flow in the designs above.

1. The user will open the app from our app icon.
2. The user is then presented with a prompt to think of a question to ask the Magic 8-Ball.
3. Finally, the user can either tap the **Shake It!** button or rage-shake their phone for an answer.

## What You'll Learn

By the end of this tutorial, you will:

- Create a new Xcode project
- Add an app icon to your app
- Navigate and become familiar with Xcode
- Build a really, **really** simple UI
- Write code that randomly generates an answer

# Important: Read Me!

Now that I have your attention...

To succeed as an iOS developer and build awesome apps, you'll need to know more than just code. This tutorial will introduce new topics like _getting to know Xcode_ and _creating UI with Interface Builder_, many which don't involve writing code. This might seem irrelevant at first, however you won't be able to build iOS apps without learning about these subjects first.

As you go through the tutorial, pay attention when learning to use Xcode. Xcode will be your bread and butter. The more fluent you are with it, the easier it'll be to build beautiful, well-executed apps.

Most importantly, relax and have some fun with it. Building iOS apps is challenging, but also extremely rewarding. There's no feeling like watching your own apps come to life and feeling the pride from knowing you built it yourself!

## If You Get Stuck

> "Sometimes, magic is just someone spending more time on something than anyone else might reasonably expect."
>
> \- Teller (Penn & Teller)

Getting stuck when coding (and debugging) is a natural part of the development process. If you find yourself stuck on a problem or lost, pause for a moment and take a breath. Maybe take a walk. Then retrace your steps (in the tutorial, not the walk). Make sure you've follow each step of the tutorial. It's easy to make typos or to accidentally skip over important steps.

If you want to compare your code to the solution, you can find it [here](https://github.com/MakeSchool-Tutorials/Magic-8Ball-Swift4-Solution).

---
title: "Creating Your First Xcode Project"
slug: new-xcode-project
---

Most of this tutorial will be devoted towards learning about Xcode. In this section, we'll have our first introduction to Xcode and go through the process of creating a new Xcode project for our app.

## What is Xcode?

Xcode is an _Integrated Development Environment_ (IDE) for developing apps in the Apple ecosystem. We'll be focusing on iOS apps, but you can also make apps for macOS, watchOS, and tvOS apps. IDEs (like Xcode) contain and integrate many powerful tools that make software development easier for programmers.

As you learn to build apps in Xcode, you'll use many of these tools. Tools that you'll use commonly on a daily basis might include:

- **Source Code Editor:** write and edit code
- **Interface Builder:** build and visualize user interfaces (UI) without code
- **Debugger:** test, catch and debug problems in your code
- **Compiler:** helps you find mistakes in your code and offers "Fix-its" suggestions
- **Assistant Editor:** edit multiple files in Xcode side-by-side
- **Simulator:** test and run your app on a simulated iPhone on your computer

We'll go through each of these tools more in-depth as we build our Magic 8-Ball.

> [info]
Remember, Xcode contains many more tools that the ones listed above. In this tutorial, we limit our focus to learn about only the most important Xcode tools for building simple iOS apps.

# Your First Xcode Project

Firsts are always special. Now that we know a little more about Xcode, we'll begin by creating our _first_ Xcode project.

Get familiar with this process! You'll repeat it over and over whenever you start a new app.

> [action]
Create a new Xcode project:
>
1. Open _Xcode_ on your computer. You should see the following launch window after you open Xcode ![Launch Window](assets/xcode_launch_window.png)
1. Next, from the launch window's quick options click `Create a new Xcode project` ![Create New Project](assets/create_new_project.png)
1. You should see the following prompt to select a template for your new project. Under _iOS_, select _Single View App_ ![Select Template](assets/select_template.png)
1. With your selected template, click _Next_. You should see a new prompt for your project details ![Set Project Details](assets/set_project_details.png)

In this new prompt, we'll set some basic info and details that Xcode needs to create a new project.

> [action]
In the project details prompt, enter the following information:
>
![Filled Project Details](assets/filled_project_details.png)
>
If you need a step-by-step breakdown:
>
1. In the _Product Name_ field, enter `MagicEightBall`. This is what Xcode will name your project in your file directory. To prevent potential name-related problems, it's best to stick with alphanumeric characters (letters and numbers) and avoid special characters.
1. In the _Team_ dropdown menu, set it as `None`. If you already have an `Apple Developer Team`, you can select that instead.
1. In the _Organization Name_, you can enter one of the following: your name, your fake company name, or _Make School_.
1. In the _Organization Identifier_, set it as _com.makeschool_. If you own a domain name, you can set this field as your reverse domain name. For example, if you own the domain name _happycarrot.com_, you would put _com.happycarrot_ as your identifier.
1. The _Bundle Identifier_ will be automatically generated from your _Organization Identifier_ and _Product Name_. Apple uses the bundle identifier to uniquely identify each app in the _App Store_.
1. In the _Language_ dropdown menu, make sure it's set to `Swift`.
1. Finally, leave all three checkboxes unchecked. We won't use _Core Data_ or testing in this tutorial. Those are more advanced topics we'll cover at another time.

<!-- break -->

> [action]
To finish up and create our new project:
>
1. After filling out your project details above, click _Next_. ![Project Details Next](assets/project_details_next.png)
1. Xcode will now prompt you to select where you'd like to store your project. Using the file navigator, choose to a place on your computer to store your project. If you don't have a place in mind, you can use your `Documents` folder. ![Select Project Location](assets/select_project_location.png)
1. Make sure you keep the _Source Control_ checkbox selected for _Create Git repository on my Mac_. ![Enabled Source Control](assets/check_source_control.png)
1. After you've selected a project location and verified that the _Source Control_ checkbox is selected, click the `Create` button. ![Create Project](assets/create_project.png)

Congrats! Meet your first new project. You should see the following:

![Newly Created Project](assets/just_created_project.png)

Can you feel the sparks? I think this is the start of something special.

# Getting To Know Xcode

As we build our Magic 8-Ball app, we'll learn about Xcode and how to harness it's power. Before moving onto the next section, we'll go over a brief overview for each of the main areas of Xcode and how to run our newly created app in the simulator.

Picking up where we left off, you should see something similar to the following:

![Newly Created Project](assets/just_created_project.png)

Woah! At first glance, you'll notice there's a lot going on. Tabs, buttons, panels and text fields everywhere!

If you feel overwhelmed, take a deep breath. We'll walk through this together.

## Xcode Main Areas

Xcode is broken down 4 main areas + a toolbar:

![Xcode Areas](assets/xcode_areas.png)

Here's a quick breakdown of each of the areas above:

1. **Toolbar (Green):** displays key information about project, expand/collapse other areas, run project
1. **Navigator (Orange):** find files, search in your project, manage source control, navigate errors
1. **Editor Area (Red):** write code, build UI with storyboard, change project settings
1. **Utilities (Purple):** gives info about files, set properties of items in Interface Builder
1. **Debug Area (Blue):** test and debug your code at runtime

Each area has many more tools and features built-in, so don't think of the summary above as a comprehensive list. We've just highlighted the key functions of each part of Xcode.

## The Toolbar

The Xcode toolbar provides easy access to information and buttons that you'll use often. You can see it at the very top of your Xcode IDE: ![Xcode Toolbar](assets/xcode_toolbar.png)

Let's go over some of the most important parts of the toolbar and figure out how to run our app.

## Xcode Status Bar

In the center of the toolbar, you'll see the Xcode status bar:

![Status Bar](assets/toolbar_status_bar.png)

The status bar provides helpful information about your project. It'll change and update as you use Xcode.

For example, if Xcode finds warnings or errors when it _builds_ (more on this soon) your project, it'll display it in the status bar. You can see this below:

![Status Bar Errors](assets/status_bar_errors.png)

Notice the yellow warning icon and the red error icon on the right side of the status bar.

## Showing / Hiding Xcode Areas

You can also hide and display the _Navigator_, _Debugger_ and _Utilities_ based on which tools you're using at the moment. This can be done by toggling the 3 buttons shown below:

![Display Xcode Areas](assets/display_xcode_areas.png)

If your computer doesn't have a large screen, it's often helpful to hide these areas when you're not using them so you can focus on the areas you are using. We'll see this in action later in the tutorial.

# Running Our App

Let's go through the process of running our app on the simulator.

> [info]
We're specifically using the iPhone 8 simulator for convenience right now. In the future, you can use any simulator of your choice or even your own device.

Take a look at the group of buttons on the left-hand side. You should see:

![Toolbar Run Group](assets/toolbar_run_group.png)

These buttons and controls allow you to _build_ and run your app on either a simulator or your iPhone.

> [info]
**What is the build process?**
>
The build process, also referred to as building, is the series of tasks that must be completed in order to turn your code into an app that can be run on a device (or simulator).
>
One of these tasks is _compiling_ your code. This means that the compiler turns your Swift code into machine-code (instructions that your computers can read). During this process, the compiler may find errors with your code. If it does, the build process will fail and Xcode will display the errors in the status bar as shown previously.

## Scheme Dropdown

![Scheme Dropdown](assets/toolbar_scheme_dropdown.png)

The _Scheme_ dropdown menu will allow you to edit and manage multiple _schemes_. A _scheme_ tells Xcode **what** to build and run when you press the _Run_ button. As a beginner, you don't need to worry about dealing with multiple schemes.

The second half of the scheme dropdown allows you to specific a simulator or device that you want your selected scheme to run on. For us, we want to run our app on an _iPhone 8_ simulator.

Click on the right-side of the _Scheme_ dropdown to see a full list of options. If you connect your iPhone to your computer, you'll see your device show up as an option as well.

![Scheme Dropdown](assets/toolbar_scheme_dropdown_open.png)

Let's change the device our scheme will run on.

> [action]
Change your scheme to build and run on the _iPhone 8_ simulator. Click on the second half of the scheme dropdown menu and select _iPhone 8_ simulator.
>
![Select iPhone 8 Scheme](assets/iphone_8_scheme.png)

With our simulator set, we can move on to build and run our project.

## Run Button

![Run Button](assets/toolbar_run_btn.png)

If you haven't guessed already, the _Run_ button will build and run your active scheme on the selected device. Since we selected the _iPhone 8_ simulator in the previous step, our app will run on the iPhone 8 simulator.

> [action]
Click the _Run_ button now and watch Xcode build and run your empty project. In the future, you can also use the keyboard shortcut command-r (`⌘R`) to run your project.

<!-- break -->

> [info]
The first time you run your app, you may see a dialog that asks for your password: ![Debug Permission](assets/debug_dialog.png)
>
Enter and click `Continue`. This permission is necessary to run your app using the _debugger_ (more on this later).

If all goes well, you'll see a simulator with your app launch:

![Empty Simulator](assets/empty_simulator.png)

If you're wondering why there's just a blank white screen, it's because we haven't added anything to our app yet. As we develop our app, we'll see the changes and functionality appear when we run our app.

## Stop Button

![Stop Button](assets/toolbar_stop_btn.png)

The _Stop_ button (looks like a square) will stop the instance of your app if it's currently running.

> [action]
Click the _Stop_ button to terminate the running instance of your app on the simulator. For future reference, the keyboard shortcut command-. `⌘.` will stop your app.

You'll see that the simulator will stop running your app.

## Progress So Far

At this point, you've created your first Xcode project and run the empty new project in the simulator. As we move forward, we'll keep running our app on the simulator to check that our project is working as expected.

Next, let's we'll learn about the _Project Navigator_, the different type of files in Xcode and how to add an app icon to our project!

---
title: "Navigating Xcode"
slug: navigating-xcode
---

Let's take a look around our newly created Xcode project. All of the files and settings in our current Xcode project are the default configurations when a project is created from the _Single View App_ template.

To see what's in our project and navigate file to file, we'll need to using the _Navigator_.

## Navigator

![Xcode Navigator](assets/navigator_pane.png)

The navigator pane contains multiple tabs (call navigator) for many different tools in Xcode.

You can change tabs by clicking on the different icons at the very top of the navigator pane.

![Navigator Top Tabs](assets/navigator_tabs.png)

Each of these navigator tabs are useful tools that you'll eventually learn to use. Some of the most important ones are:

- _Project navigator (folder icon)_: navigate and change files
- _Find navigator (magnifying glass icon)_: search through your project to find files
- _Issue navigator (warning sign icon)_: locate and fix warnings and errors in your project

In this tutorial, we'll only focus on the first tab, the _Project navigator_, but you'll learn about all of them eventually.

<!-- include issues navigator? -->

## Project Navigator

The project navigator helps you navigate and organize your project files. In other words, it makes it easier to find and open different files in the same project.

> [action]
In your Navigator pane, make sure you have the project navigator tab active. If you don't, click on the first navigator tab. It has an icon that looks like a folder. ![Project Navigator Tab](assets/project_navigator_tab.png)

With your Project navigator tab active, you should see your project's files right below the Navigator tabs:

![Project Navigator Active](assets/project_navigator_active.png)

Let's look at some of the different files in our project.

# Xcode Project File

> [action]
In the navigator, select the Xcode project file at the very top of the project navigator. You should see the following:
>
![Xcode Project Details](assets/xcode_project_details.png)

<!-- break -->

> [info]
You'll notice, whenever you choose a file in the _Project navigator_, the _Editor area_ will update with the corresponding file. In addition, the _Utilities area_ will also change to match the options available for the active file. Switch back and forth between a couple files if you want to test it out (using a single click NOT double click).

In the project details, you can configure your app's settings. For example, let's go through the process of changing the app's name that is displayed on the home screen of a user's iPhone.

> [action]
To get a better idea of what we're changing, run the app on the iPhone 7 simulator. You'll see the blank white screen as you saw earlier.
>
Next, press command-shift-h (`⇧⌘H`). This will take you to the home screen of your iPhone 7 simulator.
>
![Home App Display](assets/home_app_display.png)

As you can see above, the app icon is the default blank app icon that comes with new projects. In addition, our project name is by default the product name that we set when creating the project. We'll eventually change both, but first let's change the app's _Display Name_.

Back in Xcode, we can change the app's display name by editing the _Display Name_ field in our project details. Make sure the Xcode project file is active in your Project navigator.

> [action]
Set the app's display name from the default `MagicEightBall` to `Magic 8-Ball`.
>
![Edit Display Name](assets/edit_display_name.png)

Done! That was easy.

Before getting to changing the app's icon, let's take a look at some other types of files.

# Swift Source Files

In your Project navigator, select the file nested under your Xcode project file named `AppDelegate.swift`.

![App Delegate Active](assets/app_delegate_active.png)

Files with the `.swift` extension are Swift source files. The code you write will be in Swift source files.

The _App Delegate_ is an important object that is responsible for handling your app lifecycle. If you look at the some of the method names in the file, you'll see names like:

- `application(_:didFinishLaunchingWithOptions:)`
- `applicationWillResignActive(_:)`
- `applicationWillTerminate(_:)`

As you can guess, all of these methods happen when your app changes _state_ such as when your app first launches, when it's put into the background, or when it's terminated. Although we won't add anything in here for this tutorial, you can add code here to customize your app behavior when important app lifecycle events happen.

# Asset Catalog

Now, let's get back to changing our app icon.

> [action]
From the Project navigator, select the `Assets.xcassets` file. Within the editor area, you'll see a single asset placeholder named _AppIcon_. Normally, you'll see a list of all your app's assets in the _Asset Catalog_.
>
In your Asset Catalog, select the empty _AppIcon_ placeholder asset. You will see a bunch of empty placeholders for your app icon in multiple different sizes and devices.
>
![App Icon Asset Empty](assets/app_icon_asset_empty.png)

If you're wondering why there are so many empty app icon placeholders, it's to support different resolutions and sizes of different devices.

For our Magic 8-Ball app, we'll only add the app icon images to be displayed on the home screen. When you're really submitting your app to the App Store, you'll need to make sure to account for all the relevant app icon sizes.

> [action]
Go ahead and download the Magic 8-Ball app icon images by [clicking here](https://github.com/MakeSchool-Tutorials/Magic-8Ball-Swift4/raw/master/magic_app_icon.zip). After downloading and unzipping your image assets, drag and drop the `app_icon@2x.png` into `iPhone App iOS 7-14 60pt 2x` empty placeholder. Repeat and do the same for `app_icon@3x.png` with `iPhone App iOS 7-14 60pt 3x`.

When you're finished, your _AppIcon_ image set should look like the following:

![App Icon Set](assets/app_icon_set.png)

You've successfully added a custom app icon to your Magic 8-Ball app!

> [info]
After adding your Magic 8-Ball app icon, you'll notice some new warnings appear. These appear because our Xcode project is expecting additional version of our app icon for the App Store and the iPad device. It's ok to ignore these warnings for this tutorial.

# Testing Our Changes

To make sure our changes have worked, let's run the app. Remember, we haven't changed what the app does, so when we run the app it'll still be a blank, empty white screen.

> [action]
Run the app by pressing the Run button in the toolbar or the `⌘R` shortcut. With the app active in the simulator, press command-shift-h (`⇧⌘H`). You should see the simulator return to the iPhone home screen with your new app icon and display name!
>
![Home Screen Styled](assets/home_screen_styled.png)

---
title: "Adding UI"
slug: adding-ui
---

Up to this point, we haven't done anything that changes what our app will do when it's run. As we can see from running our app in the simulator, it's still just an empty, blank white screen.

In this section, we'll build the UI for our Magic 8-Ball.

> [info]
**What is UI?**
>
User interface, commonly referred to as UI, are any elements that your app will display on screen to a user. This includes visual elements like text and images as well as interactive elements like buttons, sliders and tabs. In programming, it's also common to refer to UI as your _views_.

## Introducing View Controllers

If you're planning to build iOS apps, you'll need to learn about the `UIViewController`. View controllers are one of the fundamental building blocks of iOS development.

The `UIViewController` is a class that is responsible for _controlling_ its set of _views_. Each view controller has a root view that acts as a canvas to place other subviews.

<!-- can consider adding jump to definition here for UIViewController view property -->

![Root View Highlighted](assets/root_view_highlighted.png)

As you can see above, both the text label and button are subviews placed on top of the view controller's root view.

As a beginner, you can think of each screen of your app as a view controller. All buttons, text, images are _subviews_ that the corresponding view controller object controls. If the user taps a button, the view controller will be responsible for what happens.

> [info]
Although we'll only use a single view controller in this tutorial, you can have any number of view controllers in your app.

Next, let's build our UI in the default view controller that comes with every _Single View App_ Xcode template.

# Adding UI in Storyboard

First we'll need to open our storyboard file.


In your Project navigator, select the `Main.storyboard` file. You'll see your editor area change to the following:

![Main Storyboard Overview](assets/main_storyboard_overview.png)

Each of the highlighted areas is important to building your UI in your Main storyboard file:

- Document Outline (Orange): displays a vertical view hierarchy of your storyboard file
- Interface Builder (Blue): displays a visual representation of what your UI will look like
- Utilities Area (Purple): configure properties, size, and other details of your storyboard elements
- Object Library (Pink): displays a list of all Apple's pre-built UI components you can use in storyboard

If you can't see your object library, click on the `+` button on top of your __Utilities Area__. However, I personally prefer using a shortcut to show your object library: `command` + `shift` + `L`

Now let's add our Magic 8-Ball _Shake It!_ button to our view controller.


![ms-video](https://media.giphy.com/media/GALfhv4hqQekPqJuyz/giphy.gif)
>
Find the `Button` object in the _Object Library_ and drag and drop it onto the root view of your view controller.

Next, let's learn more about the _Utilities area_ so we can configure our button to have the right title text.

# Utilities Area

Just like the _Navigator_, the _Utilities_ pane has multiple different tabs at the top called inspectors.

![Utilities Inspector Tabs](assets/utilities_tabs.png)

The tabs are contextual based on what is actively selected. That means that the tabs in the _Utilities area_ will change based on whatever you last clicked in Xcode.

Each inspectors allows you to configure different details and attributes about the selected item.

## Attributes Inspector

First we'll look at the _Attributes Inspector_ which changes the attributes of a selected storyboard object. We can use this to change the title of our button.

> [action]
>
1. Make sure you click on the button and that it's actively selected. Remember the _Utilities_ pane is contextual so it will change based on what is selected. ![Select Button](assets/select_button.png)
1. Next, navigate to the _Attributes Inspector_ tab in the _Utilities area_. It is the 5th icon from the left. ![Open Attributes Inspector](assets/attributes_inspector.png)
1. Last, find the title field and change it from the default text `Button` to `Shake It!`. ![Set Button Title](assets/set_btn_title.png)

You should now see a squished button with the `Shake It!` title.

![Squished Button](assets/squished_button.png)

We'll fix this next using the _Size Inspector_.

## Size Inspector

Right now our shake button is squished because the new title text is longer than the width of the button. To fix that we'll change the _frame_ of the button.

The _frame_ of an object refers to a object's X and Y position and it's size (height and width).

We can view our current skip button's frame in the _Size Inspector_.

> [action]
First, navigate to the _Size Inspector_ in the utilities area. ![Size Inspector Active](assets/size_inspector_active.png)
>
You can view and edit the current frame of the selected storyboard object under it's _View_ section. ![Size Inspector View Section](assets/size_inspector_view_section.png)

A simpler, but less precise way of changing our button's frame is by selecting it your cursor and dragging. You can drag the center of the object to move as well as the corners of it's bounds to resize it.

The positioning doesn't have to be perfect, but if you want to be more precise you can use the _Size Inspector_.

> [info]
In this tutorial, we'll be setting a pre-defined frame for each of our subviews. That means that if the user is using a simulator or iPhone with a different screen size, our UI will be incorrectly sized.
>
This is ok _for now_. This tutorial is more focused on making sure you get a lay of the land with Xcode and iOS development. In the next Tip Calculator tutorial, you'll learn about using tools like auto-layout and stack views to create dynamically re-sizable views.

# Adding a Label

To complete our UI, we'll also need to add a label to display the Magic 8-Ball's answers.


From the _Object Library_ find the label and drag it onto center of the view controller's root view.

![ms-video](https://media.giphy.com/media/WlNdGiLCUwwjyblTG0/giphy.gif)

Next, we'll change the size and attributes of our label.

> [action]
>
1. Select the label and open the _Attributes Inspector_ in the _Utilities area_. ![Label Attributes](assets/label_attributes.png)
1. Change the `Text` attribute from the default `Label` placeholder to `Have a question?`. This will be the new default text that the app starts with every time the app is opened. ![Change Label Text](assets/change_label_text.png)
1. Resize the label so that it fits the new text. ![Resize Label](assets/resize_label.png)
1. In the _Attributes Inspector_ change the text alignment to _Center_. ![Change Text Alignment](assets/change_text_alignment.png)
1. Last, change the _Font_ attribute from `System 17.0` to `System Bold 28.0`. ![Change Font](assets/change_font_attribute.png)

We've just finished setting up the UI for our app. Let's take a second to build and run to see our progress.

> [action]
Build and run your app on the iPhone 8 simulator. You'll see the following:
>
![Storyboard UI Finished](assets/storyboard_ui_finished.png)

We've laid out our UI using Interface Builder. Next, we'll look at connecting our views to our Swift source files. As you might imagine, without connecting our storyboard objects to code, our app won't be able do much.

---
title: "Connecting Code"
slug: connecting-code
---

In this section, we'll take a look at how our storyboard connects to code. When you run the app now, you'll notice that when we click _shake button_ in the simulator, nothing happens.

That's because our app won't do anything if we don't write any code. You can think of the code you write as instructions that tell the app what to do when a user is using it. When there aren't any instructions, the app won't do anything.

In the example of responding to a button tap, we'll need to write code to tell the app what to do when a user taps the _shake button_.

## How Is It Connected?

One of the most biggest sticking points for beginners is understanding how your code is connected to storyboard. Xcode connects your storyboard to Swift code by using a combination of the _Identity Inspector_, _IBOutlets_ and _IBActions_.

In order to see this, we'll first need to hold `option` and `click` the ViewController.swift file

On the right side of your addressbar, there is a button you can click to activate the _Assistant Editor_. 

![Assistant Editor Active](assets/assistant_editor_active.png)

The first thing you might notice, is the lack of screen space for each open file. We can make this better by hiding unneeded Xcode tools like the _Navigator_. You can do this by using the second group of buttons on the far right-side of the toolbar.

![Display Xcode Areas](assets/display_xcode_areas.png)

You can use these buttons to toggle between hiding and displaying the _Navigator_, _Debugger_ and _Utilities_ areas. Let's go ahead and close the _Navigator area_ for a little more screen real-estate.

> 
Close the _Navigator_ pane by clicking on the first of the buttons. Keep the _Utilities area_ open as we'll need it soon.
>
![ms-video](https://media.giphy.com/media/etOEk0khLu5m4jh5JM/giphy.gif)

Now that we know how to display two different files side-by-side, we'll look at how Xcode knows to connect our storyboard view controller to our `ViewController.swift` source file.

# Identity Inspector

> [action]
1. In the _Document Outline_ in your storyboard, select the _View Controller_ storyboard object. ![Document Outline](assets/document_outline_select_vc.png)
2. Next, open the _Identity Inspector_ in the _Utilities area_. ![Identity Inspector Active](assets/identity_inspector_active.png)

In the _Identity Inspector_, you should see a section that specifies currently selected storyboard view controller's custom class.

![Custom Class Section](assets/custom_class_section.png)

Looking at both the `ViewController.swift` file and the _Identity Inspector_, you'll notice that the _Class_ name matches. This is how you can set and define custom behavior for your storyboard object.

![Connected Class](assets/connected_class.png)

> [info]
We don't need to set this up for this project because the _Single View App_ template had this pre-configured for us. For future projects, you'll need to configure each custom view controller's class in the _Identity Inspector_ to connect storyboard view controllers to their respective Swift source file.

# IBOutlets

In our storyboard view controller, we previously added a label and a button. To implement our logic (the instructions for our Magic 8-Ball), we need some way to reference our label and button.

To solve this problem, we'll need to create _IBOutlets_.

_IBOutlets_ create a connection from our storyboard subview objects (like labels, buttons, image views) to our Swift code. The allow us to reference that we can manipulate programmatically.

> [action]
First to create some more screen space, let's close the _Utilities_ pane using the toolbar. Your Xcode IDE should look like the following:
>
![Assistant Editor Active](assets/assistant_editor_active.png)

With our `Main.storyboard` and `ViewController.swift` files open side by side, let's create our first IBOutlet.

> [action]
Create an IBOutlet for your answer label.
>
Select the answer label in _Interface Builder_. Next hold down control (`⌃`) and click-drag from your storyboard label into your `ViewController.swift` file. In the resulting prompt, name your new IBOutlet `answerLabel`. ![ms-video](https://media4.giphy.com/media/WQ8Zr2OLmqhSCeV1OM/giphy.gif?cid=790b76113c1358aeda566d4a59d7d8b0b2e9e7e4f0818cf1&rid=giphy.gif&ct=g)

Repeat the same process for the _shake button_.

> [challenge]
Create a new IBOutlet called `shakeButton` for your storyboard button in your `ViewController.swift` file.

<!-- break -->

> [solution]
Select the shake button in _Interface Builder_. Then hold down the control button (`⌃`) and click-drag from the storyboard button into your `ViewController.swift` file. Name your new IBOutlet `shakeButton`.
>
![ms-video](assets/button_iboutlet.mov)

We've created both IBOutlets so that we can reference and access our label and button in our `ViewController.swift` file.

Next, we'll look at responding when a user taps the _shake button_ using a IBAction.

# IBAction

An IBAction is a method that is called when the user interacts with a UI object. Creating an IBAction is very similar to creating an IBOutlet.

Let's create an IBAction for when a user taps on the _shake button_.

> [action]
Create a IBAction from your _shake button_ in your view controller source file: ![ms-video](https://media4.giphy.com/media/GC0PVgS4iGZwxRXyRW/giphy.gif?cid=790b7611a38a415978e330d01795b55f870e21d94f183392&rid=giphy.gif&ct=g)
>
Step-by-step:
>
1. Select the _shake button_.
1. Hold the control and click-drag from the storyboard button into your view controller source file as if you were to create a IBOutlet.
1. When prompted to name your IBOutlet, change the connection type from `Outlet` to `Action` using the dropdown menu.
1. Name the IBAction, `shakeButtonTapped`.

You'll notice this creates a new function within your view controller. Whenever the _shake button_ is tapped, this function will be called.

To see this in action, let's print some text in the debug console each time the _shake button_ is tapped.

## Print Debugging

Up to this point, we haven't really discussed or used the debugger. The debugger is an extremely powerful tool that allows us to figure out bugs in our app. In our case, we'll just be printing a simple log to the debug console when a user interacts with our button.

To start, we'll need to add a print statement within our IBAction `shakeButtonTapped`.

> [action]
In your `ViewController.swift`, modify `shakeButtonTapped(_:)` to the following:
>
```
@IBAction func shakeButtonTapped(_ sender: Any) {
    print("Shake it like a polaroid picture!")
}
```

Now, let's run the app and try it out.

Once the app launches and you see the UI, click on the _shake button_. In your Xcode debugger, you should see your print statements show up each time you press the shake button!

![Print Debugging](assets/print_debugging.png)

As you can see, our `shakeButtonTapped(_:)` is called each time the user taps the button.

# Changing Label Text

We've managed to print a log to the console when the button is tapped. Let's take it one step further and change the label text on button tap.

> [action]
In `ViewController.swift`, add the following line of code to `shakeButtonTapped(_:)`:
>
```
@IBAction func shakeButtonTapped(_ sender: Any) {
    print("Shake it like a polaroid picture!")
>
    answerLabel.text = "button was tapped"
}
```

Build and run the app again. Tap the _shake button_ and you should see the answer label change to the following text:

![Changed Text](assets/changed_text.png)

*Here's what we did:*

Each `UILabel` has a text attribute that can be changed and updated. This will also update the UI on the screen. When `shakeButtonTapped(_:)` was called, we set the text property of our label to a new string.

With our new knowledge of handling button interactions and changing the label text, we now can implement our logic of randomly selecting displaying a Magic 8-Ball answer.

# Implementing Our Logic

We now have all the tools of implementing our Magic 8-Ball. First, let's close the _Assistant Editor_ and return to the _Standard Editor_.

> [action]
Use the _Project navigator_ to display `ViewController.swift` in the _Standard Editor_.

Next, let's implement our logic. First, we'll add an instance variable that is an array of strings containing all possible answers of our Magic 8-Ball. Feel free to add in some of your own!

> [action]
Add the following array of strings above our IBOutlets:
>
```
class ViewController: UIViewController {
>
    // MARK: - Properties
>
    let answers = ["Yes, definitely", "It is certain", "Without a doubt", "Yes", "Most likely", "Sure, why not?", "Same", "Tell me more", "Out to lunch", "Reply hazy, try again", "Ask again later", "The cake is a lie", "42", "TMI", "Very doubtful", "Don't count on it", "My reply is no", "Absolutely not"]
>
    @IBOutlet weak var answerLabel: UILabel!
    @IBOutlet weak var shakeButton: UIButton!
>
    // ... rest of code
}
```
>
For your convenience, here's a the plain text version of the answers array code above:
>
let answers = ["Yes, definitely", "It is certain", "Without a doubt", "Yes", "Most likely", "Sure, why not?", "Same", "Tell me more", "Out to lunch", "Reply hazy, try again", "Ask again later", "The cake is a lie", "42", "TMI", "Very doubtful", "Don't count on it", "My reply is no", "Absolutely not"]

With our new array of answers, we can randomly select an item in our array whenever the shake button is tapped and change the text of the answer label to display it.

> [action]
To randomly choose an answer, we can use the `Int.random(in:)` method. Change `shakeButtonTapped` in our view controller to the following:
>
```
@IBAction func shakeButtonTapped(_ sender: UIButton) {
    // 1
    let randomIndex = Int.random(in: 0..<answers.count)
>
    // 2
    answerLabel.text = answers[randomIndex]
}
```
>
Let's break down our code step by step above:
>
1. We use `Int.random(in:)` to randomly generate a index of an answer (between `0` and the number of answers we have).
1. Last, we set the answer's label text to match the randomly generated answer.

Build and run the app! Ask the Magic 8-Ball a couple questions and test that it works...

Congrats, we've implemented the basic Magic 8-Ball functionality.

Before we move on, let's take it one step further and implement the shake functionality that comes with a standard Magic 8-Ball.

# Implementing the Shake Gesture

The iPhone by default has implemented certain methods you can override to listen and act on certain events the user takes.

For the shake gesture, we can override a system implemented function and place our own functionality so that the label changes if the user shakes their app.

> [action]
Add the following method to your view controller:
>
```
override func motionEnded(_ motion: UIEventSubtype, with event: UIEvent?) {
    guard motion == .motionShake else { return }
>
    let randomIndex = Int.random(in: 0..<answers.count)
>
    answerLabel.text = answers[randomIndex]
}
```
>
As you can see, we override the `motionEnded(_:with:)` event and check for the `.motionShake` event. If triggered, we run the same logic to randomly select and display an answer.

# Keeping Things DRY

One general rule of thumb for programming is keeping things _DRY_. DRY stands for Don't Repeat Yourself. In other words, you shouldn't be copying and pasting the same code over and over in your codebase.

> [info]
Why do you think copying and pasting your code in multiple places is bad practice?

In our current logic, you can see that we have the same logic for randomly choosing and display an answer twice. We can refactor this to a single method and call this method from both the shake event and button tap instead.

> [action]
In `ViewController.swift` add the following method:
>
```
func generateAnswer() {
    let randomIndex = Int.random(in: 0..<answers.count)
>
    answerLabel.text = answers[randomIndex]
}
```

Next we can refactor our code to use our new `generateAnswer` method:

> [action]
Change both `shakeButtonTapped(_:)` and `motionEnded(_:with:)` to the following respectively:
>
```
@IBAction func shakeButtonTapped(_ sender: Any) {
    generateAnswer()
}
>
override func motionEnded(_ motion: UIEventSubtype, with event: UIEvent?) {
    guard motion == .motionShake else { return }
>
    generateAnswer()
}
```

Run your app and test out your new Magic 8-Ball. Be sure to test both your new shake gesture and the existing button tap logic.

To test the shake gesture in the iPhone simulator, make sure the simulator is active and select the hardware menu. In the dropdown, you will see an option for `Shake Gesture`.

![Simulator Shake](assets/simulator_shake.png)

## Wrapping Up

In this last section, we took the UI we built in storyboard and hooked it up to our code. We looked at the relationship between storyboard and Swift source files and how they communicate on a basic level.

We figured out how to respond to some basic user gestures (button taps and shakes) and finally implemented some logic for our Magic 8-Ball to work.

In the next section, we'll wrap up by reviewing what we learned.

---
title: "Conclusion"
slug: conclusion
---

Congrats! You've just built your first iOS app.

![Finished App](assets/finished_app_flow.png)

You taken your first steps on your journey to become an iOS developer.

In this tutorial, you were introduced to many new concepts in Xcode and iOS development. To recap, you learned how to...

- Create new Xcode projects
- Use different tools in Xcode
- Build simple user interfaces (UI) using _Interface Builder_
- Connect storyboard to code with the _Identity Inspector_, IBOutlets and IBActions
- Implement app logic for your Magic 8-Ball

Try to remember and visualize what you did for each of these steps in your head.

## Where To Go From Here?

If it went by in a blur, don't worry. You'll need to keep practicing, but eventually these steps will be drilled into your head once you go through the process on your own a few times...

Which leads us to your next challenge!

# A Challenge Approaches

To quote Zig Ziglar, "Repetition is the mother of learning."

To really learn iOS development, we'll have to put the new skills we learned to the test. We'll want to keep repeating and practicing these foundational steps until we know them by memory.

## The Challenge

Coming up with new ideas for apps can be hard. To help out, you're going to creating a startup idea generator. This app will require many of the same skills and concepts you learned during the Magic 8-Ball tutorial.

Try completing this challenge on your own. Refer back to the tutorial only when you get stuck.

## App Design

![Startup Idea Generator Design](assets/startup_generator_design.png)

Here's an example screenshot for the final app. Feel free to get creative and add your style into app design.

## Specs

Similar to the Magic 8-Ball app, you're project will revolve around randomly generated content. This time around, you'll be generating new content for two labels instead of one.

The first label will be set from an array of strings.

Your array will containing the names of existing startups. You can use the array below or generate your own:

```
["Make School", "Uber", "Netflix", "Facebook", "Google", "Kickstarter", "Spotify", "Airbnb", "Snapchat", "YouTube", "Dropbox", "Amazon", "Craigslist", "Tinder", "Instagram", "Tesla", "Twitter", "SpaceX"]
```

The second label will be also set from an array of strings. This time, the array will contain the names of random industries, animals or categories. You can use the array below or generate your own:

```
["Dogs", "Books", "Gamers", "Star Wars", "Bitcoin", "Goats", "Zombies", "Rich People", "Swimmers", "Florida", "Vampires", "Dragons", "Internet of Things", "Mars", "Cryptocurrency", "Mosquito Repellent", "Fidget Spinners", "Sun Screen", "Water Bottles", "Lost Travelers", "Superheroes"]
```

Your app will generate new startup idea whenever the user taps the generate button or shakes the phone.

> [info]
**Pitch That**
>
Another fun way to make use of this app (when you're done) is by practicing your pitching skills with friends. Take turns generating startup ideas with your app and pretend to give a 1 minute pitch to your friends. Your friends can act as investors. At the end of each round, everyone can decide who got funding and who didn't.

Good luck the challenge! Remember, you can look back on the tutorial or your previous code if you get stuck.

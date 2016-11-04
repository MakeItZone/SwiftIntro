# SwiftIntro

*These are the Swift files for the starship Enterprise...*

er, no.

Instead they are the humble beginnings of an introduction to Swift iOS app development course, targeting 12+ year olds. The course is for small groups. Students decide on their own project and topics are introduced to enable them to build their app. The course also covers some of the wider aspects of successful software development, such as team work, source code control, design methodologies, and computer science.

The first iteration of this course was co-taught with an introduction to robotics course using Lego MindStorms. At times this was used to advantage to compare and contrast approaches- e.g. graphical, block based (Labview/NXT) vs text based development; top-down vs iterative design.

The robotics course was left to be very free form with a basic outline challenge that was brainstormed with the students: *create a 'tank' robot that has a cannon to shoot/defend itself from other robots.* Soon after a second 'buddy' bot was added. Once the basic vehicles were built coding challenges were given. They will be included in *italics* in the class notes below. Other robots (Sphero, Ollie, Parrot Jumping Spider, Makelangelo style drawbot) were bought in to discuss and explore as well.
 
These notes were written after the first few classes were taught; the exact order of topics and duration is not 100% accurate!

## Classes ##

### Class 1 ###

* introductions
* learning about the tools: XCode
	* checking installed version; upgrading/installing as needed
	* talking about tools developers use
	* potential effects of working with different versions of tools
* brainstorming applications
	* mindmaps/notes
* concept: requirements
	* that there are different kinds of requirements, e.g. business, user, customer, developer, QA, etc
	* that there may be conflicts
	* importance vs priority 

*Similar breakdown for the MindStorms class. Started building.*

### Class 2 ###

* Source code control
	* What is it?
	* Why is it useful? For the individual? For a team? Product development? Release?
	* History
	* Branches
* Advantages of distributed SCM, focusing on Git
	* Backup
	* easy to replicate to new computers
	* teams
* Public vs Private development
	* e.g. (free) GitHub vs BitBucket
* Students choose a provider (GitHub or BitBucket) and created an account (and personalized icons, etc)
* Those who choose GitHub also downloaded the desktop client
* Created an "hello world" repository
* Downloaded it
* Changed
* Uploaded
* verified changes showed up on the Github/BitBucket website
* **Important** - lab computers are shared. Showed students how to log out of GitHub app.
* some more time brainstorming their apps

*References*

* [Great explanation to source control, using `git`][betterexplained-git]
* Github + XCode
	* [BlogPavBlog article re XCode and GitHub integration][pavley-xcode-github]
	* [Ray Weinerlich article re Git + XCode][raywenderlich-xcode-git]

*Robotics class: looked at a Makelangelo style drawbot. Got it running, drew a picture while class was running. Continued building, designing, and re-designing robots. E.g. 'What about the controller brick- where is that going to go?'*

### Class 3 ###

* Objects
* Briefly introduced the concept of abstraction
* families of items
* allows for *interfaces*/*contracts*
* can be used for testing
* used clichéd, but easy to understand "animals" class hierarchy. Abstract animal, with "move", "makeSound" "verbs". Dog, Cat, Duck concrete classes.
* beneficial side-effect: may have to type less code
* beneficial side-effect: may be able to re-use tests
* started to review app ideas for likely objects/hierarchies

*Mindstorms class: diversion. Looked at Sphero, Ollie, and Rolling Spider. Made a challenge course where first bot had to be programmed to go through maze to get to 2nd, that solved it's maze, that triggered third. Each student had to program their part using e.g. Tinker or Sphero Lightning lab.*

### Class 4 ###

* Iterative vs Top-Down design
* compared and contrasted top-down (gather all requirements first; what they'd been doing with their apps) vs iterative (how they've built their robots)
* Noted:
	* hard to gather all requirements up front
	* easy to get bogged down in ideas and theoretical "what-if" analysis
	* building fast can lead to "doh!" mistakes and rework
	* building fast can give a sense of accomplishment early
* Highlighted
	* neither wrong or right
	* tools to use as needed
	* situation should heavily influence choices (pacemaker or passenger jet flight control vs game website or phone app)
* Created new X-Code projects
* Created new GitHub repositories
* started typing in UI animation playground
	* discovered:
		* tab-completion/auto-completion
		* syntax highlighting
		* importance of upper/lower case
		* compiler errors
	* compared graphical block programming (e.g. scratch) vs freeform, text based, coding

*MindStorms class: more building, but started to add some requirements analysis to iterative "just build" approach. Redesigned to incorporate NXT controller.*

### Class 5 ###

* UI Animation playground II
* Finished typing it in
* Code walk-through
* think of a modification (e.g. color, size), figure out how to implement it, see the change work, fix errors, repeat

*Mindstorms class: started programming main bot- go in a straight line, turn 180˚, go straight, fire canon. Buddybot build finished. Programmed to go straight and turn. Discovered turning is dragging the wheels and not smooth.*

### Class 6 ###

* `UIButton` Playground
* Typing in code to a new playground/playground page: draw a `UIKit` button.
* Think of modification, then implement, test, repeat- e.g. size, color
* add a `UILabel`
* Start drawing out buttons for apps

*References*

Example `UIButton` playground is based on:

* [SO: adding a `UIButton` to a playground][SO-playground_button]
* [SO: programmatically create a button][SO-create_button_programmatically]
* tweaked and modified to work with latest Swift and Xcode

*Note*
Choose not to use interface builder because

* students are a group that very much want to know what's going on in the code
* `IBOutlets`, and the boilerplate pack a lot of concepts and abstractions
* StoreyBoard/XIB/NIB files can be hard to debug
* suggest introducing Interface Builder after students have implemented a `class` in a playground that implements call-backs and have some confidence in how the pieces work together, and then transferred that into their iOS app.

*MindStorms class: Mainbot - program it to move in a square "patrol" pattern. Rebuild buddy-bot so that it can turn better.*

## Future Class Ideas ##

**App Dev**

* implement a class in the `UIButton` playground that has a callback function. Add callback to button and test.
* make sure UI has a few elements; e.g. couple of buttons ('about', 'help', ...), label(s)...
* move code from playground into the app template and show it working in the simulator
* talk about resolution independence- portrait vs landscape, different screen sizes => size classes.
* introduce more advanced/useful automatic layouts techniques: constraints, relationships, grids, etc
* modify UI to work landscape, portrait, multiple devices
* introduce Interface Builder (IB). Compare generated code to handcrafted code. Show round-tripping. Compare and contrast pros and cons of handcrafted UI vs IB.
* Get UI mocked up using hand-crafted code or IB
* design and implement business logic classes
* introduce test cases, test automation
* explain how model, view, and control (logic) can be separated but still work together
* really work on the app!
* iTunes publishing process

** MindStorms **

* get 'main bot' to 'patrol'
* introduce sensors- get buddy-bot to follow
* get 'main bot' to follow a line
* detect an intruder
* target and fire cannon


## References ##

* [Apple’s list of XCode 8 and Swift 3 resources][apple-swift-resources]
* [Adding documentation to playgrounds- markup][apple-playground-markup]
* [Appcoda iOS10 Swift dev book][appcoda-book] - very detailed, looks to be well written.
* Raywenderlich is well known as an online educator for Apple development. Given the quality of his online tutorials, guessing his [Swift Apprentice][swift-apprentice] book is equally good.
* [Swift 3 complete language cheat-sheet][hackingwithswift] 
* [O'Reilly XCode Playgrounds Video Tutorial][infiniteskills]
* [Prototyping `UIView` animations in a Swift Playground][possiblemobile]
* _"The goal of Swift SpriteKit: Playground Animation Workbook is to introduce you to 2D sprite animation with SpriteKit. SpriteKit is Apple’s framework for manipulating 2D graphics in iOS, OS X, and tvOS applications."_ Looks reasonable, very inexpensive. [Kindle eBook][swift-spritekit-playground]
* [IBM's online Swift sandbox for server development][ibm-playgrounds]

[raywenderlich-xcode-git]: http://www.raywenderlich.com/13771/how-to-use-git-source-control-with-xcode-in-ios-6
[pavley-xcode-github]: http://www.pavley.com/2013/06/12/getting-xcode-and-github-to-work-together-like-besties/
[betterexplained-git]: https://betterexplained.com/articles/a-visual-guide-to-version-control/
[swift-spritekit-playground]: https://www.amazon.ca/Swift-SpriteKit-Playground-Animation-Workbook-ebook/dp/B01A7WSGBA/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1474597762&sr=1-1
[possiblemobile]: https://possiblemobile.com/2015/03/prototyping-uiview-animations-swift-playground/
[infiniteskills]: http://www.infiniteskills.com/training/learning-to-program-with-swift/xcode-playgrounds.html
[hackingwithswift]: https://www.hackingwithswift.com/read/0/0/introduction
[swift-apprentice]: https://www.raywenderlich.com/store/swift-apprentice
[appcoda-book]: http://www.appcoda.com/learnswift/index.html
[apple-swift-resources]: https://developer.apple.com/swift/resources/
[apple-playground-markup]: https://developer.apple.com/library/content/documentation/Xcode/Reference/xcode_markup_formatting_ref/AddingMarkup.html
[ibm-playgrounds]: https://developer.ibm.com/swift
[SO-playground_button]: http://stackoverflow.com/questions/27631133/how-to-add-a-uibutton-to-swift-playground
[SO-create_button_programmatically]: http://stackoverflow.com/questions/24030348/how-to-create-a-button-programmatically
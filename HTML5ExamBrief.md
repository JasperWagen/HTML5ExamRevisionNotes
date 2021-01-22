# HTML5 Application Development Fundamentals

## Application life cycle (20-25%)
### Understand the platform fundamentals
**Packaging and runtime environment:**
* The runtime environment is responsible for access to devices, media, networking and storage
* The Document Object Model (DOM) is and API that allows programs and scripts to update content structure and states on the fly. It ties HTML and JS together.
* Windows Runtime environment is called WinRT

**Host Process:**
* Apps require a runtime host to start them (for instance your OS starts your browser)
* Talks a lot about metro style apps (wiget style apps built with HTMl5)
* The host process for Metro apps is WWAHost
* Code inside apps is mostly restricted to that application
* If a metro app wants to access other parts of the system it must declare this in the Capabilities section of the manifest 

**App package and app container:**
* The purpose of an app package is for ease of distribution and deployment 
* An app container ensures the app runs in its own memory space and does not corrupt the operating system
* App packages, after installation, execute in a runtime app container with separate memory space
* Packages can be nested

**Credentials/permission sets:**
* The .NET framework is a background Windows component, providing a code execution environment  
* .NET framework provides a secure environment in which HTML5/JS apps can run, it uses security transparency to separate different kinds of code while running. Using permission sets and identity permissions to control the environment.
* Permission sets are defined by the .NET framework and have several levels, ranging from nothing (no code can run) to full trust.
* Identity permissions protect assembilies (compiled code libraries). Each identity permission represents set of credentials that an assembly must have to run

**Tablet applications:**

### Manage the state of an application:

**Manage session state:**
* A session state is created when a user accesses and app, ends when the session closes
* In a browser this is from the time a request is made to a site to the time the browser closes 

**Persist state information:**
* Persistent state information is data the app needs after the session ends

**Understand the different application states:**
* Session state is created when the users first requests access to an application, ending when the user closes the session 
* Application state is created when the browser sends the first request to the webserver, ending when the browser is closed 

**Understand differences between local and session storage:**
* HTTP is stateless so data isn't stored from session to session 
* Cookies are used to save state
* They are small files that contain information about the user and are save on the users local machine 
* Cookies are a security risk 
* They can be max 4mb 
* localStorage allows users to persist large amounts of data between sessions
* sessionStorage method keeps data for only one session

**AppCache:**
* Caches data on a users local machine that would be usually stored on a server
* Stores resources such as photos, pages, css files etc.
* This enables faster load times 

### Debug and test HTML5-based touch enabled application:
**Touch gestures:**
* A gesture is any finger move
* The response to a gesture is called an event (touchstart, touchend and touchmove)
* Design for differing hand sizes, dominant hand and screen orientation

**Which touch gestures you test on a device:**
* Multi touch events resulting in unintended scrolling or zooming
* Reaction to touch events 
* Overall responsiveness 
* Tapping, pinching and rotating 
* Controlled scrolling and panning 
* Ability to disable scrolling and panning
* Accuracy of snap points

**Leveraging existing HTML5 skills and content for tablet apps:**
* Exiting HTML5 skills translate to metro style tablet apps 
* Shallow learning curve

**Debugging and testing HTML5 apps:**
* Aim to provide reliable secure and useful 
* A validator looks for anything that could cause misinterpretation of code 
* Windows app certification kit is a tool for testing local apps before publishing to the windows store 

## HTML5: Building a UI (25-30%):

Chose and configure HTML5 tags:
* To display text content
* To display graphics:
  * When why and how to use canvas 
  * When why and how to use scalable vector graphics (SVG)
* To play media (video and audio)
* To organise content and forms:
  * Tables
  * Lists
  * Sections
  * Semantic HTML 

## CSS: Formatting the user interface (20- 25%)
Understand the core CSS concepts:
* Separate presentation from content 
* Manage content flow (inline vs block)
* Manage positioning of individual elements
* Manage content overflow
* Basic CSS styling

Arrange UI content:
* Proportional scaling, free scale, flexbox, grid
* Order and arrange content
* Flexbox for simple layouts
* Grid for complex layouts
* Grid content properties 
* App templates

Manage the flow of content by using CSS
* Regions and using regions to flow text content between multiple sections
* Content source, content container, dynamic flow, flow-into, flow-from, msRegionUpdate, msRegionOverflow, msGetRegionContent
* Columns and hyphenations, optimising readability 

Manage the graphical interface by using CSS:
* Graphics effects  (rounded corners, shadows, transparency,background gradients, typography, and Web Open Font Format)
* 2D and 3D transformations (translate, scale, rotate, skew, and 3-D perspective transitions and animations)
* SVG filter effects
* Canvas

## JavaScript: Writing code (30-35%)
Manage and maintain JS:
* Create and use functions
* jQuery
* 3rd party libraries 

Update the UI by using JS:
* Locate/access elements
* Listen and respond to events
* Show and hide elements
* Update the content of elements 
* Add elements 

Code animations using JS:
* Use animation
* Manipulate the canvas 
* Work with images
* Shapes
* Other graphics

Access data access using JS:
* Send and receive data
* Transmit complex objects and parsing 
* load and save files 
* App cache
* Data types 
* Forms 
* Cookies 
* Local storage 

Respond to the touch interface:
* Gestures
* How to capture and respond to gestures

Access device and operation system resources 
* In memory resources (ie. contact lists and calender)
* Hardware capabilities (ie GPS accelerometer and camera)
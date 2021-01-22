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
* In order to enable app cache the attribute manifest must be addeed to the html tags 

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

## HTML5: Building a UI (25-30%)
### Understanding the essentials of HTML
**Using Attributes:**
* Attributes are modifiers of HTML elements the provide additional info
* They are included within the tag 

**Understanding Entities:**
* An entity is a special character ie dollar sign or trademark
* Incorporating these in a webpage is known as character encoding  
* These can become garbled between systems so is safer to use the numbered entry that starts with &
* It is best to use UTF-8 charset, this is specified in the HTML header

**Understanding the DOCTYPE:**
* The doctype is the declaration found at the top of HTML documents is <!DOCTYPE html>

### Chose and configure HTML5 tags
There are several new text related elements compared to HTML4 such as: command, mark, time, meter and progress. Whilst beasefont, center, font and strike have been depreciated. 

**Text Elements:**
* b - (bold) should be used to offset text without conveying importance ie product names as actionable items
* i - (italic) is used for alternate voice or mood 
* strong - denotes strong importance 
* em - indicates emphatic stress 
* small - is used for smallprint like copywrite 
* mark - highlights a section of text 

**Deprecated Elements:**
* acronym - Defines acronyms in HTML 4 that can be spoken as if they are a single
word, such as GUI for graphical user interface. Use the abbr tag instead.
* applet - Defines an embedded applet. Use the object tag instead.
* basefont - Defines a default font color, font size, or font family for all the text in a
document. Use CSS for applying all fonts.
* big - Makes text bigger relative to the current font size. Use CSS instead.
* center - Center-aligns text and content. Use CSS instead.
* dir - Defines a directory list. Use the ul tag instead.
* font - Specifies the font face, font size, and font color of text. Use CSS instead.
* frame - Defines a particular frame (a window) within a frameset (see the next
bulleted item).
* frameset - Defines a frameset for organizing multiple frames (windows).
* noframes - Displays text for browsers that don’t support frames.
* strike - Defines strikethrough text. Use the del tag instead for small amounts of
text, or use CSS for large blocks of text.
* tt - Defines teletype or monospaced text. Use the code tag or CSS instead.

**To display graphics:**
Img:
* Use img tags to display linked images
* Can by in server files or external api 
* Scalable vector graphics (SVG) enables creation of scalable objects the resize to best fit the viewport 
* A raster image is made up of pixels where
* A vector image is made up of lines and curves based on maths expressions
* Raster imaged loose quality as you enlarge whereas vector images maintain quality 
* The alt attribute of the img tag displays on a hover event or with screen readers

Figure: 
* Figure and figure captions enable you to control the type of image you are displaying and the ability to include captions
* figure specified the type fo figure you're adding ie image, diagram or photo
* figcaption adds a caption to the figure

Canvas:
* canvas - creates a container for graphics, using JS to draw the graphics dynamically 
* canvas - can be used to create online games,rotating photo galleries and stocktickers similar to flash
* A canvas is first designed with attribute requiring the id attribute to be added to the DOM
* This element can be the retrieved using JS and manipulated within a function using the context api
* Canvas functions:
  * fillText - draws text 

SVG:
* Scalable vector graphics (SVG) is a language for describing 2D graphics in (XML) 
* XML is a cousin to HTML
* Main benefit is flexibility as vector graphics scale to fit the viewport 

Canvas vs SVG:
* If the drawing is small use canvas
* Canvas is better for a large amount of objects as SVG degrades as more elements are added
* Canvas for small screens, SVG for large
* SVG for high detailed applications
* Canvas for realtime data output 

Other tags:
* meter - displays a colored bar

**To play media (video and audio):**
* video is used alongside the src attribute to include video files in HTML, height and width can also be specified 
* Other attributes inclue:
  * poster: displays a static img before the video loads
  * autoplay: Start playing the video automatically on page load
  * controls: Displays a play pause vol etc.
  * loop: repeats the video 
* Both file format and codec should be specified 

**Audio Tags:**
* audio tag is used to incorporate audio 
* Multiple formats should be specified to ensure compatibility 

**Touch Controls**
* Diabling certain touch controls is performed in meta tags:
  * user-scalable ="no" - disables touch zooming 

### To organise content and forms
**Understanding semantic HTML:**
* Semantic markup uses taf names that are intuitive, aiding building and modifying HTML documents and interpretation by web browsers
* Note: class and id are *global attributes* which can be used with any element 
* Example: instead of using div elements with classes and ids use specific tags for that element ie header, nav, aside 

**Using tags to add structure:**
* Examples of semantic structural elements:
  * address - Defines an area for contact information for a page or section
  * article - Defines an article, such as a magazine or newspaper article, blog post, or
  similar content
  * aside - Defines content that’s separate from but related to the page content; similar to a sidebar in book chapters and magazine articles
  * details - Contains additional details pertinent to text around it; creates an interactive widget a user can display or hide
  * footer - Defines a footer for a document or section; may include the document author, contact information, copyright information, and links to terms of use
  * header - Defines a header for a document or section; may contain introductory content or navigation links
  * hgroup - Groups headings and subheadings (using the h1 to h6 tags) for multi-level headings
  * nav - Defines a block of navigation links
  * section - Defines a section in a document, such as chapters, parts of a thesis, or parts of a Web page whose content is distinct from each other
  * summary - Defines a visible heading for a details element; user can click to display or hide information
  * wbr - Defines a possible line break; when a word is very long, or you’re concerned the browser will break a line at the wrong place
  * sub - defines subscript text

**Using tags to create tables and lists:**
Tables:
* Tables display information in grids]
* Tables are created with the following tags:
  * table
  * tr - table row
  * th - column header
  * td - cell
  * caption can be used on tables
  * thead, tfoot, tbody - used for lond tables which require scrolling, the content in thead and tbody will stay on screen whilst tbody will scroll between them 


Lists:
* Lists can be ordered or unordered 
* Entries use li
* Ordered lists:
  * ol - Orders using numbers by default 
  * Has attributes:
    * reversed
    * start number
    * type - kind of marker such as letters or numerals 

* Unordered lists:
  * ul - Displays a bulleted list 
  * Has a type attribute that denotes the bullet style 

* Definition list:
  * dl - Desplays items with their definitions below them and indented
  * dt - Denotes each term in the item
  * dd - Denotes each description

### Input and Validation
**Understanding input and forms:**
form Attributes:
* accept-charset=character_set - Specifies a set of character encodings the server accepts
* action=URL - Specifies the Web address to which form data is sent
* autocomplete="on"/"off" - Specifies whether autocomplete is on or off
* enctype - application/x-www, form-urlencoded, multipart/form-data,  text/ plain -Specifies the encoding type for form data when submitting the data to a server; used only for method="post"
* method="GET"/"Post" - specifies the http transmission method used when sending form data
* name=TEXT
* novalidate 

input attributes:
* pattern - matches against regex
* placeholder - displays greyed out text
* type = "file" - for file upload 

### Touch input:
* When a touch event is received the *target* property of each touch item in the *touchList* represents the DOM element that was touched

* Resistive touch is best for use with gloves


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
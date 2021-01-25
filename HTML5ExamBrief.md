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
### Understand the core CSS concepts:
**Separate presentation from content:**
* the *link* tag is used to link html to CSS
* *link* requires the follow attributes:
  * href - URL to the .css file
  * rel = "stylesheet"
  * type = "text/css"
* Standard practice is to link to separate stylesheets although inline styling is acceptable in small projects 
* "Separation of content and style"
* *@import* is used to embed one css file in another 

**Selectors and Declarations:**
* selector selects the element to be styles ie p, #header, .user-form
* Declaration is what is between the {}, ie. {colour: brown}
* Property is the key in the declaration key value pair
* Value is the value in the key value pair 

**Fonts:**
* Prior to CSS3 only web-safe fonts could be used
* CSS3 provides the @font-face rule which enables developers to use any fonts they choose 

**Manage content flow (inline vs block):**
* "Flow" is the filling of horizontal lines from left to right across the display, and separation of lines from top to bottom
* Inline flow: Fills only as much width as required
* Block flow: Fills as much width as is available 

**Manage positioning of individual elements:**
  * Default value of the position property is *static* (immediately after the document's previous element)

Float positioning:
  * *Float Positioning* moves an element as far to the left or right as it is permitted, text then wraps around this element. 
  * Simple columns are examples of float positioning (text would not overflow between columns however)
  Note: you can generate lipsum in MS Word by typing =lorem() and pressing enter 

Absolute positioning:
  * Element is excluded from the flow of the document
  * It is instead placed in a "geometric position"  (fixed distance from top and side)
  * Position does not vary with scrolling ie. header and footer 

**Manage content overflow:**
* Overflow is the management of elements that exceed their allotted *bounding box*
* A bounding box a rectangle that an element is assigned to fit within

Scrolling overflow:
* In scrolling overflow an element's content will not exceed it's bounding box
* The extra content will be accessed by scrolling within the bounding box
* {overflow:scroll} is used to access this property value 

Visible and hidden overflow:
* Visible overflow writes over the content that follows it
* Hidden overflow makes overflow invisible 

* Basic CSS styling

### Arrange UI content
**Designing UI with CSS:**
* Relative positioning was used traditionally to achieve flexibility in website design but does not work well for mobile
* Instead a combination of absolute positioning and flexible boxes work much better for mobile UI 

**Browser Compatibility:**
* *Vendor prefixes* are used to work around browsers supporting different CSS3 properties:
  * -ms- - Internet explorer
  * -moz- - Mozilla Firefox
  * -o- - Opera 
  * -webkit- - Chrome and Safari

**Flexbox:**
* Hold text, images, toolbars, menus and other content 
* Used for simpler layouts
* Browser automatically adjusts the size of the box depending on the viewport
* Based on the box model:
  * Margin: transparent and sits at the outermost edge of the box, providing space between the box and other boxes in the document 
  * Boarder: surrounds the box itself. Can be coloured or patterned
  * Padding: the space between the element and the boarder, usually taking on the same colour as the element's background 
* Flexbox is similar to block layout but dows not use columns or floats. 
* Flexboxes resize both horizontally and vertically
* Has two flavours:
  * flexbox: stet the flexbox as a block-level element 
  * inline-flexbox: sets the flexbox as an inline-level element 
* Flexbox properties:
  * **flex**: makes child boxes flexible by height and width 
  * **flex-align**: Sets the default alignment for child boxes, if the orientation of the parent box is horizontal flex-align determines the vertical alignment of the child boxes and vise versa  
  * **flex-direction**: Controls the direction of child boxes in the parent box
  * **flex-flow**: Sets the flex-direction and flex-wrap properties at the same time 
  * **flex-item-align**: Overrides te default alignment of child boxes styled with the flex-align property 
  flex-line-pack: Sets child box alignment within the parent box when extra space is present
  * **flex-order**: Assigns child boxes to groups and controls the order in which they appear in a layout, beginning with the lowest numbered group 
  * **flex-pack**: justifies the alignment of child boxes within a flexbox to ensure all whitespace in the parent box is filled 
  * **flex-wrap**: determines whether child boxes automatically create a new line and wrap ono it or overflow the flexbox 

 

**Grid layouts:**
* {display: grid/inline-grid}
* Simply rows and columns that control the layout in an HTML document
* Give greater control over complex layouts 
* Offers modularity so you can easily drop elements into a grid. 
* More flexible and easier thant HTML tables 
* Child elements of a grid are called grid items, which are positioned acording to:
  * **Grid tracks** - The columns and rows of the grid; defined using the *grid-rows* and *grid-columns properties
  * **Grid lines** - The horizontal and vertical lines that divide the grid
  * **Grid cells** - The logical space used to layout grid items
* Columns and rows can have a fixes size in px, a fractional size in fr or be set to auto scale
* Grid properties:
  * **grid-columns/grid-rows**: Specifies parameters for one or more columns or rows in a grid 
  * **grid-template**: Provides a visualization of the grid element's structure and defines the grid cells 
  * **grid-cell**: Positions a child item within a named gridcell 
  * **grid-column/grid-cell**: Positions child items in a grid 
  * **grid-column-span/grid-column-span**: Defines the dimensions of a grid by specifying the distance (in lines) from the starting line to ending line 
  * **grid-column-sizing/grid-row-sizing**: Changes the size of implicit columns or rows, which are auto-sized by default
  * **grid-flow**: creates additional columns otr tows as needed to accommodate content 
  **grid-column-align/grid-row-align**: controls a child item's alignment within a cell 

Grid Templates:
* A grid template uses alphabetical characters to represent the position of items in a grid. 
* {grid-template: "abcd"}
  
### Manage the flow of content by using CSS:
**CSS Regions:**
* Regions manage the flow of content between  discontiguous areas of the page (areas that don't touch)
* In the event of overflow from one region of the HTML document the remaining content will automatically flow to the next region 
* This makes document more responsive and accessible for screen magnifiers 

Flow-into and flow-from: 
* To implement CSS regions both a content source and content containers need to be specified
* This is achieved with the *flow-into* and *flow-from* properties
* **Content source:**
  * May be one or more blocks of text in the shame or a separate HTML file, this is referred to as a *content stream*
  * {flow-into: main} - content sources are assigned by specifying where content should be flowed to 
  * The value of the property ("main" in the above example) is called a *named flow*
* **Content containers:** 
  * The areas into which the content flows 
  * {flow-from: main} - creates the content container by referencing the *named flow*
* Both flow-into and flow-from can be assigned to multiple elements referencing the same named flow, The content will be pulled from the source in the order in which it appears in the DOM. This is known as the *document order*

Overflow:
* In order for flow to work the dimensions of the region must be fixed 
* How overflowing the last region is handled is defined by the `region-overflow` and `overflow` properties

Microsoft's implementation:
* Microsoft's implementation of CSS regions differs slightly
* *iframes* are used, like mini boxes on a web page that can contain external content
* The `-ms-` prefix must be used with the `flow-into` and `flow-from` properties 
* iframes properties:
  * `msRegionUpdate` - Allows dynamic manipulation of regions 
  * `msRegionOverflow` - Handles content overflow, similar to the `region-overflow` property
  * `msGetRegionContent` - A script method that returns an array of Range instances corresponding to the content from the region flow that is positioned in the region 

**Using columns and hyphenation:**

Columns: 
* The following properties are used to create and manipulate CSS columns:
  * `columns` - shorthand way of setting the number of columns and the column width in one declaration
  * `column-count` - Sets the number of columns and element should be divided into
  * `column-gap` - Sets the fap between columns, also known as the gutter
  * `column-rule` - Creates a vertical line in the gap between columns and sets it's style
  * `break-after` - Inserts a break after the generated column box 
  * `break-before` - Inserts a break before the generated column box
  * `break-inside` 
  * `column-fill` - Specifies how to fill columns, balanced equally between them or filling sequentially 
  * `column-span` - Specifies whether an element should span no columns or all columns 

Hyphenation:
* *Hyphenation* allows the proper breaking of words at the end of lines, avoiding the problem of long words wrapping to the next line
* Controlled with the `hyphens` property:
  * `auto` - Enables automatic hyphenation of words based on line-break opportunities within words or by "language-appropriate hyphenation resource"
  * `manual` - Enables hyphenation of word based only on line-break opportunities 
  * `none` - Prevents hyphenation 
* Language must be declared with `<html lang="en">` in order for correct hyphenation to occur 
* Vendor prefixes must be used with the hyphens property ie. `-moz-hyphens` (when this book was written anyway)
* Microsoft provides additional hyphenation properties:
  * `-ms-hyphenate-limit-zone` - Specifies the width of the trailing whitespace that can be left in a line before hyphenation occurs 
  * `-ms-hyphenate-limit-chars` - Specifies the minimum number of characters in a word that my be hyphenated

Exclusions:
* A *positioned float* is a CSS construct that enables positioning of images, text and boxes and then wrap text around them.
* Positioned floats achieved with *CSS exclusions*
* CSS exclusions alow the precise positioning of a float, exact distance from the top, bottom, left or right of it's container
* Exclusions are controlled with the following properties:
  * `shape-outside` - Creates the general shape of an exclusion
  * `shape-inside` - Modifies a shape's contents
  * `wrap` - Shorthand method of setting `wrap-flow`, `wrap-margin` and `wrap-padding` properties
  * `wrap-flow` - Specifies how exclusions affect inline content within block-level elements 
  * `wrap-margin` - Provides and offset for the content inside and element 
  * `wrap-padding` Provides a pad for content inside an element 
  * `wrap-through` - Specifies how content should wrap around an exclusion element 

### Manage the graphical interface by using CSS
**Creating Graphical Effects** 
Some new graphical effects to CSS3 are:
* `border-radius` 
* `box-shadow`
* `opacity`
* `linear-gradient`
* `radial-gradient`

Rounded corners:
* `border-radius` is used to create rounded corners around elements
* It's value can be in px, em or &

Shadows:
* `box-shadow` creates a *drop shadow* behind an element 
* `box-shadow: h-shadow v-shadow blur spread color inset;` is the syntax used:
  * `h-shadow` - horizontal position of the shadow in relation to the box
  * `v-shadow` - as above but vertical 
  * `inset` - moves shadow from the outside to the inside of the box 

Transparency:
* `opacity: value`
* Where value is a float between 0.0 and 1.0

Gradient:
* Several different types:
  * `linear-gradient(angle, color start, color end)` - Creates a gradient from top to bottom (default), side to side or corner to corner, specified as and angle in args
  * `radial-gradient(position,size and shape,color stops)` - Gradient radiates out from a central point 
  * `repeating-linear-gradient` - Straight bands of gradient colour 
  * `repeating-linear-gradient` - Circular bands of gradient colour 
* Can be applied to the `background` property 
* Supports colour interpolation in the RGBA space to avoid banding 

**Web Open Font Format (WOFF):**
* A way to enhance UI with any available or custom made font 
* Previously limited to *web safe* fonts
* To use WOFF host fonts on a webserver or use a web font service 
* WOFF files are compressed into:
  * True Type
  * OpenType
  * Open Font Format
* `@font-face {
    font-family:"font-name";
    src: url("URL");
  }`

**2D and 3D transformations**
* `transform` property can:
  * translate
  * scale
  * rotate
  * skew
  * spin 2D and 3D elements 
* Can have the following values:
  * `matrix (n,n,n,n,n,n)` - Specifies a 2D transformation with a 6 value matrix
  * `matrix (n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n)` - Specifies a 3D transformation with a 16 (4x4) value matrix 
  * `perspective(n)` - Specifies a perspective view for a 3D elements that's been transformed 
  * `rotate(angle)` - Rotates in 2D
  * `rotate3D(x,y,z,angle)` - Rotates in 3D 
  * `rotateX(angle)/rotateY(angle)/rotateZ(angle)` - Rotates in 3D along the specified angle 
  * `scale(x,y)` - Scales in 2D
  * etc..

3D perspective:
* *3D Perspective* - in this context it is how the browser renders the depth of a 3D transformed element 
* `perspective` takes a number value (1 to 1000), with lower values creating a more pronounced effect  

Transitions:
* A change of an element from one style to another 
* Created with the following properties:
  * `transition` - Shorthand way to specify settings for the following properties at once
  * `transition-property` - Specifies the CSS properties that will be transitioned
  * `transition-delay` - Specifies the amount of time after the value changing and the transition starting, (s or ms)
  * `transition-duration` - Length of transition (s or ms)
  * `transition-timing-function` - The speed curve of the transition effect (default: `ease`)

Animation:
* Like transitions, animations affect CSS properties and transformations 
* The difference being that in animations you specify *keyframes* a construct that enables changing values anywhere within the animation
* `@keyframes fadeout{from{opacity:1; to {opacity:0;}}`
, transitions and animations:

(translate, scale, rotate, skew, and 3-D perspective transitions and animations)
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
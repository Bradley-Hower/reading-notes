# *Course 201, Entry 1: Setup Developer Toolbelt*

## Components of a Web Page

Websites are probably the funnest part of the internet. But, in a basic sense, how do they work.

### HTTP - A Poem

The lights come on, the browswer comes up,
But what shall I do today? Yes, what?

I want to go to my favorite website,
but how does my computer know where to go?

My internet service provider has a set DNS server inside,
there it will find, readmymind... .com
This is how it will know where to go.

The name of the site isn't enough, as HTTP uses numbers,
that is where the DNS server works wonders.

It pulls up my site's IP address. And shortly I can see,
my favorite website via transer protocols HTTP and ICP/IP.

TCP/IP is the outer most wrapper,
and inside is the HTTP, looking all dapper.

Once my favorite site's server say "200 OK",
All the beautiful data packets, small chunks, of the website files,
are on their way.

My browser receives them,
ney, it needs them,
to display my favorite site.

### Parsing of HTML, CS, and JS Files

Firstly, the browers parses an HTML file. After running through, it will find any link elements refrencing CSS files and any script elements referencing any JavaScript.

Knowing that there are CSS and JavaScript files, the brower then request those from the server.

The browser then starts generating structures. The browser generates an in-memory DOM tree from the HTML and a CSSOM structure from the CSS files. Lastly, any JavaScript is compiled and executed.

In building this DOM tree with CSS styles and JavaScript scripts, an ouput is created on the user's screen.

### Finding Images to Add to a Website

When adding images to a website, it is important to be complied with copyright laws. To be in compliance, an easy way is to search for images using a *Creative Commons Licensed* search option. This is something which is available on Google.

### String vs Numbers

To create a string in JavaScript, text needs to be in quotes or apostrophies, preferrably apostrophies when possible.

To enter a number, a numerical digit is the choice. No quotes necessary.

### Variables

Variables are how information is stored as **values**. The are important to JavaScript because this is how information is processed. It is what allows lots of data manipulation to take place. The following example is when a variable is declared, a name for the variable set and assigned, a value assigned thereto. The keyword used here is `let`. This is a temporary variable which can have the value updated. The other keyword option is `const`, which does not allow a value update.


```
let dog = 12
```

## Parts of HTML

HTML, or HyperText Markup Language, is composed of **elements** and **attributes**.

### Elements

An **element** has four main components. The *opening tag*, the *content* and the *closing tag*. Unlike some other coding languages, tags can not be invented. They are set by the version of the language. In the year 2023, that is HTML5.

For the *opening tag*, there is an opening angle bracket, the element name, lastly, the closing bracket.

A *closing tag* similarly consists of an opening angle bracket, a forward slash, the element name, and the closing bracket. Note, some elements do not have closing brackets; *image* is an example. These are known as void elements. If there is no closing tag, special attention should be paid. There is likely something else that is different about that element too. Image elements, for example, have a forward slash just before the closing bracket.

![HTML Element Illustrated](https://raw.githubusercontent.com/Bradley-Hower/reading-notes/main/element-structure.png)[^1]

[^1][^2][source: [https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)]

### Attributes

Living within the opening tag of the element is the **attribute**, which holds information to be used by that element. Similarly, as with elements, a coder should be mindful of the elemnt within which the attribute lives. The attribute should make sense within the context of that element. For example, it may be the case that CSS would be better suited, rather than modifying with an attribute. The basic structure of an attribute constists of the attribute name, separated by a space from the element name, immediately followed by `=` and then followed by the attribute value, wrapped in quotes.

![HTML Atttribute Illustrated](https://raw.githubusercontent.com/Bradley-Hower/reading-notes/main/attribute-structure.png)[^2]

## HTML Tags

### Difference Between <article> and <section>

Article and section are similar in their functionality. They used to hold content. However, `<section>` is moreso used to hold subparts of a webpage. The `<article>` element is moreso used to hold information which can stand on its own and still make sense.

### Typical Elements of a Website

A website typically consists of the following:

#### Header
The top-most bar which sits at the top of a page. Typically holds the logo, a search bar, and perhaps a few other key navigation buttions.

#### Navigation Bar
This functions much like the index of the website. It is the modd by which a user can easily move around to other pages. A lot of times navigations are organized into menus and submenus. In more recent years, there has been a vast simplification of navigations for ease-of-use for users. 

#### Main Content
This is what the user came for. Entertainment and information. Article texts, images and videos are placed here.

#### Sidebar
Not as common anymore, but this holds information which might be useful to the user or that the website wants the user to know. Many designers find that a sidebar which is not a navigation bar, should not be used. Context is key.

#### Footer
This sectin normally holds the site index, legal information, copyrights, and conact information.

## Metadata

### Character Encoding

This is the character sets used for text on the page. By specifying the character set to pull from an operating system, the browser can actually display the text.

### Name and Content - Search Engine Optimization

Specifies content name and the actual content. The purpose here is to describe the page in some way. This is the information that will show up in search engine search. Think of it as headings and subheading describers of a website. By constructing this content according to a target audiance, a website can optimize its search performance.

### Logos

Other entries that might be inluded using meta tags are logos and icons. These can be of various sizes, thus to match the viewing screen and application. For example, if a link is referenced on anther site, like Facebook, Facebook can pull the appropriate local and thus enhance the user experience.

## Staring a Website

To start to build a website, there must be a "why" in place. The key factor here is what is the goal. A website doesn't just exist for its own purpose (at least it shouldn't). And a website should not be haphazzardly put together without a clear goal in mind. First principles dictates that one must start with the basics and then fill out the technical details. The seond step is determining how a website can best be used to the fulfill that goal. Entertain others? Content-focused creation. Solve a problem for others through a product? Webstore.

## Semantics

### <h1> vs <span>

Semantical elements are what give elements their role and meaning within a web page. Browser will treat these elements accordingly. So between `<h1>` and `<span>`, the browser will automatically size the prior as a heading, while the latter is relative and dependent on other elements of a page.

This is the advantage of semantic elements. Semantic elements take away the relative factor of an element. It also adds readability for the coder.


## What Requires JavaScript?

There are two things that require JavaScript. Storing values and APIs.

Storing values - By storing input values from the user, the webpage becomes dynamic. This greatly increases the interactivity of a page. It also greatly increases what can be done. 

### APIs

APIs or Application Programming Interfaces, are the plug-and-play of a webpage. APIs are what allow other mapped data inputs, applications and more.

#### Browser APIs - Information pulled from browser environment

+DOM (Document Object Model) - the top level organizer of HTML and CSS
+Geolocation - provides GPS and IP address.
+Canvas and WebGL - 2D and 3D graphics.
+Audio and Video - Video feed. Web camera, microphone inputs.
	
#### Third-party APIs - Code from Other Sites
+Examples:
+Twitter feed
+Maps
+Analytics
	

## Adding JavaScript

To add JavaScript to a web page, the code can either be internal to the HTML document, or it can be external as a JavaScript file. Considerationg to stage of interpretation should be given. Referring to code which has not been loaded in will generate errors.

### Internal

To add internally, the JavaScript code can be inserted inbetween two script element tags.

```
<script>
     alert("Hello World");
</script>
```

### External

For adding externally, there are two components. The first is the line referrencing the source JavaScript file. The second is the JavaScript file itself.


#### HTML File

The following line of script is normally found in the head section of the HTML file.

```
<script src="script.js"></script>
```

##### JavaScript File

```
alert("Hello World");
```

#### Location Inserts

Note, by cleverly writing JavaScript code to also contain HTML therewithin, JavaScript can be targeted within an HTML page by containing a JavaScript function call within script elements. Here is an example:

```
<script>
  visitorstatus()
</script>
```

## Things I want to know more about
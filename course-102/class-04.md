# *Course 102, Entry 4: Structure web pages with HTML*

## Wireframe - Structuring a Web Page

### Design Principles

To begin designing a website, we first need to know what the main structure of the website will be. It is desirable for a website to be easy to use. To accomplish this goal, the design of the site needs to be constructed in a way that allows for that ease of use. However, it is difficult to solve problems with lots of pieces and complexity. This is where wireframing comes in. Reducing a web page to the most basic principles, the problem becomes much more manageable. How to start?

### UX - How the User Interacts

To set up a well-designed wireframe, it is important to know how the layout will be interacted with by the user. This interaction is very contextual, and can be significantly influenced by the audience and where that audience is coming from. There are prevailing UX trends and well-guided best practices, but if the designer wishes to really optimize the design, it becomes imperative to dig deeper and do user analysis - to see how users are actually using the interface. That is not the point here though. The point of bringing it up is to understand that design matters and it should be very intentional. Going deeper is for another time.

Once there is an idea of how the web page will be interacted with, it is important to use these pearls of wisdom when laying the wireframing. Know the directions the users' eyes will be drawn. Prioritize areas of the page accordingly.

### Draw

Now with a general philosophy in mind, it is time to lay the wiring. There are many ways to do so, software and traditional.

**Software**

+ InVision (most popular)
+ Wireframe.cc
+ UXPin
+ Google Draw

**Traditional**

+ Pen and Paper (works great!)
+ Whiteboard
+ Paper, marker pens, and Scissors

Manipulate, modify, and repeat. This is the fun part. Looking at what others have done (especially in the intended industry) can offer a lot of insight too.

### Iterate

After designing it is important to test and see what works. Do users intuitively understand how to navigate and use what has been created? This is where reality butts heads with vision. It is important to try to get to this stage sooner rather than later. Hence the reason for doing it at the wireframe stage before time is wasted putting in the graphical finishing touches. Iterating a number of times until a comfortable state is found is critical.

## Translating to Code

The map is set. Beautiful. Now to set it with real building materials. The code  which makes up the majority of a web page is HTML and CSS. This article's scope is within the HTML realm. HTML is the best way to set the framing for our web page. CSS can be found in another reading notes entry.

### The Components of HTML

HTML, or HyperText Markup Language, is composed of **elements** and **attributes**.

#### Element

An **element** has four main components. The *opening tag*, the *content* and the *closing tag*. Unlike some other coding languages, tags can not be invented. They are set by the version of the language. In the year 2023, that is HTML5.

For the *opening tag*, there is an opening angle bracket, the element name, lastly, the closing bracket.

A *closing tag* similarly consists of an opening angle bracket, a forward slash, the element name, and the closing bracket. Note, some elements do not have closing brackets; *image* is an example. These are known as void elements. If there is no closing tag, special attention should be paid. There is likely something else that is different about that element too. Image elements, for example, have a forward slash just before the closing bracket.

![HTML Element Illustrated](https://github.com/Bradley-Hower/reading-notes/assets/139923955/6eff7162-68fd-4e4d-9ed8-e2d65dc5a57f)[^1]

[^1]: <sub>Image source:[https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)</sub> 

Note, when selecting an element, the coder should be mindful of semantics. That is to say, what is the meaning of the element and its intended use? For describing a figure, the "figure" element would make the most sense. Likewise, for a paragraph, the "paragraph" element. For things that would exist within the header, "header". And so forth. Context of use is important. The more contextual the meaning can be, the more semantic the element is. An element that is not semantic is the "div" element. It is purely functional.

#### Attribute

Living within the opening tag of the element is the **attribute**. Similarly, as with elements, a coder should be mindful of the elemnt within which the attribute lives. The attribute should make sense within the context of that element. It may be the case that CSS would be better suited, rather than modifying with an attribute.

![HTML Atttribute Illustrated](https://github.com/Bradley-Hower/reading-notes/assets/139923955/78f4e8d0-ff74-4d47-8931-97ac30c0baeb)[^2]

[^2]: <sub>Image source:[[HTML Atttribute Illustrated](https://github.com/Bradley-Hower/reading-notes/assets/139923955/78f4e8d0-ff74-4d47-8931-97ac30c0baeb)](https://github.com/Bradley-Hower/reading-notes/assets/139923955/78f4e8d0-ff74-4d47-8931-97ac30c0baeb)</sub> 

#### Nesting

Elements need to be nested. Do not commingle. Close an element with a closing tag once their song has been sung. If an element exists within another element's zone, no problem. For example, everything lives within the HTML element. The last closing tag for a page should be the HTML element closing tag. If you are making a list of dogs, a poodle is a list item of a type of dog. Thus, the list would not close prior to the poodle. The list would only close once all the dogs to be listed, have been listed.

### Basic HTML Page Structure

A HTML page consists of a few major elements, in the following order:

```
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width">
        <title></title>
    </head>
    <body>
    <header></header>
    <footer></footer>
    </body>
</html>
```

### Markup Elements

For basic writeup, one can use the following tags:

```
<h1></h1> - Largest heading.
<h2></h2> - Second largest heading.
<h3></h3> - Second smallest heading.
<h4></h4> - Smallest heading.

<ul> - Unordered list opening tag.
  <li>Poodle</li> - Unordered list List Item.
  <li>Labrador</li> - Unordered list List Item.
</ul>
```

### Links

For links, use the `<a></a>` element, also known as the anchor element. Spaced between the a' of the opening tag and the closing bracket of the opening tag, the intended URL should appear, per the following example. The text between the opening and closing tags will be the openable link.

`<a href="https://github.com">GitHub</a>`

[^1][^2]: <sub>Image source:[https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)</sub>

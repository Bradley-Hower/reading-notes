# *Course 102, Entry 5: Design web pages with CSS*

## CSS

Cascading Style Sheets (CSS) is what adds beauty to the framework set by HTML. With CSS, color and styling can be added. Things such as font size, font, border, backgrounds, margins, etc can now be added.

CSS sets what are, basically, rules for how the browser should treat the elements in HTML. However, just like any rules, they can be interpreted differently. Different browsers will interpret some instructions in unequal ways.

Nonetheless, rules are important. How are these rules written? 

CSS is formatted with a **selector** (that to which the rules apply), it then encompasses curly brackets with **declarations** (the rules), which consist of various **properties** and the **values** attached to them. Note, multiple elements can be selected as selectors. Also, subelements can be specified. Every selector just needs to be separated with a space.

### Example:

```
p {
  color: red;
  font-size: 5em;
}
```

In the above example, the selector is `p` elements. The declarations are inside the curly brackets, which consist of color and font-size properties and the values of "red" and "5em", respectively.

[MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) is a great reference for various CSS properties.

[W3 Schools](https://www.w3schools.com/css/default.asp) is another great resource.

There are three ways to apply CSS code to an HTML document. Internal, External, and Inline.

## Adding Internally

To add **Internally**, one can just use the above-referenced formatting and add it to the head of an HTML document.

## Adding Externally

Pulling **Externally** from a document can be done by saving a .css file with CSS added therewithin using the formatting mentioned in the example above. To have the CSS added to an HTML document, the following coding needs to be added to the head of the HTML document.

```
<link rel="stylesheet" href="styles.css" />
```

The "link" tag of the code tells the browser to pull in a document. The "rel" portion declares that this CSS code being pulled in will be known as "stylesheet". And finally, the "href" tells the browser where to find the CSS document (if in another directory) and what the name of the file is.

## Add Inline

The last way to add CSS is **Inline**. This method should be avoided when possible though as it easily makes an HTML page very dirty.

To add CSS inline, simply add a "style" attribute. Within the style attribute are the declaration, formatted just as in the example mentioned earlier in this article.

```
<p style="color: red; font-size: 5em;">Color me red.</p>
```
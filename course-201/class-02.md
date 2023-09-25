# *Course 201, Entry 2: Basics of HTML, CSS & JS*

## HTML Text Fundamentals and Formatting

How web pages are formatted is important. It is what gives structure to the page. It also gives much-needed context for us all, including machines.

### Using Semantic Elements in HTML

**Semantics** allow the context of content to be easily understood. It allows the user's browser to know how to interpret a given element. Moreover, it allows for search engine optimization and improves accessibility for disabled folks who are using screen readers.

### HTML Headings Levels
There are six levels of heading elements in HTML, starting with `<h1>`. Each subsequent level is of the same formatting, but with a single increase in number, all the way up to `<h6>`.

### Uses of `sup` and `sub` Elements

To write superscript and subscript text, use the `<sup>` and `<sub>` elements, respectively. Some great uses of this are for writing out chemical formulas and mathematical logs and exponents.


### Using the `abbr` element
To use the abbreviation element, there must also be the title attribute. Here is an example:

```
<abbr title="National Science Foundation">NSF</abbr>
```
attribute which must be added to provide the full expansion of the term

## CSS
CSS is the component which gives our page some style. What are the ways we implement CSS?

### Ways we can Apply CSS to our HTML

CSS can be applied via an external stylesheet, internal stylesheet, or inline code.

```
p {
  color: red;
  font-size: 5em;
}
```

To add **Internally**, one can just use the above-referenced formatting and add it to the head of an HTML document.

Pulling **Externally** from a document can be done by saving a .css file with CSS added therewithin using the formatting mentioned in the example above. To have the CSS added to an HTML document, the following coding needs to be added to the head of the HTML document.

```
<link rel="stylesheet" href="styles.css" />
```

The last way to add CSS is **Inline**. To add CSS inline, simply add a "style" attribute. Within the style attribute are the declaration, formatted just as in the example mentioned earlier in this article.

```
<p style="color: red; font-size: 5em;">Color me red.</p>
```

### Avoid Using Inline Styles

This method should be avoided when possible though as it easily makes an HTML page very dirty. It is difficult to update and unnecessarily challenging to read.


### Example:

```
h2 {
    color: black;
    padding: 5px;
  }
```

>What is representing the selector?

The text "h2" is the selector.

>Which components are the CSS declarations?

Declarations are what make changes to elements. Declarations are composed of properties and their corresponding values.

>Which components are considered properties?

These are the targeted identifiers which give the elements different features. They are quite sensible. For example, "padding" adds padding, "width" defines the width.

## JS

JavaScript is very powerful. It adds a lot more capabilities to our websites via a number of ways, including inputs and functions.

### Single Quotation Marks?
The data type which is held within single quotation marks, or apostrophes, are strings.

### JavaScript operators
Here are four types of JavaScript operators: addition (also used for concatenation) `+`, assignment `=`, strict equality `===`, and subtraction, multiplication and division, `-`, `*`, `/`.

### Solutions via Function
Here is an example of a real-world problem you could solve with a function. Let's say you want to convert a measurement of inches to feet and inches, a function could do that.


### Conditional Statements

>An if statement checks a __ and if it evaluates to ___, then the code block will execute.

If statements check a boolean. If the boolean evaluates to "True", the code block executes.

>What is the use of an else if?

The purpose of the "else if" statement is to run more than two possible scenarios. From there, a tree of scenarios can be run with corresponding processing.

>List 3 different types of comparison operators.

 There are three comparison operators. They are:

`===` identical, `!===` not identical

`<` less than `>` greater than

`<=` less than or equal to `>=` greater than or equal to

>What is the difference between the logical operator `&&` and `||`?

The use of `&&` is to chain together multiple expressions. This allows the coder to avoid typing out a bunch "else if" statements, and instead group them as one. The `||` is used to chain two more expressions, however, unlike `&&` where all need to result in "True", for the use of `||`, only one needs to be true.

## Things I want to know more about

Learning more advanced JavaScript code is what I am looking forward to. Learning about the `calc()` function option for CSS was great. That is something I have been wondering.

# *Course 201, Entry 4: HTML Links, JS Functions, and Intro to CSS Layout*

## Hyperlinnks

It is important to understand the full functionality of hyperlinks and best practices for implementation, especially given how fundamental and useful hyperlinks are.

### Creating a Basic Link

To create a link, the anchor `<a>` element is used. Herein, the `href` attribute (HyperText Reference) sits, holding the target URL (Uniform Resource Locator)/web address.


### Link Accessibility

To improve accessibility, including title link tags can be helpful, especially for navigation links. The title attribute holds text, typically regarding the link's purpose or other relevant information regarding. Moreover, the link itself should be self-descriptive in some regards. This vastly helps screen reader software work properly.

Example:
```
<a href="https://developer.mozilla.org/en-US/" title="Mozilla's web developer documentation home page.">
```

## CSS Layout
CSS layout is what dictates how elements will be placed within a page. Proper usage of positioning and display properties allows for great layout control.

### Normal Flow

Normal flow is the way by which elements are placed one after another inside the browser viewport. Block-level elements have a block flow. Meaning, each element will appear on a new line, stacked like building blocks, vertically. Conversely, inline elements don't appear on new lines. They sit side-by-side, like English text, carrying over to the next line once the current one is full. Thus, inline elements stack horizontally within the viewport.

### Positioning
Positioning allows for normal document flow (default flow) to be overridden. The default positioning for every HTML element is **static positioning**.

#### Relative Positioning

**Relative positioning** is similar to static positioning, except it can be tweaked. The position is modified via `top`, `bottom`, `left`, and `right` property tags. In relative positing, these position tags act as "bumps" in a given direction.

#### Absolute Positioning

**Absolute positioning** removes the element from the rest of the page. Think of it as being on its own layer. Any positioning tags (`top`, `bottom`, `left`, and `right`) will now act according to the containing element. And remember, there is always a containing element, even if it is the `<html>` tags. This containing element is known as the **initial containing block**. By changing where the element is located within the HTML document relative to other element tags, the **positing context** is changed. The advantages of absolute positioning are that there is a lot more control over where the element goes. It keeps elements within containers but allows for more control within those containers. Moreover, layering can occur. How? Other elements ignore an absolutes existance. They do not move relative to it as they treat it as being on another layer.

#### Fixed Positioning

**Fixed positioning** is similar to absolute positioning, except that it is based on the viewport (exception: ancestor element has modified transform property). By having a fixed positioning, the element takes a dominant purpose, always staying in view.

#### Overlapping - Setting Order

Once there is a layering of elements, it might be difficult to otherwise change how they are layered, apart from changing the order they are written in the HTML. If there is no other straightforward option, **z-index** is a hero. It sets order on the Z-axis (going into the screen).

#### Sticky Positioning

This one is unique. **Sticky positioning** acts with relative positioning, until scrolling reaches a certain position, at which point, it becomes fixed.

## JS - Reusing Blocks

Code is best used when it can be reused. Functions allow just that. When writing a function and defining its parts, this is **declaration**. When the function is called into action, to work, to execute code, this is **invocation**.

Within some functions, within the parentheses of the function, values can be fed it. These are defined as **parameters**. Once the values are fed into the function through execution and performing duties, they then become known as **arguments**.

## Pair Programming

Among the reasons listed, "**greater efficiency**" and "**engaged collaboration**" are my favorite reasons for pair programming.

I think being able to solve a problem together with a co-worker can be very fruitful, allowing for a mastermind to work. People can become in sync and really get a lot of work done, filling in each other's gaps of perception or understanding. Without someone there to assist in the gaps, it can take one much more time to keep going, with more errors or misconceptions likely to occur.

And by working together as a mastermind, a rapid exchange of ideas can occur, as they come to mind. Being that they occur right within the context of relevance, it boosts productivity in communication.

## Things I want to Learn more About

Understanding how each browser differs in its interpretation of CSS I think would be really helpful to know. It would allow me to know how to avoid writing code that alienates people. I do acknowledge that the CSS reset helps cut out a lot of differences.

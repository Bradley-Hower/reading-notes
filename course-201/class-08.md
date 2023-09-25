# *Course 201, Entry 8: CSS Layout*

## Flexbox

### One-dimensional

When flexbox `flex-wrap`  is set to `wrap`, it will create new **flex lines** for the content items (when set to "nowrap" - as by default, the content will overflow). Flex lines are independent of other flex lines. This demonstrates itself in alignment. Alignment is applied independently. Thus an item on line two can not be set to align with an item on line one. This is what is meant when it is said that flexbox is one-dimensional. Only one axis can be controlled. Either horizontally or vertically. Horizontally is within a line, and vertically is between lines.

These two axes have two names. The **main axis** and the **cross axis**. The main is left to write content placement. The cross axis is top to bottom content placement. However, this is dependent on set writing directions which are language dependent.

### Direction

The direction of content can be overridden with the following values for `flex-direction`:

+ row
+ row-reverse
+ column
+ column-reverse

Thus, main axis content can be placed vertically, but still use justify for the alignment. See alignment further down.

### Content Spacing

Content can be spaced from three primary properties, `flex-grow`, `flex-shrink`, and `flex-basis`. 

Grow - Enlargement of items on expansion of window.
Shrink - Shrink of items on contraction of the window.
Basis - On auto, sets content sizes to where they all fit and match. Alternatively, size can be set.

And while these each can be custom modified, it makes more sense to use the encompassing property `flex` to select each of these to a preset. Moreover, using `flex` passes these properties to children elements. 

The value options are:

+ initial - Grow: no. Shrink: yes. Basis: auto.
+ auto - Grow: yes. Shrink: yes. Basis: auto.
+ 1 - Grow: yes. Shrink: yes. Basis: no.
+ none - Grow: no. Shrink: no. Basis: no.

### Alignment

There are two main categories of properties for alignment:

justify-... - main axis

align-... - cross axis

The next subcategories for these are to which they apply:

...-self - this element

...-items - this element and all of its children

The values that can be attached to these are:

+ stretch - content fills its flex line space. (align only)
+ start - pushes item to the start of the axis.
+ end - pushes items to the end of the axis.
+ center - aligns all items to the middle center.

### Space

Space along the main and cross access can be set with the shorthand `place-content`. The first value is for the main axis, the second value is for the cross axis.

The values that can be attached to these are:

+ stretch - content fills its flex line space. (cross axis only)
+ start - pushes item to the start of the axis.
+ end - pushes items to the end of the axis.
+ center - aligns all items to the middle center.
+ space-around - puts an even amount of space between items, and half space on the far ends.
+ space-between - puts an even amount of space between items, no space on the far ends.
+ space-evenly - puts an even amount of space between items and on the far ends.

### Accessibility

While flexbox has many capabilities for modification, accessibility should be kept in mind. Screen readers will work according to the DOM, in other words, how the HTML is set up. So while content order and alignment can be changed, one should keep in mind the effects for accessibility. If the content flow is different from the HTML, then change the HTML. For this reason, the `order` property should be avoided.

## Why Flexbox

Flexbox overcomes the following issues that arise with using floats and positioning.

+ Vertically centering
+ Items taking up equal amounts of space in all contexts
+ Eveness across columns, regardless of content differences therein

## Longer Term

Using flexbox allows for a lot of flexibility in various scenarios, thus allowing a coder to have a handy tool at hand. This is certainly one I will keep in mind.

## Things I want to Know More About

Grids. I am seeing that is another option. Not sure if I will use it, but it would be good to at least understand what it does.
# *Course 201, Entry 9: Forms and JS Events*

## Web Forms

**Web forms** are one of the most important aspects of web commerce. They allow users to submit information in a standardized way which can then be stored in a database with data tags. Moreover, they allow for a safe and predictable standard of interaction with users and websites. Web forms are comprised of **form controls** and **HTML forms**. These form controls come in the form of text fields, dropdown boxes, buttons, checkboxes, or radio buttons.

To help facilitate forms are properly completed, **form  validation** can be implemented.

Some forms elements are:

1. form - sets the stage for the form. Defines where data should be pulled or sent via get and post respectively. The `action` attribute defines the location the `method` defines if it will be via get or post.

2. label - indicates a new field. Takes the descriptive name displayed to the user and tags it to the input field. Useful for accessibility. Mapped to input field vis `for` attributed.

3. input - the location for data entry via the determined `type` attribute. Data is tagged with a `name` attribute for the server later. A label element is tied to input via `id` attribute.

4. textarea - a special type of text input. Unlike "input", not a void element.

5. button - has three different `type` attribute options. Submit, reset, or button. "Button" is customizable.


Some form elements to improve accessibility are:

1. fieldset - groups a bunch of input fields together. Used for styling and semantics.
2. legend - categorically describes options. For screen readers, states lengend and label text. Repeats for each label.

To improve accessibility, use the following structure for form inputs. This improves screen reader usability. 

```
<div>
  <label for="username">Name: <span aria-label="required">*</span></label>
  <input id="username" type="text" name="username" required />
</div>
```

## Events

**Events** are a way for the computer to trigger some code upon a certain action of the user. Some basic cases are mouse clicks, hover-over items, keystrokes, form submission, and video playback.

### Event Listeners

**Event handlers/event listeners** are registered upon creation by  coder. To run an event listener, the coder must put in the event, followed by the function to run. This follows the following syntax:

```
btn.addEventListener("click", () => {
});
```

In the above, "click" can be replaced with the event being listened for. 

### Event Objects

Within the code block of the event listener can be some helper code which passes extra information or functionality; this parameter is called an **event object**. The syntax of an even object starts with `event`, `evt`, or `e`. Following, `target` will specify where the event object code will apply to. This is important as it allows for a specific dynamic response.

Example:

```
const btn = document.querySelector("button");

function bgChange(e) {
  const rndCol = `rgb(${random(255)}, ${random(255)}, ${random(255)})`;
  e.target.style.backgroundColor = rndCol;
  console.log(e);
}

btn.addEventListener("click", bgChange);
```

In the preceding code, the event is the changing of the background and the target would be where the click occurred. In this case, as indicated by `btn` in the function call code.

### Event Bubbling

Event listeners can sit within nested elements. If it is desired, an event listener can be set to trigger at multiple element layers and the message be passed up the chain. This passing up of the event is called **event bubbling**.

A way to stop this midway is via `stopPropagation()`.

### Event Capturing

**Event capture** is like event bubbling, but in reverse order. The event triggers from higher-order elements and works its way down.
What is the difference between event bubbling and event capturing?

## Things I Want to Know More About

How input elements are exploited. 

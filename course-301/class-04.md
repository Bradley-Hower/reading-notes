# *Course 301, Entry 4: React and Forms*

## Forms

In a form, when a input element is used, the value is managed by React. These elements are thus considered “controlled component”.

There is a great advatage of storing the user inputs prior to submission. This allows the user to come back to the form and continue where they left off if they happen to get pullled away for some reason. This greatly improves the user experience, especially if the form is necessarily tedious.

### Targeting User Keystroke Inputs

To target the user inputs on the input field using an event handler, the "onChange" attribute is used.

Example from [https://legacy.reactjs.org/docs/forms.html](https://legacy.reactjs.org/docs/forms.html)

```
class EssayForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: 'Please write an essay about your favorite DOM element.'
    };

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('An essay was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Essay:
          <textarea value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```
## The Conditional (Ternary) Operator

The Ternary Operator is a very convenient syntax to the if statements. These two snippets of code are functionly equivalent.

```
if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}
```

```
person.driver = person.age >=16 ? 'Yes' : 'No';
```

### Nested Ternary Statements

To add multiple tests, follow the following syntax:

```
let isStudent = false;
let isSenior = true;
let price = isStudent ? 8 : isSenior ? 6 : 10
console.log(price);
// 6
```

### Multiple Operations

Using a ternary, multiple operations can be run on an outcome. Each operation needs to be seperated with a comma. Parenthesis optionally can be use to contain the two greoups of potential outcomes  (if evaluates to true or false).

let isStudent = true;
let price = 12;

isStudent ? (
  price = 8,
  alert('Please check for student ID')
) : (
  alert('Enjoy the movie')
);

## Why Use the Ternary Operator?

In simple use cases, the ternary operator is much easier to read. This lends well when a lot is going on.

### Example

Using traditional syntax:

```
if(x===y){
  console.log(true);
} else {
  console.log(false);
}
```

Using ternary syntax:

```
x===y ? console.log(true) : console.log(false)

```

## Things I want to know more about

"this.handleLogoutClick = this.handleLogoutClick.bind(this);"

I need to read into more as to how this works the cases for when to use it.

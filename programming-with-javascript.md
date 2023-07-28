# *Course 102, Entry 7: Programming with JavaScript*

## Control Flow

**Control flow** is the order in which code is executed. A computer's flow starts off being from top to bottom, but will change what is read and where if it comes across specific commands. This happens a lot.

A simple example of a switch would be an if-else (conditional statement). Once the first line of the conditional is met, the next options are irrelevant. Thus, the computer can skip the next lines in the conditional statement and move on.

## JavaScript Functions

### Components of a Function Definition

In JavaScript, a **function** is a block of code that is set to run certain, **localized** (within the block), code **statements**.

Calling a function, or **invoking** it, is to execute a function.

A function is composed of the **keyword**, the **name** of the function, the **parameters** which are within parentheses (dependent on the function workings), each separated by commas, and then the lines of code, **statements**, within curly brackets.

Functions, like other code, can also be assigned to variables. However, when assigning, there are some important considerations. Remember, when defining a variable in JavaScript, either `let` or `const` needs to be used. There are workarounds to this though, such as creating a new variable within HTML instead.

![function components](function_components.png)

Another important part of a function is the **return** statement. The return statement is written within the code curly brackets; It is what allows code to exit the function and continue to be used elsewhere.

### Components of a Call Function Command

If the function is to be invoked, the function name must be typed out followed by open and closed parenthesis. The open and closed parentheses together are known as the **operator**. Without the operator, one is just calling the object. If the function by definition has parameter components, then **values** need to be fed into the function, replacing the places of the parameters. Once the values enter the function into the lines of code, these values are then known as **arguments**. The discerning difference between parameters and arguments is that parameters are in the function definition, while arguments are values that have entered the statements when the function is being called.

Functions have a lot of neat uses. And while they aren't mandatory to execute code, they make it a whole lot easier and more useful. The key advantage of computers is their efficiency. Less code can be used and code can be repurposed.

## JavaScript Operators

### Arithmetic Operators

    Operator	Description
	    +	Addition
    	-	Subtraction
	    *	Multiplication
	    **	Exponentiation (ES2016)
	    /	Division
	    %	Modulus (Division Remainder)
	    ++	Increment
	    --	Decrement

Note, increment and decrement operators will still work in a loop, even if entered into console.log command.

### Assignment Operators
    Operator	Example	    Same As
        =		x = y	    x = y
        +=		x += y	    x = x + y
        -=		x -= y	    x = x - y
        *=		x *= y	    x = x * y
        /=		x /= y	    x = x / y
        %=		x %= y	    x = x % y
        **=		x **= y	    x = x ** y

### Comparison Operators
    Operator	Description
        ==	    equal to
        ===	    equal value and equal type
        !=	    not equal
        !==	    not equal value or not equal type
        >	    greater than
        <	    less than
        >=	    greater than or equal to
        <=	    less than or equal to
        ?	    ternary operator

### Logical Operators
    Operator	Description
        &&	    logical and
        ||	    logical or
        !	    logical not

### Type Operators
    Operator	    Description
    typeof		    Returns the type of a variable
    instanceof	    Returns true if an object is an instance of an object type

### Bitwise Operators
    Operator	Description			    Example		Same as			Result	Decimal
    &		    AND						5 & 1		0101 & 0001		0001	 1
    |		    OR						5 | 1		0101 | 0001		0101	 5
    ~		    NOT						~ 5	 		~0101			1010	 10
    ^		    XOR						5 ^ 1		0101 ^ 0001		0100	 4
    <<		    left shift				5 << 1		0101 << 1		1010	 10
    >>		    right shift				5 >> 1		0101 >> 1		0010	  2
    >>>		    unsigned right shift	5 >>> 1		0101 >>> 1		0010	  2

#### Bitwise Operators Explained

    Operator	    Name	                Description
            &	    AND		                Sets each bit to 1 if both bits are 1
            |	    OR		                Sets each bit to 1 if one of two bits is 1
            ^	    XOR		                Sets each bit to 1 if only one of two bits is 1
            ~	    NOT		                Inverts all the bits
            <<	    Zero fill left shift	Shifts left by pushing zeros in from the right and let the leftmost bits fall off
            >>	    Signed right shift	    Shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off
            >>>	    Zero fill right shift	Shifts right by pushing zeros in from the left, and let the rightmost bits fall off


See [W2 Schools](https://www.w3schools.com/js/js_bitwise.asp) for a more detailed explanation. 

### String Operators
    Operator	Example					Output Result
    +			text1 = "big" + "deal"	big deal
    +=			text1 = "no"
                text1 += "problem"		no problem

### Ternary Operators
    Syntax:
    condition ? val1 : val2

    If condition is True - val1
    If condition is False - val2

### Comma Operator
The comma operator is a rare one to use. But it can be useful when trying to run a loop with multiple variables at the same time. Don't use this otherwise, as two separate statements normally can be used.

Example: 

```
const x = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
const a = [x, x, x, x, x];

for (let i = 0, j = 9; i <= j; i++, j--) {
  //                              ^
  console.log(`a[${i}][${j}]= ${a[i][j]}`);
}
```

### Unary Operators
An operation with just one operand.

### Other Operators

Some other operators to be used later are `delete`, `void`, `in`, `this` `new`, and `super`.


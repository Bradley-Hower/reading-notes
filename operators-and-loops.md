# *Course 102, Entry 8: Operators and Loops*

## Expressions in JavaScript

What are **expressions**?

```
x = 11
```

Expressions are a way of representing something elase, such as a value. In the above, `x` can represent `11`. Expressions can be be created by **assignment**. However, expressions aren't always via proxy. Expressions sometime only evaluate. That is to say, the expression can simply be mathed out. Examples of this are an arithmatic problem or just a number itself.

In arithmatic problems there are different math signs, or operators. These operators must be done in order of operations, or **precedence**, as it's known in coding.

## While Loops

In **while loops**, a **condition** is taken into consideration if it is true or false. A condition is any logical expression which can be tested. If the condition is true, the statement within the block is executed. The increment or decrement is then applied (if applicable). Increments and degrements are applied to argument values in an expression which is within the condition. Note, other more complex alterattins can occur, other than just an increment or decrement. The while loop function then runs again, **evaluating** the condition. The process repeats (without limit) until the condition runs false, at which point the loop will stop. 

![parts of while loop](placeholder)

**While Loop Example**

```
let j = -5
while (j <= 0){
  console.log(j);
j++
}

-5 <= 0 ? T | Execte code j = -4
-4 <= 0 ? T | Execte code j = -3
-3 <= 0 ? T | Execte code j = -2
-2 <= 0 ? T | Execte code j = -1
-1 <= 0 ? T | Execte code j = 0
 0 <= 0 ? T | Execte code j = 1
 1 <= 0 ? F | BREAK THE LOOP
```

**While Loop Diagram**

![while loop diagram](placeholder)

It is important to note, in JavaScript, any variables that are to be evaluated as part of a condition, must be declared and assigned outside of the while function. Within the loop, in the statements, variables can then be created or reassigned locally. This includeds any variables that will again be evaluated within the condition. Remeber that reassigning does not require declaration via a keyword.

## For Loops

**For loops** are similar to while loops, except that there is a predetermined number of loops that will run. With while loops, there could be repeat runs caused by user input. The parts of a for loop are the **initialization** or the set expression. This is likeunto a variable within a while loop.

The condition, like a while loop, is evaluated. If the condition is true, the loop statements execute and the **afterthought** is applied. The afterthought is like the increment or decrement, as mentioned in while loops. It too can be any alteration though.

![parts of for loop](placeholder)

**For Loop Example**

```
for (let i = 0; i <= 12; i = i +1){
  console.log(i*8);
}

 0 <= 12 ? T | Execte code i = 1
 1 <= 12 ? T | Execte code i = 2
 2 <= 12 ? T | Execte code i = 3
 3 <= 12 ? T | Execte code i = 4
 4 <= 12 ? T | Execte code i = 5
 5 <= 12 ? T | Execte code i = 6
 6 <= 12 ? T | Execte code i = 7
 7 <= 12 ? T | Execte code i = 8
 8 <= 12 ? T | Execte code i = 9
 9 <= 12 ? T | Execte code i = 10
10 <= 12 ? T | Execte code i = 11
11 <= 12 ? T | Execte code i = 12
12 <= 12 ? T | Execte code i = 13
13 <= 12 ? F | BREAK THE LOOP
```

**For Loop Diagram**

![for loop diagram](placeholder)


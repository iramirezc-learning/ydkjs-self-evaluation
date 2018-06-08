# Quiz - YDKJS: Up & Going 1/3

## Chapter 1. Into Programming

### Answer Sheet

#### Section: Code

---

##### What's a program?

> A set of instructions that tell a computer what to do.

##### What's a computer language?

> The rules of valid format and combinations of instructions. aka syntax. Just as the English language.

##### What's a variable?

> Variables are like simple boxes where you can store any of your stuff in.

##### What's a statement?

> A group of words, numbers, and operators that performs a specific task.
>
> Example: `a = b * 2;`

##### From the statement `a = b * 2` name its parts

> **variables**: a, b
>
> **literal values**: 2
>
> **operators**: =, *

##### What is an expression?

> An expression is any reference to a variable or value, or a set of variable(s) and value(s) combined with operators.

##### Name the expressions in the statement `a = b * 2`

> `b` is a variable expression
>
> `2` is a literal value expression
>
> `b * 2` is an arithmetic expression of multiplication
>
> `a = b * 2` is an assignment expression

##### What's the difference between `interpreted` and `compiled` code?

> Interpreted code is read on the fly, from top to bottom, line by line, execution happens immediately.
>
> Compiled code is when all the translation to commands happens first, then the program is executed.

##### Is JavaScript interpreted or compiled? Explain why

> The JavaScript engine actually compiles the program on the fly and then immediately runs the compiled code.

#### Section: Try It Yourself

---

##### Output

Consider:

`var a = 1;`

Write the code to:

1. print `a` in the __console__

> `console.log(a);`

2. show `a` in a __popup__

> `alert(a);`

##### Input

Code challenge:

Ask user's name with a __prompt__ message `"Please, type your username"` and store it in a variable `username`, then log the value in the console

> solution:

```js
var username = prompt('Please, type your username')
console.log(username)
```

#### Section: Operators

---

##### JavaScript has both u___ and b___ operators, and one special t___ operator

> unary, binary, ternary

##### Operators types

Name the _types of operators_ you know, and give some __basic__ examples.

> Assignment: `=`, `+=`, `-=`, `*=`, `/=`
> Comparison: `==`, `!=`, `===`, `!==`, `>`, `<`, `>=`, `<=`
> Arithmetic: `+`,`-`, `/`, `*`, `++`, `--`
> Logical: `&&`, `||`, `!`

#### Section: Values & Types

---

##### Name JavaScript built-in types aka as _primitive_ values

> number, string, boolean

##### What's coercion in JS?

> is when a values are converted to a different type, for example, converting a string to a number, or a number to string.

##### Explain the difference between `implicit` and `explicit` coercion in JS. Give examples

> implicit coercion is done automatically, example:

```js
var number = 10;
// number is converted to a string
console.log(number);
```

> explicit coercion is when __you want__ to convert values from one type to another, example:

```js
var number = 10;
// I want to convert number to a string
number = String(number);
// number is a string already, no need to converted
console.log(number)
```

#### Section: Code Comments

---

##### What are the two types of comments in JS? Give examples

> single-line:
> `// this is a single line comment`
>
> multiline:

```js
/* this is
 a multiline
 comment */
```

##### Why is it important to comment code?

> Comments describe the hows and whys of something implemented in code. They help to document things in a way other team members and your future self can understand better your code.
>
> Comments are one effective way to write more readable code.

#### Section Variables

---

##### Does JavaScript use Static or Weak typing?

> Weak typing

##### Describe `static typing` aka `type enforcement`

> Variables can hold only the type they are defined with, for example:
>
> `int number = 10`

##### Describe `weak typing` aka `dynamic typing`

> Variables can hold any type, for example:

```js
var a = 10;
a = 'Isaac'
```

##### Conventions to write constants in JS

> Constants are placed on top of a program
>
> Constants are capitalized separated with an underscore `_`, example: `TAX_RATE`
>
> Use keywork `const` only availble for ES6

#### Section: Blocks

---

##### Is this valid code in JS?

```js
var amount = 100;

{
  amount = amount * 2;
  console.log(amount)
}
```

> yes, it's called `general block`

#### Section: Conditionals

---

##### Write a block of code to validate if a variable `number` is less than `10` to log `one digit`, log `two digits` otherwise

> solution:

```js
if (number < 10) {
  console.log('one digit');
} else {
  console.log('two digits');
}
```

#### Section: Loops

---

##### Write a block of code to log numbers from `0-9` using `while`, `do-while` and `for` loops

> __While__ solution:

```js
var i = 0;
while(i <= 9) {
  console.log('number ->', i);
  i = i + 1;
};
```

> __Do-While__ solution:

```js
var i = 0;
do {
  console.log('number ->', i);
  i = i + 1;
} while(i <= 9)
```

> __For__ solution:

```js
for (var i = 0; i <= 9; i = i + 1) {
  console.log('number ->', i);
}
```

##### What are the three clauses of a `for` loop?

> initialization clause
>
> conditional test clause
>
> update clause

#### Section: Functions

---

##### What's a function?

> a named block of code that performs a specific task, it's called (executed) by its name

##### Write a function `sum` that receives two numbers as arguments and returns the sum of both

> solution:

```js
function sum (a, b) {
  return a + b;
}
```

##### What's `scope` in JS?

> a collection of variables as well as the rules for how those variables are accessed by name.

##### Answer `true` or `false` for the following statements

Consider:

```js
function outer() {
  var a = 1;

  function inner() {
    var b = 2;
  }

  inner();
}

outer();
```

###### Does the `inner` function have access to the `outer` function scope?

> true

###### Does the `outer` function have access to the `inner` function scope?

> false

#### Section: Challenges

---

##### 1.1 Create a function `calculateAreaOfACircle` that receives `radius` as parameter. Use a constant `PI` equal to `3.14159`. _Avoid the temptation of using the `Math`library_

```js
// create a constat PI = 3.14159

// create your function here

// Do NOT touch this code.

console.log('Expect area of a circle with radius = "3" to be "28.27431" ->', calculateAreaOfACircle(3) == 28.27431)
```

> solution:

```js
const PI = 3.14159;

function calculateAreaOfACircle(r) {
  return PI * (r * r);
}
```

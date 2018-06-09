# Quiz - YDKJS: Up & Going 1/3

## Chapter 1: Into Programming

### Answer Sheet

#### Section: Code

---

##### 1. What's a program?

> _a set of instructions that tell a computer what to do._

##### 2. What's a computer language?

> _the rules of valid format and combinations of instructions. aka syntax. Just as the English language._

##### 3. What's a variable?

> _variables are like simple boxes where you can store any of your stuff in._

##### 4. What's a statement?

> _a group of words, numbers, and operators that performs a specific task._
>
> _example:_ `a = b * 2;`

##### 5. From the statement `a = b * 2` identify its parts _(literals, variables, operators)._

> _variables:_ `a`, `b`
>
> _literal values:_ `2`
>
> _operators:_ `=`, `*`

##### 6. What's an expression?

> _an expression is any reference to a variable or value, or a set of variable(s) and value(s) combined with operators._
>
> _example:_ `a * b`

##### 7. How many expressions can you indentify from the statement `a = b * 2;`?

> _4 expressions in total:_
>
> * `b` _is a variable expression_
>
> * `2` _is a literal value expression_
>
> * `b * 2` _is an arithmetic expression of multiplication_
>
> * `a = b * 2` _is an assignment expression_

##### 8. What's the difference between `interpreted` and `compiled` code?

> _interpreted code is read on the fly, from top to bottom, line by line, execution happens immediately._
>
> _compiled code is when all the translation to commands happens first, then the program is executed._

##### 9. Is JavaScript `interpreted` or `compiled`? Explain why.

> _the JavaScript engine actually compiles the program on the fly then immediately runs the compiled code._

#### Section: Try It Yourself

---

##### 10. Output Exercises.

Consider: `var a = 1;`

Write the code to:

###### 10.1. print `a` in the __console__

> `console.log(a);`

###### 10.2. show `a` in a __popup__

> `alert(a);`

##### 11. Input Exercises.

Code challenge:

Ask the user's name with a __prompt__ message `"Please, type your username"` and store it in a variable `username`, then log the value in the console.

Solution:

```js
var username = prompt('Please, type your username');
console.log(username);
```

#### Section: Operators

---

##### 12. Complete the sentence:

JavaScript has both u___ and b___ operators, and one special t___ operator

> _unary, binary, ternary_

##### 13. Operators types.

Name the _types of operators_ you know, and give some __basic__ examples.

> _assignment:_ `=`, `+=`, `-=`, `*=`, `/=`
>
> _comparison:_ `==`, `!=`, `===`, `!==`, `>`, `<`, `>=`, `<=`
>
> _arithmetic:_ `+`,`-`, `/`, `*`, `++`, `--`
>
> _logical:_ `&&`, `||`, `!`

#### Section: Values & Types

---

##### 14. Name JavaScript built-in types aka as _primitive_ values.

> _number, string, boolean_

##### 15. What's coercion in JS?

> _when values are converted to a different type, for example, converting a string to a number, or a number to string._

##### 16. Explain the difference between `implicit` and `explicit` coercion in JS. Give examples.

> _implicit coercion is done automatically_
>
> _example:_

```js
var number = 10;
// number is converted to a string
console.log(number);
```

> _explicit coercion is when __you want__ to convert values from one type to another_
>
> _example:_

```js
var number = 10;
// I want to convert number to a string
number = String(number);
// number is a string already, no need to converted
console.log(number)
```

#### Section: Code Comments

---

##### 17. What are the two types of comments in JS? Give examples.

> _single-line comment:_
>
> `// this is a single line comment`
>
> _multiline comment:_

```js
/* this is
 a multiline
 comment */
```

##### 18. Why is it important to comment code?

> _comments describe the hows and whys of something implemented in code. They help to document things in a way other team members and your future self can understand better your code._
>
> _comments are one effective way to write more readable code._

#### Section Variables

---

##### 19. Does JavaScript use Static or Weak typing?

> _weak typing_

##### 20. Describe `static typing` aka `type enforcement`.

> _variables can hold only the type they are defined with, for example:_
>
> `int number = 10`

##### 21. Describe `weak typing` aka `dynamic typing`.

> _variables can hold any type, for example:_

```js
var a = 10;
a = 'Isaac'
```

##### 22. Name some conventions to write constants in JS.

> _constants are placed on top of a program._
>
> _constants are capitalized separated with an underscore `_`, example: `TAX_RATE`_
>
> _use keywork `const` only availble for ES6._

#### Section: Blocks

---

##### 23. Is this valid code in JS?

```js
var amount = 100;

{
  amount = amount * 2;
  console.log(amount)
}
```

> _yes, it's called `general block`_

#### Section: Conditionals

---

##### 24. Write a block of code to validate if a variable `number` is less than `10` to log `one digit`, log `two digits` otherwise.

Solution:

```js
if (number < 10) {
  console.log('one digit');
} else {
  console.log('two digits');
}
```

#### Section: Loops

---

##### 25. Write a block of code to log numbers from `0-9` using `while`, `do-while` and `for` loops.

**`while`** solution:

```js
var i = 0;
while(i <= 9) {
  console.log('number ->', i);
  i = i + 1;
};
```

**`do-while`** solution:

```js
var i = 0;
do {
  console.log('number ->', i);
  i = i + 1;
} while(i <= 9)
```

**`for`** solution:

```js
for (var i = 0; i <= 9; i = i + 1) {
  console.log('number ->', i);
}
```

##### 26. What are the three clauses for a `for` loop?

> _initialization clause_
>
> _conditional test clause_
>
> _update clause_

#### Section: Functions

---

##### 27. What's a function?

> _a named block of code that performs a specific task. It's called (executed) by its name._

##### 28. Write a function `sum` that receives two numbers as arguments and returns the sum of both.

Solution:

```js
function sum (a, b) {
  return a + b;
}
```

##### 29. What's `scope` in JS?

> _a collection of variables as well as the rules for how those variables are accessed by name._

##### 30. Answer `true` or `false` for the following statements:

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

###### 30.1. Does the `inner` function have access to the `outer` function scope?

> `true`

###### 30.2. Does the `outer` function have access to the `inner` function scope?

> `false`

#### Section: Challenges

---

##### 1.1 Create a function `calculateAreaOfACircle` that receives `radius` as parameter. Use a constant `PI` equal to `3.14159`. _Avoid the temptation of using the `Math`library._

Solution:

```js
// create the constat PI here
const PI = 3.14159;

// create your function here
function calculateAreaOfACircle(r) {
  return PI * (r * r);
}

// Do NOT touch this code.
console.log('Expect area of a circle with radius = "3" to be "28.27431" ->', calculateAreaOfACircle(3) == 28.27431)
```

# Quiz - YDKJS: Up & Going 1/3

## Chapter 1: Into Programming

### Self-Evaluation

#### Section: Code

---

##### 1. What's a program?

> _your answer here_

##### 2. What's a computer language?

> _your answer here_

##### 3. What's a variable?

> _your answer here_

##### 4. What's a statement?

> _your answer here_

##### 5. From the statement `a = b * 2` identify its parts _(literals, variables, operators)._

> _your answer here_

##### 6. What's an expression?

> _your answer here_

##### 7. How many expressions can you indentify from the statement `a = b * 2;`?

> _your answer here_

##### 8. What's the difference between `interpreted` and `compiled` code?

> _your answer here_

##### 9. Is JavaScript `interpreted` or `compiled`? Explain why.

> _your answer here_

#### Section: Try It Yourself

---

##### 10. Output Exercises.

Consider: `var a = 1;`

Write the code to:

###### 10.1. print `a` in the __console__

> _`// your code here`_

###### 10.2. show `a` in a __popup__

> _`// your code here`_

##### 11. Input Exercises.

Code challenge:

Ask the user's name with a __prompt__ message `"Please, type your username"` and store it in a variable `username`, then log the value in the console.

Solution:

```js
// your code here
```

#### Section: Operators

---

##### 12. Complete the sentence:

JavaScript has both u___ and b___ operators, and one special t___ operator

> _your answer here_

##### 13. Operators types.

Name the _types of operators_ you know, and give some __basic__ examples.

> _your answer here_

#### Section: Values & Types

---

##### 14. Name JavaScript built-in types aka as _primitive_ values.

> _your answer here_

##### 15. What's coercion in JS?

> _your answer here_

##### 16. Explain the difference between `implicit` and `explicit` coercion in JS. Give examples.

> _your answer here_

#### Section: Code Comments

---

##### 17. What are the two types of comments in JS? Give examples.

> _your answer here_

##### 18. Why is it important to comment code?

> _your answer here_

#### Section Variables

---

##### 19. Does JavaScript use Static or Weak typing?

> _your answer here_

##### 20. Describe `static typing` aka `type enforcement`.

> _your answer here_

##### 21. Describe `weak typing` aka `dynamic typing`.

> _your answer here_

##### 22. Name some conventions to write constants in JS.

> _your answer here_

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

> _your answer here_

#### Section: Conditionals

---

##### 24. Write a block of code to validate if a variable `number` is less than `10` to log `one digit`, log `two digits` otherwise.

Solution:

```js
// your code here
```

#### Section: Loops

---

##### 25. Write a block of code to log numbers from `0-9` using `while`, `do-while` and `for` loops.

**`while`** solution:

```js
// your code here
```

**`do-while`** solution:

```js
// your code here
```

**`for`** solution:

```js
// your code here
```

##### 26. What are the three clauses for a `for` loop?

> _your answer here_

#### Section: Functions

---

##### 27. What's a function?

> _your answer here_

##### 28. Write a function `sum` that receives two numbers as arguments and returns the sum of both.

Solution:

```js
// your code here
```

##### 29. What's `scope` in JS?

> _your answer here_

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

> _your answer here_

###### 30.2. Does the `outer` function have access to the `inner` function scope?

> _your answer here_

#### Section: Challenges

---

##### 1.1 Create a function `calculateAreaOfACircle` that receives `radius` as parameter. Use a constant `PI` equal to `3.14159`. _Avoid the temptation of using the `Math`library._

Solution:

```js
// create the constat PI here


// create your function here


// Do NOT touch this code.
console.log('Expect area of a circle with radius = "3" to be "28.27431" ->', calculateAreaOfACircle(3) == 28.27431)
```

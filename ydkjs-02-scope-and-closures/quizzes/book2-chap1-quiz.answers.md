# Quiz - YDKJS: Scope & Closures 1/5

## Chapter 1. What is Scope?

### Answer Sheet

#### Section: Compiler Theory

---

##### 1. What are the three typical steps in a traditional compiled-language process?

> 1. Tokenizing / Lexing
>
> 2. Parsing
>
> 3. Code-Generation

##### 2. What does `AST` stands for?

> **A**bstract **S**yntax **T**ree

##### 3. So, is JS `interpreted` or `compiled`? Explain why

> JS is compiled as compilation happens just before (microseconds) the code is executed.

#### Section: Understanding Scope

---

##### 4. Once again: What's Scope?

> A well-defined set of rules for storing and finding variables (identifiers) in some location.

##### 5. What are the main "characters" involved in the compilation process?

> Engine
>
> Compiler
>
> Scope

##### 6. Describe both the `LHS` and `RHS` look-up terms.

> `LHS` Left-hand Side look-up. Process of looking for a variable (target) to **assign** it a value.
>
> `RHS` Right-hand Side look-up. Process of **retrieving** the value of a variable (source).

##### 7. Identify all the `LHS` and `RHS` look-ups for the following code snippet:

###### Snippet #1

```js
function square(number) {
  return number * number;
}

function cube(number) {
  return number * square(number);
}

const result = cube(3);
```

> Total `LHS` look-ups: 3
>
> * assignment to `result = ...`
>
> * implicit param assignment `number = 3` in fuction `cube(number)`
>
> * implicit param assignment `number = 3` in fuction `square(number)`
>
> Total `RHS` look-ups: 6
>
> * `cube(3)` function execution
>
>
> * inside `cube` function > retrieve the value for `number` in `number *`
>
> * inside `cube` function > execution of `square(...)`
>
> * inside `cube` function > retrieve the value of argument `number` in `square(number)`
>
> * inside `square` function > retrieve value for `number` in `number *`
>
> * inside `square` function > retrieve value for `number` in `* number`

#### Section: Nested Scope

---

##### 8. What are the rules for traversing a nested Scope?

> Engine starts at the currently executing Scope, then looks for a variable there, if not found, keeps going up one level an so on util it reaches the outermost **global** scope and stops whether it finds the variable or not.

##### 9. What would be the output for the following snippets?

###### Snippet #2

```js
g = 10;

function foo(a) {
  function bar(a, b) {
    var c = 5;

    function baz(d) {
      return d + c + b + a + g;
    }

    return baz(5);
  }

  return bar(10, a + 5);
}

var g;

console.log(foo(15));
```

> 50

###### Snippet #3

```js
(function foo(x) {
  function bar(y) {
    function baz(z) {
      w = x * y * z;

      return x + y + z;
    }

    return baz(4);
  }

  return bar(4);
})(4);

console.log(w);
```

> 64

#### Section: Errors

---

##### 10. When does a `ReferenceError` happen?

> When a variable couldn't be found in any of the Scopes.

##### 11. When does a `TypeError` happen?

> When a variable is found but an illegal/impossible action is attempted against its result.

##### 12. Write the output for the following snippets:

###### Snippet #4

```js
function bar(n) {
  return n * m;
  var m = 2;
}

console.log(bar(3));
```

> NaN

###### Snippet #5

```js
function bar(n) {
  return n * m;
  m = 2;
}

console.log(bar(3));
```

> ReferenceError: m is not defined

###### Snippet #6

```js
function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> 6

###### Snippet #7

```js
'use strict';

function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> ReferenceError: m is not defined

###### Snippet #8

```js
function bar(n) {
  var m = 2;
  return n * m;
}

bar = 5;

console.log(bar(3));
```

> TypeError: bar is not a function

###### Snippet #9

```js
var bar;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> 6

###### Snippet #10

```js
var bar = 3;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> TypeError: bar is not a function

###### Snippet #11

```js
function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));

var bar = 3;
```

> 6

###### Snippet #12

```js
var bar = 2;
var bar = 'a';

console.log(bar);
```

> "a"
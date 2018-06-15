# Quiz - YDKJS: Scope & Closures 1/5

## Chapter 1: What is Scope?

### Self-Evaluation

#### Section: Compiler Theory

---

##### 1. What are the three typical steps in a traditional compiled-language process?

> _your answer here_

##### 2. What does `AST` stands for?

> _your answer here_

##### 3. So, is JS `interpreted` or `compiled`? Explain why

> _your answer here_

#### Section: Understanding Scope

---

##### 4. Once again: What's Scope?

> _your answer here_

##### 5. What are the main "characters" involved in the compilation process?

> _your answer here_

##### 6. Describe both the `LHS` and `RHS` look-up terms.

> _your answer here_

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

> _total `LHS` look-ups:_
>
> _your answer here_
>
> _total `RHS` look-ups:_
>
> _your answer here_

#### Section: Nested Scope

---

##### 8. What are the rules for traversing a nested Scope?

> _your answer here_

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

> _your answer here_

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

> _your answer here_

#### Section: Errors

---

##### 10. When does a `ReferenceError` happen?

> _your answer here_

##### 11. When does a `TypeError` happen?

> _your answer here_

##### 12. Write the output for the following snippets:

###### Snippet #4

```js
function bar(n) {
  return n * m;
  var m = 2;
}

console.log(bar(3));
```

> _your answer here_

###### Snippet #5

```js
function bar(n) {
  return n * m;
  m = 2;
}

console.log(bar(3));
```

> _your answer here_

###### Snippet #6

```js
function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> _your answer here_

###### Snippet #7

```js
'use strict';

function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> _your answer here_

###### Snippet #8

```js
function bar(n) {
  var m = 2;
  return n * m;
}

bar = 5;

console.log(bar(3));
```

> _your answer here_

###### Snippet #9

```js
var bar;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> _your answer here_

###### Snippet #10

```js
var bar = 3;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> _your answer here_

###### Snippet #11

```js
function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));

var bar = 3;
```

> _your answer here_

###### Snippet #12

```js
var bar = 2;
var bar = 'a';

console.log(bar);
```

> _your answer here_
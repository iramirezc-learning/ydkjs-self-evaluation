# Quiz - YDKJS: Scope & Closures 1/5

## Chapter 1: What is Scope?

### Self-Evaluation

#### Section: Compiler Theory

---

##### 1. What are the three typical steps in a traditional compiled-language process?

> your answer here

##### 2. What does `AST` stands for?

> your answer here

##### 3. So, is JS `interpreted` or `compiled`? Explain why

> your answer here

#### Section: Understanding Scope

---

##### 4. Once again: What's Scope?

> your answer here

##### 5. What are the main "characters" involved in the compilation process?

> your answer here

##### 6. Describe both the `LHS` and `RHS` look-up terms.

> your answer here

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

> Total `LHS` look-ups:
>
> your answer here
>
> Total `RHS` look-ups:
>
> your answer here

#### Section: Nested Scope

---

##### 8. What are the rules for traversing a nested Scope?

> your answer here

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

> your answer here

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

> your answer here

#### Section: Errors

---

##### 10. When does a `ReferenceError` happen?

> your answer here

##### 11. When does a `TypeError` happen?

> your answer here

##### 12. Write the output for the following snippets:

###### Snippet #4

```js
function bar(n) {
  return n * m;
  var m = 2;
}

console.log(bar(3));
```

> your answer here

###### Snippet #5

```js
function bar(n) {
  return n * m;
  m = 2;
}

console.log(bar(3));
```

> your answer here

###### Snippet #6

```js
function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> your answer here

###### Snippet #7

```js
'use strict';

function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> your answer here

###### Snippet #8

```js
function bar(n) {
  var m = 2;
  return n * m;
}

bar = 5;

console.log(bar(3));
```

> your answer here

###### Snippet #9

```js
var bar;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> your answer here

###### Snippet #10

```js
var bar = 3;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> your answer here

###### Snippet #11

```js
function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));

var bar = 3;
```

> your answer here

###### Snippet #12

```js
var bar = 2;
var bar = 'a';

console.log(bar);
```

> your answer here
# Quiz - YDKJS: Scope & Closures 1/5

## Chapter 1. What is Scope?

### Answer Sheet

#### Section: Compiler Theory

---

##### 1. What are the three typical steps in a traditional compiled-language process?

> _1. Tokenizing / Lexing_
>
> _2. Parsing_
>
> _3. Code-Generation_

##### 2. What does `AST` stands for?

> _**A**bstract **S**yntax **T**ree_

##### 3. So, is JS `interpreted` or `compiled`? Explain why

> _JS is compiled as compilation happens just before (microseconds) the code is executed._

#### Section: Understanding Scope

---

##### 4. Once again: What's Scope?

> _a well-defined set of rules for storing and finding variables (identifiers) in some location._

##### 5. What are the main "characters" involved in the compilation process?

> _engine_
>
> _compiler_
>
> _scope_

##### 6. Describe both the `LHS` and `RHS` look-up terms.

> _`LHS` Left-hand Side look-up. Process of looking for a variable (target) to **assign** it a value._
>
> _`RHS` Right-hand Side look-up. Process of **retrieving** the value of a variable (source)._

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

> _total `LHS` look-ups: 3_
>
> * _assignment to `result = ...`_
>
> * _implicit param assignment `number = 3` in fuction `cube(number)`_
>
> * _implicit param assignment `number = 3` in fuction `square(number)`_
>
> _total `RHS` look-ups: 6_
>
> * _`cube(3)` function execution_
>
>
> * _inside `cube` function > retrieve the value for `number` in `number *`_
>
> * _inside `cube` function > execution of `square(...)`_
>
> * _inside `cube` function > retrieve the value of argument `number` in `square(number)`_
>
> * _inside `square` function > retrieve value for `number` in `number *`_
>
> * _inside `square` function > retrieve value for `number` in `* number`_

#### Section: Nested Scope

---

##### 8. What are the rules for traversing a nested Scope?

> _engine starts at the currently executing Scope, then looks for a variable there, if not found, keeps going up one level an so on util it reaches the outermost **global** scope and stops whether it finds the variable or not._

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

> _`50`_

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

> _`64`_

#### Section: Errors

---

##### 10. When does a `ReferenceError` happen?

> _when a variable couldn't be found in any of the Scopes._

##### 11. When does a `TypeError` happen?

> _when a variable is found but an illegal/impossible action is attempted against its result._

##### 12. Write the output for the following snippets:

###### Snippet #4

```js
function bar(n) {
  return n * m;
  var m = 2;
}

console.log(bar(3));
```

> _`NaN`_

###### Snippet #5

```js
function bar(n) {
  return n * m;
  m = 2;
}

console.log(bar(3));
```

> _`ReferenceError: m is not defined`_

###### Snippet #6

```js
function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> _`6`_

###### Snippet #7

```js
'use strict';

function bar(n) {
  m = 2;
  return n * m;
}

console.log(bar(3));
```

> _`ReferenceError: m is not defined`_

###### Snippet #8

```js
function bar(n) {
  var m = 2;
  return n * m;
}

bar = 5;

console.log(bar(3));
```

> _`TypeError: bar is not a function`_

###### Snippet #9

```js
var bar;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> _`6`_

###### Snippet #10

```js
var bar = 3;

function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));
```

> _`TypeError: bar is not a function`_

###### Snippet #11

```js
function bar(n) {
  var m = 2;
  return n * m;
}

console.log(bar(3));

var bar = 3;
```

> _`6`_

###### Snippet #12

```js
var bar = 2;
var bar = 'a';

console.log(bar);
```

> _"a"_
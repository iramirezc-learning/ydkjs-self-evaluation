# Quiz - YDKJS: Scope & Closures 2/5

## Chapter 2. Lexical Scope

### Self-Evaluation

#### Section: Lex-time

---

##### 1. What are the two predominant models for how Scope works used by the majority of programming languages?

> _your answer here_

##### 2. Which is the `Scope` model that JavaScript employs?

> _your answer here_

##### 3. How many `Scopes` can you identify in the following snippet, and what would be the output?

###### Snippet #1

```js
var result = (function (a) {
  function foo(b) {
    return bar(5);

    function bar(c) {
      return a + b + c;
    }
  }

  return foo(2);
})(3);

console.log(result);
```

> _your answer here_

##### 4. What is `shadowing`?

> _your answer here_

##### 5. Look Up in nested scopes. What would be the output for the following snippets?

_**NOTE:** replace `window` with `global` if you are using node.js_

###### Snippet #2

```js
var name = "John";

function foo(name) {
  function bar() {
    var name = "Doe";

    return (function baz() {
      return name;
    })();
  }
  return bar();
}

console.log(foo(name));
```

> _your answer here_

###### Snippet #3

```js
var a = 2;

console.log(window.a);
```

> _your answer here_

###### Snippet #4

```js
function foo() {
  var a = 3;
}

console.log(foo.a);
```

> _your answer here_

###### Snippet #5

```js
function foo() {
  // noop
}

foo.a = 4;

console.log(foo.a);
```

> _your answer here_

###### Snippet #6

```js
var a = 5;

function foo() {
  a = 10;

  console.log(a);
  console.log(window.a);
}

foo();
```

> _your answer here_

#### Section: Cheating Lexical

---

##### 6. `eval`. Write the output for the following snippets:

###### Snippet #7

```js
"use strict";

function foo(str) {
   eval(str);
   console.log(z);
}

foo("var z = 4;");
```

> _your answer here_

###### Snippet #8

```js
function foo(str) {
   eval(str);
   console.log(x);
}

foo("var x = 5;");
```

> _your answer here_

###### Snippet #9

```js
function foo(str) {
   eval(str);
}

foo("y = 7;");

console.log(y);
```

> _your answer here_

###### Snippet #10

```js
function foo(str) {
   eval(str);
}

foo("var y = 7;");

console.log(y);
```

> _your answer here_

##### 7. `with`. Write the output for the following snippets:

###### Snippet #11

```js
function foo(o) {
   with (o) {
     a = 5;
   }
}

var obj = { a: 2 };

foo(obj);

console.log(obj.a);
```

> _your answer here_

###### Snippet #12

```js
function foo(o) {
   with (o) {
     b = 10;
   }
}

var obj = { a: 2 };

foo(obj);

console.log(obj.b);
```

> _your answer here_

###### Snippet #13

```js
function foo(o) {
   with (o) {
     b = 5;
   }
}

var obj = { a: 2 };

foo(obj);

console.log(b);
```

> _your answer here_

###### Snippet #14

```js
function foo(o) {
   with (o) {
     b = 5;
   }
}

var obj = { a: 2 };

foo(obj);

console.log(a);
```

> _your answer here_

###### Snippet #15

```js
function foo(o) {
   with (o) {
     var b = 3;
   }
   console.log(b);
}

var obj = { b: 2 };

foo(obj);
```

> _your answer here_

###### Snippet #16

```js
function foo(o) {
   with (o) {
     var b;
   }
   b = 3;
   console.log(b);
}

var obj = { b: 2 };

foo(obj);
```

> _your answer here_

###### Snippet #17

```js
function foo(o) {
   with (o) {
     var b = 3;
   }
}

var obj = { b: 2 };

foo(obj);

console.log(b);
```

> _your answer here_

###### Snippet #18

```js
function foo(o) {
   with (o) {
     b = 3;
   }
}

var obj = { b: 2 };

foo(obj);

console.log(b);
```

> _your answer here_

###### Snippet #19

```js
"use strict";

function foo(o) {
   with (o) {
     b = 3;
   }
}

var obj = { a: 2 };

foo(obj);

console.log(b);
```

> _your answer here_

##### 8. Why should you avoid using both `eval` and `with` in your code?

> _your answer here_

##### 9. What's the difference between `Lexical Scope` and `Scope`?

> _your answer here_
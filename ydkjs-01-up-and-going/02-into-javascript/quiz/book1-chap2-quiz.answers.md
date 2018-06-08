# Quiz - YDKJS: Up & Going 2/3

## Chapter 2. Into JavaScript

### Answer Sheet

#### Section: Values & Types

---

##### Name the 7 built-in types available in JavaScript

> `undefined`
>
> `object`
>
> `boolean`
>
> `number`
>
> `string`
>
> `symbol`
>
> `function`

##### Name the two ways to access object properties

> dot notation `.`
>
> brackets notation `[]`

##### Typeof. Look at the following snippets and write what would be the ouput

###### Snippet #1

```js
console.log(typeof a);
var a;
```

> "undefined"

###### Snippet #2

```js
console.log(typeof "hello world");
```

> "string"

###### Snippet #3

```js
console.log(typeof false);
```

> "boolean"

###### Snippet #4

```js
console.log(typeof 21);
```

> "number"

###### Snippet #5

```js
console.log(typeof null);
```

> "object"

###### Snippet #6

```js
console.log(typeof undefined);
```

> "undefined"

###### Snippet #7

```js
console.log(typeof { name: "John" });
```

> "object"

###### Snippet #8

```js
console.log(typeof typeof 42);
```

> "string"

###### Snippet #9

```js
console.log(typeof 3.1416);
```

> "number"

###### Snippet #10

```js
console.log(typeof "10");
```

> "string"

###### Snippet #11

```js
var person = {
  name: "Peter",
  age: 40
};

console.log(typeof person.name);
console.log(typeof person.age);
console.log(typeof person.lastName);
```

> "string"
> "number"
> "undefined"

###### Snippet #12

```js
console.log(typeof []);
```

> "object"

###### Snippet #13

```js
console.log(typeof ["Hello", 20, true][2]);
```

> "boolean"

###### Snippet #14

```js
console.log(typeof ["Hello", 20, true][3]);
```

> "undefined"

###### Snippet #15

```js
console.log(typeof { a: 2 }["a"]);
```

> "number"

###### Snippet #16

```js
var index = "c";
console.log({ a: 1, b: 2, c: 3 }[index]);
```

> 3

###### Snippet #17

```js
console.log({ x: 100, y: 200 }.x);
```

> 100

###### Snippet #18

```js
function getX (point) {
  return point.x;
}

getX.PI = '3.1416';

console.log(typeof getX);
console.log(typeof getX({ x: 34, y: 54 }));
console.log(typeof getX.PI);
```

> "function"
> "number"
> "string"

###### Snippet #19

```js
var n = "47";
console.log(typeof n);
console.log(typeof Number(n));
```

> "string"
> "number"

###### Snippet #20

```js
var n = "47";
console.log(typeof (n * 2));
```

> "number"

##### Coercion. Label the following code snippets with `explicit` or `implicit` accordingly

###### Snippet #21

```js
var a = "13";
var b = a * 2;
console.log(a); // "13"
console.log(b); // 26
```

> `implicit`

###### Snippet #22

```js
var a = "13";
var b = Number(a);
console.log(a); // "13"
console.log(b); // 13
```

> `explicit`

##### List the `falsy` values in JS

> `""` or `''` Empty string
>
> `0`, `-0`, `NaN` Zero, -Zero, Not a Number
>
> `null` Object
>
> `undefined` Undefined
>
> `false` Boolean

##### Boolean Coercion. Write the result `true` or `false` for the following snippets

###### Snippet #23

```js
Boolean('');
```

> `false`

###### Snippet #24

```js
Boolean('.');
```

> `true`

###### Snippet #25

```js
Boolean("");
```

> `false`

###### Snippet #26

```js
Boolean(0);
```

> `false`

###### Snippet #26-2

```js
Boolean("0");
```

> `true`

###### Snippet #27

```js
Boolean(1);
```

> `true`

###### Snippet #28

```js
Boolean(1/0);
```

> `true`

###### Snippet #29

```js
Boolean(0/1);
```

> `false`

###### Snippet #30

```js
Boolean(NaN);
```

> `false`

###### Snippet #31

```js
Boolean(Infinity);
```

> `true`

###### Snippet #32

```js
Boolean(0 + "0");
```

> `true`

###### Snippet #33

```js
Boolean("0" + 0);
```

> `true`

###### Snippet #34

```js
Boolean("0" * 1);
```

> `false`

###### Snippet #35

```js
Boolean(1 * "0");
```

> `false`

###### Snippet #36

```js
Boolean(-1 * 0);
```

> `false`

###### Snippet #37

```js
Boolean(null);
```

> `false`

###### Snippet #38

```js
Boolean(undefined);
```

> `false`

###### Snippet #39

```js
Boolean(false);
```

> `false`

###### Snippet #40

```js
Boolean(true);
```

> `true`

###### Snippet #41

```js
Boolean([]);
```

> `true`

###### Snippet #42

```js
Boolean([1, 2, 3]);
```

> `true`

###### Snippet #43

```js
Boolean([0].toString());
```

> `true`

###### Snippet #43-2

```js
Boolean([1, '', {}][1]);
```

> `false`

###### Snippet #43-3

```js
Boolean([1, '', { n: 0 }][2].n);
```

> `false`

###### Snippet #44

```js
Boolean([].toString());
```

> `false`

###### Snippet #45

```js
Boolean({});
```

> `true`

###### Snippet #45-2

```js
Boolean({}.toString());
```

> `true`

###### Snippet #46

```js
Boolean({ name: "Doe" });
```

> `true`

###### Snippet #47

```js
Boolean({ toString: function () {
  return '';
}}.toString());
```

> `false`

###### Snippet #48

```js
Boolean({ number: 0 }.number);
```

> `false`

###### Snippet #49

```js
Boolean({ char: 'a' }.char);
```

> `true`

###### Snippet #50

```js
Boolean(function noop() {});
```

> `true`

##### operator that checks for value equality with coercion allowed

> `==`

##### operator that checks for value equality without allowing coercion

> `===`

##### operator that checks for value non-equality with coercion allowed

> `!=`

##### operator that checks for value non-equality without allowing coercion

> `!==`

##### Equality Coercion. Write the result `true` or `false` for the following snippets

###### Snippet #51

```js
"12" == 12;
```

> `true`

###### Snippet #51-2

```js
12 === "12";
```

> `false`

###### Snippet #52

```js
1 == true;
```

> `true`

###### Snippet #52-2

```js
true === 1;
```

> `false`

###### Snippet #53

```js
false == 0;
```

> `true`

###### Snippet #54

```js
false == "false";
```

> `false`

###### Snippet #55

```js
"" == false;
```

> `true`

###### Snippet #56

```js
null == false;
```

> `false`

###### Snippet #57

```js
undefined == null;
```

> `true`

###### Snippet #58

```js
false == undefined;
```

> `false`

###### Snippet #59

```js
0 == "";
```

> `true`

###### Snippet #60

```js
0 == null;
```

> `false`

###### Snippet #61

```js
var a;
a == null;
```

> `true`

###### Snippet #62

```js
({} == {});
```

> `false`

###### Snippet #63

```js
({} === {});
```

> `false`

###### Snippet #64

```js
 [] == [];
```

> `false`

###### Snippet #65

```js
 [1, 2, 3] === [1, 2, 3];
```

> `false`

###### Snippet #66

```js
 [1, 2, 3] == "1,2,3";
```

> `true`

###### Snippet #67

```js
 NaN == NaN;
```

> `false`

###### Snippet #68

```js
 NaN === NaN;
```

> `false`

###### Snippet #68-2

```js
 (function noop (){}) == (function noop (){});
```

> `false`

###### Snippet #68-3

```js
 (function noop (){}).toString() == (function noop (){});
```

> `true`

##### Inequality Coercion. Write `true` or `false` for the following snippets

###### Snippet #69

```js
 2 > "1";
```

> `true`

###### Snippet #70

```js
 "a" < "b";
```

> `true`

###### Snippet #71

```js
 3 < "a";
```

> `false`

###### Snippet #72

```js
 "3" < "a";
```

> `true`

###### Snippet #73

```js
 0 > NaN;
```

> `false`

#### Variables

---

##### Are these valid JS indentifiers? Fill the table with `true` or `false`

| identifier | is valid? |
|------------|-----------|
| `Name` | `true` |
| `0duck` | `false` |
| `last.name` | `false` |
| `$account` | `true` |
| `_age` | `true` |
| `-price` | `false` |
| `car[123]` | `false` |
| `for` | `false` |

##### What's hoisting?

> when a `var` declaration is conceptually "moved" to the top of its enclosing scope.

##### Hoisting. What would be the output for this snippet?

###### Snippet #74

```js
a = 10;

foo ();

function foo () {
  a = 5;

  console.log(a);

  var a;
}

var a;

console.log(a);
```

> 5
> 10

##### What's the main difference between `var` and `let`?

> `var` declares variables at function level
> `let` declares variables at block level

##### Nested Scopes, `var` & `let`. Write the output for the following code snippets

###### Snippet #75

```js
var a = 1;

function foo () {
  if (a == 1) {
    var b = 2;
  }

  console.log(b);
}

foo();
```

> 2

###### Snippet #76

```js
var a = 1;

function foo () {
  if (a == 1) {
    let b = 2;
  }

  console.log(b);
}

foo();
```

> `Uncaught ReferenceError: b is not defined`

###### Snippet #77

```js
function foo () {
  var a = 10
}

foo();

console.log(a);
```

> `Uncaught ReferenceError: a is not defined`

###### Snippet #78

```js
function foo () {
  a = 20
}

foo();

console.log(a);
```

> 20

#### Section: Conditionals

---

##### Write the code to log if a number is `even` or `odd` using the `if` statement, `switch` statement and the conditional operator `?:` aka ternay operator

_Clue_: you can determine if a number is `even` if the remainder of `n` divided by `2` is equal to `0`. Use the remainder operator `%`.

> `if` solution:

```js
var n = 10;

if (n % 2 == 0) {
  console.log('even');
} else {
  console.log('odd');
}
```

> `switch` solution:

```js
var n = 10;

switch (n % 2) {
  case 0:
    console.log('even');
    break;
  default:
    console.log('odd');
}
```

> `ternary` solution:

```js
var n = 10;

console.log(n % 2 == 0 ? "even" : "odd")
```

#### Section: Strict Mode

---

##### In your own words, what's `use strict;`?

> Is a way to force code to be better written.
>
> Is a way to opt in to a restricted variant of JS.
>
> Is a way to avoid bugs.
>
> Is the opposite of `sloppy mode`.

##### Use Strict. Write the output for the following code snippets

###### Snippet #79

```js
function yummy () {
  a = 50
}

yummy();

console.log(a);
```

> 50

###### Snippet #80

```js
'use strict';

function yummy () {
  a = 50
}

yummy();

console.log(a);
```

> `Uncaught ReferenceError: a is not defined`

#### Section: Functions As Values

---

##### Complete the sentence

Functions are the primary mechanism of _____ in JS.

> _scope_

##### Create a function `square` that takes one parameter `number` that returns the result of that `number` multiplied by itself. You need to perform this in `3` different ways

* by using `function declaration` syntax

> solution:

```js
function square (number) {
  return number * number;
}
```

* by using `function expression with an anonymous function` syntax.

> solution:

```js
var square = function (number) {
  return number * number;
};
```

* by using `function expression with a named function` syntax.

> solution:

```js
var square = function square (number) {
  return number * number;
};
```

##### What's an `IIFE`? Give an example

> an **I**mmediately **I**nvoked **F**unction **E**xpression
> example:

```js
(function hello () {
  console.log("hello!");
})();
```

##### What's a `closure` in JS?

> A _closure_ is the combination of a function and the lexical environment within which that function was declared.

##### Closure. What would be the output for the following code?

###### Snippet #81

```js
function createHello (greeting) {
  return function greet (name) {
    return greeting + " " + name + "!";
  }
}

var greetInSpanish = createHello('Hola');

console.log(greetInSpanish("Pedro"));
console.log(createHello('Hi')("Mike"));
```

> "Hola Pedro!"
>
> "Hi Mike!"

#### Section: `this` Keyword

---

##### `this`. Write the output for the following code

###### Snippet #82

```js
// Kitties
function sayHello() {
  console.log("Hello " + this.name);
}

var name = "Fluffy";

sayHello();

var kitty = {
  name: "Buttercup",
  sayHello: sayHello
};

kitty.sayHello();

sayHello.call({ name: "Cocoa" });

new sayHello();
```

> "Hello Fluffy"
>
> "Hello Buttercup"
>
> "Hello Cocoa"
>
> "Hello undefined"

#### Section: Prototypes

---

##### Prototypes. Write the output for the following code

###### Snippet #83

```js
var animal = {
  walk: "I'm walking!"
};

var bird = Object.create(animal);

bird.fly = "I'm flying!";

var penguin = Object.create(bird);

penguin.fly = "I can't fly :(";
penguin.swim = "I'm swimming!";

var canary = Object.create(bird);

var tiger = Object.create(animal);

console.log(tiger.walk);
console.log(tiger.fly);
console.log(canary.fly);
console.log(canary.walk);
console.log(canary.swim);
console.log(penguin.fly);
console.log(penguin.walk);
console.log(penguin.swim);
```

> "I'm walking!"
>
> "undefined"
>
> "I'm flying!"
>
> "I'm walking!"
>
> "undefined"
>
> "I can't fly :("
>
> "I'm walking!"
>
> "I'm swimming!"

#### Section: Old & New

---

##### What are the two main techniques to make older browsers work with newer features available in JS? Describe each

> __Polyfilling.__ A piece of code that provides the techonology that you expect the browser to provide natively.
>
> __Transpiling.__ The process that converts your newer code into older code equivalents.

#### Section: Non-JavaScript

---

##### Is the `alert` method provided by the JS engine?

> No, `alert` is provided by the browser.

#### Section: Challenges

---

##### 2.1 Create a module in an `IIFE` stored in a variable `calculator` that exposes 4 methods: `plus`, `minus`, `times` and `dividedBy`. Each method should receive one parameter `firstNumber` and return a function that receives another parameter `secondNumber`. Every method should perform the operation it describes, for example, it's expected that `plus` adds the `firstNumber` to the `secondNumber`, `dividedBy` should divide the `secondNumber` by the `firstNumber` and so on. The idea is to have "stored" the `firstNumber` to perform the next operations with it

_TIP:_ You can create a `script.js`file and test your code in the browser or node.js.

```js
// create your calculator module here
var calculator;

// Do NOT touch this code

const testCases = [
  { type: "plus", n1: 3, n2: [1, 2, 3], expected: [4, 5, 6] },
  { type: "minus", n1: 1, n2: [1, 0, -1], expected: [0, -1, -2] },
  { type: "times", n1: 5, n2: [2, 5, 10], expected: [10, 25, 50] },
  { type: "dividedBy", n1: 10, n2: [10, 100, 1000], expected: [1, 10, 100] }
];

const result = testCases.every(test => {
  const operation = calculator[test.type](test.n1);
  return test.n2.every((number, i) => {
    const testPassed = operation(number) === test.expected[i];
    if (!testPassed) {
      console.log(`Expected: ${operation(number)} to be: ${test.expected[i]}. Operation: secondNumber(${number}) ${test.type} firstNumber(${test.n1})`);
    }
    return testPassed;
  });
});

console.log("All tests passed: ", result);
```

> solution:

```js
var calculator = (function calc () {
  function plus (firstNumber) {
    return function addTo (secondNumber) {
      return secondNumber + firstNumber;
    }
  }

  function minus (firstNumber) {
    return function subtractTo (secondNumber) {
      return secondNumber - firstNumber;
    }
  }

  function times (firstNumber) {
    return function multiplyTo (secondNumber) {
      return secondNumber * firstNumber;
    }
  }

  function dividedBy (firstNumber) {
    return function divideTo (secondNumber) {
      return secondNumber / firstNumber;
    }
  }

  return {
    plus: plus,
    minus: minus,
    times: times,
    dividedBy: dividedBy
  };
})();
```

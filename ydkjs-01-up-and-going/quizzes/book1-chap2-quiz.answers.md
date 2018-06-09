# Quiz - YDKJS: Up & Going 2/3

## Chapter 2: Into JavaScript

### Answer Sheet

#### Section: Values & Types

---

##### 1. Name the 7 built-in types available in JavaScript.

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

##### 2. Name the two ways to access object properties.

> _dot notation `.`_
>
> _brackets notation `[]`_

##### 3. Typeof. Look at the following snippets and write what would be the ouput.

###### Snippet #1

```js
console.log(typeof a);
var a;
```

> _"undefined"_

###### Snippet #2

```js
console.log(typeof "hello world");
```

> _"string"_

###### Snippet #3

```js
console.log(typeof false);
```

> _"boolean"_

###### Snippet #4

```js
console.log(typeof 21);
```

> _"number"_

###### Snippet #5

```js
console.log(typeof null);
```

> _"object"_

###### Snippet #6

```js
console.log(typeof undefined);
```

> _"undefined"_

###### Snippet #7

```js
console.log(typeof { name: "John" });
```

> _"object"_

###### Snippet #8

```js
console.log(typeof typeof 42);
```

> _"string"_

###### Snippet #9

```js
console.log(typeof 3.1416);
```

> _"number"_

###### Snippet #10

```js
console.log(typeof "10");
```

> _"string"_

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

> _"string"_
>
> _"number"_
>
> _"undefined"_

###### Snippet #12

```js
console.log(typeof []);
```

> _"object"_

###### Snippet #13

```js
console.log(typeof ["Hello", 20, true][2]);
```

> _"boolean"_

###### Snippet #14

```js
console.log(typeof ["Hello", 20, true][3]);
```

> _"undefined"_

###### Snippet #15

```js
console.log(typeof { a: 2 }["a"]);
```

> _"number"_

###### Snippet #16

```js
var index = "c";
console.log({ a: 1, b: 2, c: 3 }[index]);
```

> _3_

###### Snippet #17

```js
console.log({ x: 100, y: 200 }.x);
```

> _100_

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

> _"function"_
>
> _"number"_
>
> _"string"_

###### Snippet #19

```js
var n = "47";
console.log(typeof n);
console.log(typeof Number(n));
```

> _"string"_
>
> _"number"_

###### Snippet #20

```js
var n = "47";
console.log(typeof (n * 2));
```

> _"number"_

##### 4. Coercion. Label the following code snippets with `explicit` or `implicit` accordingly.

###### Snippet #21

```js
var a = "13";
var b = a * 2;
console.log(a); // "13"
console.log(b); // 26
```

> _`implicit`_

###### Snippet #22

```js
var a = "13";
var b = Number(a);
console.log(a); // "13"
console.log(b); // 13
```

> _`explicit`_

##### 5. List the `falsy` values in JS.

> _`""` or `''` empty string_
>
> _`0`, `-0`, `NaN` zero, -zero, not a number_
>
> _`null` object_
>
> _`undefined` undefined_
>
> _`false` boolean_

##### 6. Boolean Coercion. Write the result `true` or `false` for the following snippets.

###### Snippet #23

```js
Boolean('');
```

> _`false`_

###### Snippet #24

```js
Boolean('.');
```

> _`true`_

###### Snippet #25

```js
Boolean("");
```

> _`false`_

###### Snippet #26

```js
Boolean(0);
```

> _`false`_

###### Snippet #26-2

```js
Boolean("0");
```

> _`true`_

###### Snippet #27

```js
Boolean(1);
```

> _`true`_

###### Snippet #28

```js
Boolean(1/0);
```

> _`true`_

###### Snippet #29

```js
Boolean(0/1);
```

> _`false`_

###### Snippet #30

```js
Boolean(NaN);
```

> _`false`_

###### Snippet #31

```js
Boolean(Infinity);
```

> _`true`_

###### Snippet #32

```js
Boolean(0 + "0");
```

> _`true`_

###### Snippet #33

```js
Boolean("0" + 0);
```

> _`true`_

###### Snippet #34

```js
Boolean("0" * 1);
```

> _`false`_

###### Snippet #35

```js
Boolean(1 * "0");
```

> _`false`_

###### Snippet #36

```js
Boolean(-1 * 0);
```

> _`false`_

###### Snippet #37

```js
Boolean(null);
```

> _`false`_

###### Snippet #38

```js
Boolean(undefined);
```

> _`false`_

###### Snippet #39

```js
Boolean(false);
```

> _`false`_

###### Snippet #40

```js
Boolean(true);
```

> _`true`_

###### Snippet #41

```js
Boolean([]);
```

> _`true`_

###### Snippet #42

```js
Boolean([1, 2, 3]);
```

> _`true`_

###### Snippet #43

```js
Boolean([0].toString());
```

> _`true`_

###### Snippet #43-2

```js
Boolean([1, '', {}][1]);
```

> _`false`_

###### Snippet #43-3

```js
Boolean([1, '', { n: 0 }][2].n);
```

> _`false`_

###### Snippet #44

```js
Boolean([].toString());
```

> _`false`_

###### Snippet #45

```js
Boolean({});
```

> _`true`_

###### Snippet #45-2

```js
Boolean({}.toString());
```

> _`true`_

###### Snippet #46

```js
Boolean({ name: "Doe" });
```

> _`true`_

###### Snippet #47

```js
Boolean({ toString: function () {
  return '';
}}.toString());
```

> _`false`_

###### Snippet #48

```js
Boolean({ number: 0 }.number);
```

> _`false`_

###### Snippet #49

```js
Boolean({ char: 'a' }.char);
```

> _`true`_

###### Snippet #50

```js
Boolean(function noop() {});
```

> _`true`_

##### 7. Operator that checks for value equality with coercion allowed:

> _`==`_

##### 8. Operator that checks for value equality without allowing coercion:

> _`===`_

##### 9. Operator that checks for value non-equality with coercion allowed:

> _`!=`_

##### 10. Operator that checks for value non-equality without allowing coercion:

> _`!==`_

##### 11. Equality Coercion. Write the result `true` or `false` for the following snippets:

###### Snippet #51

```js
"12" == 12;
```

> _`true`_

###### Snippet #51-2

```js
12 === "12";
```

> _`false`_

###### Snippet #52

```js
1 == true;
```

> _`true`_

###### Snippet #52-2

```js
true === 1;
```

> _`false`_

###### Snippet #53

```js
false == 0;
```

> _`true`_

###### Snippet #54

```js
false == "false";
```

> _`false`_

###### Snippet #55

```js
"" == false;
```

> _`true`_

###### Snippet #56

```js
null == false;
```

> _`false`_

###### Snippet #57

```js
undefined == null;
```

> _`true`_

###### Snippet #58

```js
false == undefined;
```

> _`false`_

###### Snippet #59

```js
0 == "";
```

> _`true`_

###### Snippet #60

```js
0 == null;
```

> _`false`_

###### Snippet #61

```js
var a;
a == null;
```

> _`true`_

###### Snippet #62

```js
({} == {});
```

> _`false`_

###### Snippet #63

```js
({} === {});
```

> _`false`_

###### Snippet #64

```js
 [] == [];
```

> _`false`_

###### Snippet #65

```js
 [1, 2, 3] === [1, 2, 3];
```

> _`false`_

###### Snippet #66

```js
 [1, 2, 3] == "1,2,3";
```

> _`true`_

###### Snippet #67

```js
 NaN == NaN;
```

> _`false`_

###### Snippet #68

```js
 NaN === NaN;
```

> _`false`_

###### Snippet #68-2

```js
 (function noop (){}) == (function noop (){});
```

> _`false`_

###### Snippet #68-3

```js
 (function noop (){}).toString() == (function noop (){});
```

> _`true`_

##### 12. Inequality Coercion. Write `true` or `false` for the following snippets

###### Snippet #69

```js
 2 > "1";
```

> _`true`_

###### Snippet #70

```js
 "a" < "b";
```

> _`true`_

###### Snippet #71

```js
 3 < "a";
```

> _`false`_

###### Snippet #72

```js
 "3" < "a";
```

> _`true`_

###### Snippet #73

```js
 0 > NaN;
```

> _`false`_

#### Variables

---

##### 13. Are these valid JS indentifiers? Fill the table with `true` or `false`

| identifier  | is valid? |
|-------------|-----------|
| `Name`      | _`true`_  |
| `0duck`     | _`false`_ |
| `last.name` | _`false`_ |
| `$account`  | _`true`_  |
| `_age`      | _`true`_  |
| `-price`    | _`false`_ |
| `car[123]`  | _`false`_ |
| `for`       | _`false`_ |

##### 14. What's hoisting?

> _when a `var` declaration is conceptually "moved" to the top of its enclosing scope._

##### 15. Hoisting. What would be the output for this snippet?

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

> _5_
>
> _10_

##### 16. What's the main difference between `var` and `let`?

> _`var` declares variables at function level_
>
> _`let` declares variables at block level_

##### 17. Nested Scopes, `var` & `let`. Write the output for the following code snippets

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

> _2_

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

> _`Uncaught ReferenceError: b is not defined`_

###### Snippet #77

```js
function foo () {
  var a = 10
}

foo();

console.log(a);
```

> _`Uncaught ReferenceError: a is not defined`_

###### Snippet #78

```js
function foo () {
  a = 20
}

foo();

console.log(a);
```

> _20_

#### Section: Conditionals

---

##### 18. Write the code to log if a number is `even` or `odd` using the `if` statement, `switch` statement and the conditional operator `?:` aka ternay operator

_Clue_: you can determine if a number is `even` if the remainder of `n` divided by `2` is equal to `0`. Use the remainder operator `%`.

**`if`** Solution:

```js
var n = 10;

if (n % 2 == 0) {
  console.log('even');
} else {
  console.log('odd');
}
```

**`switch`** Solution:

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

**`ternary`** Solution:

```js
var n = 10;

console.log(n % 2 == 0 ? "even" : "odd")
```

#### Section: Strict Mode

---

##### 19. In your own words, what's `use strict;`?

> _Is a way to force code to be better written._
>
> _Is a way to opt in to a restricted variant of JS._
>
> _Is a way to avoid bugs._
>
> _Is the opposite of `sloppy mode`._

##### 20. Use Strict. Write the output for the following code snippets

###### Snippet #79

```js
function yummy () {
  a = 50
}

yummy();

console.log(a);
```

> _50_

###### Snippet #80

```js
'use strict';

function yummy () {
  a = 50
}

yummy();

console.log(a);
```

> _`Uncaught ReferenceError: a is not defined`_

#### Section: Functions As Values

---

##### 21. Complete the sentence

Functions are the primary mechanism of _____ in JS.

> _scope_

##### 22. Create a function `square` that takes one parameter `number` that returns the result of that `number` multiplied by itself. You need to perform this in `3` different ways

###### 22.1. by using `function declaration` syntax.

Solution:

```js
function square (number) {
  return number * number;
}
```

###### 22.2. by using `function expression with an anonymous function` syntax.

Solution:

```js
var square = function (number) {
  return number * number;
};
```

###### 22.3 by using `function expression with a named function` syntax.

Solution:

```js
var square = function square (number) {
  return number * number;
};
```

##### 23. What's an `IIFE`? Give an example.

> _an **I**mmediately **I**nvoked **F**unction **E**xpression_
>
> _example:_

```js
(function hello () {
  console.log("hello!");
})();
```

##### 24. What's a `closure` in JS?

> _a `closure` is the combination of a function and the lexical environment within which that function was declared._

##### 25. Closure. What would be the output for the following code?

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

> _"Hola Pedro!"_
>
> _"Hi Mike!"_

#### Section: `this` Keyword

---

##### 26. `this`. Write the output for the following code

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

> _"Hello Fluffy"_
>
> _"Hello Buttercup"_
>
> _"Hello Cocoa"_
>
> _"Hello undefined"_

#### Section: Prototypes

---

##### 27. Prototypes. Write the output for the following code

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

> _"I'm walking!"_
>
> _"undefined"_
>
> _"I'm flying!"_
>
> _"I'm walking!"_
>
> _"undefined"_
>
> _"I can't fly: :("_
>
> _"I'm walking!"_
>
> _"I'm swimming!"_

#### Section: Old & New

---

##### 28. What are the two main techniques to make older browsers work with newer features available in JS? Describe each

> _**polyfilling.** A piece of code that provides the techonology that you expect the browser to provide natively._
>
> _**transpiling.** The process that converts your newer code into older code equivalents._

#### Section: Non-JavaScript

---

##### 29. Is the `alert` method provided by the JS engine?

> _nope, `alert` is provided by the browser._

#### Section: Challenges

---

##### 2.1 Create a module in an `IIFE` stored in a variable `calculator` that exposes 4 methods: `plus`, `minus`, `times` and `dividedBy`. Each method should receive one parameter `firstNumber` and return a function that receives another parameter `secondNumber`. Every method should perform the operation it describes, for example, it's expected that `plus` adds the `firstNumber` to the `secondNumber`, `dividedBy` should divide the `secondNumber` by the `firstNumber` and so on. The idea is to have "stored" the `firstNumber` to perform the next operations with it.

_**TIP:**_ You can create a `script.js`file and test your code in the browser or node.js.

Solution:

```js
// create your calculator module here
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

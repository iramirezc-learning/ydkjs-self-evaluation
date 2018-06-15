# Summary - Chapter 1: What's Scope?

JavaScript is __compiled__, no argue.

`LHS` Left-hand Side look-up. Process of looking for a variable (target) to **assign** it a value.

Example:

`var a = 2;`

`RHS` Right-hand Side look-up. Process of **retrieving** the value of a variable (source).

Example:

`console.log(a); // What's the value for "a"`

Functions declarations do __NOT__ involve a `LHS` look-up since the compiler handles both the declaraion and value definition during code-generation.

The following code has:

* 1 `LHS` look-up
  * `a = 3` initialization of param `a` in function `foo`
* 2 `RHS` look-ups
  * `foo` execution `foo(3)`
  * `a` in expresion `a * 2`

```js
function foo(a) {
  return a * 2;
}

foo(3);
```
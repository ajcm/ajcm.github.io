# Javascript

### Tutorials

[Javascript tutorial](https://javascript.info/)

[Destructuring objects](https://codeburst.io/es6-destructuring-the-complete-guide-7f842d08b98f)

[Arrow Functions](https://zendev.com/2018/10/01/javascript-arrow-functions-how-why-when.html)



### Basics

**variables**
>  let variable = value

```javascript
let user = 'John', age = 25, message = 'Hello';
```

**constants**

> const constant = value

```javascript
const myBirthday = '18.04.1982';
```

> There is a widespread practice to use constants as aliases for difficult-to-remember values that are known prior to execution.
..
const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";





### Datatypes

#### Number
```javascript
let n = 123;
n = 12.345;
```
> `NaN` represents a computational error

#### BigInt
Added to represent integers of arbitrary length.
```javascript
// the "n" at the end means it's a BigInt
const bigInt = 1234567890123456789012345678901234567890n;
```
#### String

```javascript
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed another ${str}`;
```
> there is no Character type in js

#### Boolean
```javascript
let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked
```

**Conversions**

Values that are intuitively “empty”, like `0`, an empty string, `null`, `undefined`, and `NaN`, become `false`, other values become `true`.

```javascript
alert( Boolean(1) ); // true
alert( Boolean(0) ); // false
alert( Boolean("hello") ); // true
alert( Boolean("") ); // false
```

#### null/undefined
> `null` is not a “reference to a non-existing object” or a “null pointer”
`undefined` is “value is not assigned”.

#### typeof
>`typeof` operator returns the type of the argument

It supports two forms of syntax, as operator: `typeof x` and as a function: `typeof(x)`.

```javascript
typeof undefined // "undefined"
typeof 0 // "number"
typeof 10n // "bigint"
typeof true // "boolean"
typeof "foo" // "string"
typeof Symbol("id") // "symbol"
typeof Math // "object"  (1)
typeof null // "object"  (2)
typeof alert // "function"  (3)
```



### Comparison

| expression | value|
|--|--|
| `'2' > 1` |  `true` |
| `'01' == 1`  | `true`  |
|`true == 1`|`true`|
|`false == 0`|`true`|
|`0 == false`|`true`|
|`'' == false` |`true`|
|`null == undefined`| `true`|
|`null == 0` |`false`|
|`undefined == 0`|`false`|

>  strict equality operator `===` checks the equality without type conversion.**
 if `a` and `b` are of different types, then `a === b` immediately returns `false` without an attempt to convert them.

| expression | value|
|--|--|
|`0 === false` |  `false` |
|`null === undefined` | `false`|





### Functions

with default values
```javascript
function showMessage(from, text = "no text given") {
  alert( from + ": " + text );
}
showMessage("Ann"); // Ann: no text given
```

> A function with an empty `return` or without it returns `undefined`

**Function Expression**
```javascript
let sayHi = function() {
  alert( "Hello" );
};
```

**Arrow functions**
```javascript
const add = (a, b) => a + b;
```

Without curly braces: `(...args) => expression` – the right side is an expression: the function evaluates it and returns the result. With curly braces: `(...args) => { body }` – brackets allow us to write multiple statements inside the function, but we need an explicit `return` to return something.

>arrow functions do not have `this`. If `this` is accessed, it is taken from the outside.
>Arrow functions also have no `arguments` variable.

To indicate that instead you want a single expression that happens to be an object, you wrap the object with parentheses:

```javascript
(name, description) => ({name: name, description: description});
```

There’s a subtle difference between an arrow function `=>` and a regular function called with `.bind(this)`:

-   `.bind(this)` creates a “bound version” of the function.
-   The arrow `=>` doesn’t create any binding. The function simply doesn’t have `this`. The lookup of `this` is made exactly the same way as a regular variable search: in the outer lexical environment.





### Objects

```javascript
let user = new Object(); // "object constructor" syntax
let user = {};  // "object literal" syntax
```
```javascript
let user = {
  name: "John",
  age: 30,
  "likes birds": true  // multiword property name must be quoted
};

user.name = 'New name'

user["likes birds"] = true;
```




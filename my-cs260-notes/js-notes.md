# Java Script
from MDN

```
JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles.

JavaScript's dynamic capabilities include runtime object construction, variable parameter lists, function variables, dynamic script creation (via eval), object introspection (via for...in and Object utilities), and source-code recovery (JavaScript functions store their source text and can be retrieved through toString()).
```

## Adding JS to HTML

you can insert JS into HTML either by including it in HTML between `<script>` element or by using `src` attribute of script element (link in head of html)

special attributes like `onclick` automatically create event listeners

## Declaring variables 

`let` allows you to change variable
`const` allows you to 

### type
Primitive types

| Type        | Meaning                                                    |
| ----------- | ---------------------------------------------------------- |
| `Null`      | The type of a variable that has not been assigned a value. |
| `Undefined` | The type of a variable that has not been defined.          |
| `Boolean`   | true or false.                                             |
| `Number`    | A 64-bit signed number.                                    |
| `BigInt`    | A number of arbitrary magnitude.                           |
| `String`    | A textual sequence of characters.                          |
| `Symbol`    | A unique value.                                            |

Object types

| Type       | Use                                                                                    | Example                  |
| ---------- | -------------------------------------------------------------------------------------- | ------------------------ |
| `Object`   | A collection of properties represented by name-value pairs. Values can be of any type. | `{a:3, b:'fish'}`        |
| `Function` | An object that has the ability to be called.                                           | `function a() {}`        |
| `Date`     | Calendar dates and times.                                                              | `new Date('1995-12-17')` |
| `Array`    | An ordered sequence of any type.                                                       | `[3, 'fish']`            |
| `Map`      | A collection of key-value pairs that support efficient lookups.                        | `new Map()`              |
| `JSON`     | A lightweight data-interchange format used to share information across programs.       | `{"a":3, "b":"fish"}`    |

### Common operators

When dealing with a number variable, JavaScript supports standard mathematical operators like + (add), - (subtract), * (multiply), / (divide), and === (equality). For string variables, JavaScript supports + (concatenation) and === (equality).

### Type Conversions

JS is weekly typed language. Variable always has a type but type can change when assigned a new value

```js
2 + '3';
// OUTPUT: '23'
2 * '3';
// OUTPUT: 6
[2] + [3];
// OUTPUT: '23'
true + null;
// OUTPUT: 1
true + undefined;
// OUTPUT: NaN
```

STRICT VS LOOSE EQUALITY (===, !==, vs ==, !=)
USE STRICT -- it is more intuitive
```js
1 === '1';
// OUTPUT: false
null === undefined;
// OUTPUT: false
'' === false;
// OUTPUT: false
```

Falsy and truthy evaluations (falsy are things like '' null, undetfiend, 0, -0, etc)
```js
1 == '1';
// OUTPUT: true
null == undefined;
// OUTPUT: true
'' == false;
// OUTPUT: true
```

### Conditionals

`if`, `else`, `if else`

ternary operator (if else)
```js 
a === 1 ? console.log(1) : console.log('not 1');
```


### Loops
`for`, `for in`, `for of`, `while`, `do while` and `switch`

### Functions

In JS are first class objects;
They can be assigned name, passed parameter, returned as a result, and ref from an object or array just like any other variable

```js
function name(params0+){
    body 
    zero or more return
        return only 1 
    No type declarations, type inferreed by assignement of value to param
}
```


#### Function params
if paramnot provided, value of param id `undefined`
Function can define default value in function declaration

```js
function labeler(value, title = 'title') {
  console.log(`${title}=${value}`);
}

labeler();
// OUTPUT: title=undefined

labeler('fish');
// OUTPUT: title=fish

labeler('fish', 'animal');
// OUTPUT: animal=fish
```

#### Anonymous Functions
In JS functions are commonly assigned to variable and then passed as param into another function

assigning functions to variables, as well as using functions as parameters and return values.
```js
// Function that takes a function as a parameter
function doMath(operation, a, b) {
  return operation(a, b);
}

// Anonymous function assigned to a variable
const add = function (a, b) {
  return a + b;
};

console.log(doMath(add, 5, 3));
// OUTPUT: 8

// Anonymous function assigned to a parameter
console.log(
  doMath(
    function (a, b) {
      return a - b;
    },
    5,
    3
  )
);
// OUTPUT: 2
```


#### Inner functions
Functions can also be declared inside other functions. This allows you to modularize your code without always exposing private details.

## JS arrow Function
functions are first order objects and can be declared anywhere and passed as params

`arrow` `=>` replaces need for function keyword and enclosing curly braces are optional (if no curly braces single expression returned, else need return)

compact but cannot be used for constructor or iterator generators

### return values
return implied for single expression (no curly braces)

### This pointer
arrow functions inherit `this` pointer from scope in which they are created.. makes `closure`. Closure allows function to ref creation scope even when passed outside of scope

## JSON
### Format

A JSON document contains one of the following data types:

| Type    | Example                 |
| ------- | ----------------------- |
| string  | "crockford"             |
| number  | 42                      |
| boolean | true                    |
| array   | [null,42,"crockford"]   |
| object  | {"a":1,"b":"crockford"} |
| null    | null                    |


Most commonly, a JSON document contains an object. Objects contain zero or more key value pairs. The key is always a string, and the value must be one of the valid JSON data types. Key value pairs are delimited with commas. Curly braces delimit an object, square brackets and commas delimit arrays, and strings are always delimited with double quotes.

Here is an example of a JSON document.

```json
{
  "class": {
    "title": "web programming",
    "description": "Amazing"
  },
  "enrollment": ["Marco", "Jana", "فَاطِمَة"],
  "start": "2025-02-01",
  "end": null
}
```

JSON is always encoded with [UTF-8](https://en.wikipedia.org/wiki/UTF-8). This allows for the representation of global data.

### Converting to JavaScript

You can convert JSON to, and from, JavaScript using the `JSON.parse` and `JSON.stringify` functions.

```js
const obj = { a: 2, b: 'crockford', c: undefined };
const json = JSON.stringify(obj);
const objFromJson = JSON.parse(json);

console.log(obj, json, objFromJson);

// OUTPUT:
// {a: 2, b: 'crockford', c: undefined}
// {"a":2, "b":"crockford"}
// {a: 2, b: 'crockford'}
```

Note that in this example, JSON cannot represent the JavaScript `undefined` object and so it gets dropped when converting from JavaScript to JSON.


## JS object and classes
JS object represents collection of name value pairs referred to as properties. Objects have common object-oriented functionality such as constructors, `this` pointer, static properties and functions, inheritance

Property NAME must be of tye String or Symbol: VALUE any type

objects created with new operator . calls objects constructor
const obj = new Object({a:3})
once declared you can add properties by simply referencing name in assignment. Any type of variable can be assigned to property including sub-object, array, function

obj.prop or obj['prop']

### object-literals
this syntax allows you to provide initial composition of object
```js
const obj = {
  a: 3,
  b: 'fish',
};
```
### obj functions
several intersting static functions. some common ones:
```js
const obj = {
  a: 3,
  b: 'fish',
};

console.log(Object.entries(obj));
// OUTPUT: [['a', 3], ['b', 'fish']]
console.log(Object.keys(obj));
// OUTPUT: ['a', 'b']
console.log(Object.values(obj));
// OUTPUT: [3, 'fish']
```

### constructor
any function that returns an object is considered a `constructor` and can be invoked with `new` operator:

```js
function Person(name) {
  return {
    name: name,
  };
}

const p = new Person('Eich');
console.log(p);
// OUTPUT: {name: 'Eich'}
```

function Person(name) {
  return {
    name: name,
    log: function () {
      console.log('My name is ' + this.name);
    },
  };
}

const p = new Person('Eich');
p.log();
// OUTPUT: My name is Eich


### Classes
classes look similar to declaraing na object but have explicit constructor and assumed function delcarations

you can make properties and functions private by prefixing them with `#`

#### Inheritance
    classes can be extended by using `extends` keyword to define inheritanc
    Parameters passed to parent class are deliverd using `super` function -- calls parent constructor
    any functions defined on child of same name of parent function override parents implementation
    A parent's function can be explicitly accessed using `super` keyword

## JS regEx

You can create a regular expression using the class constructor or a regular expression literal.

second arg represents flag, /regex/flag (such as i - case insensitive)
```js
const objRegex = new RegExp('ab*', 'i');
const literalRegex = /ab*/i;
```

## JS rest and spread

### Rest -- varaiadic functions
sometimes you want function to take unkown number of param
`rest` syntax -- think of a paramter that contains the rest of parameters passed to function. 
function(param1, ...lastParam)  last param is turned into an array that contains the rest of params (only last param to know what paramaters to combine)

### Spread
    spread does opposite of rest. takes an object that is iterable (e.g. array or string) and expands it into a functions params

functionCall(...[item1, item2])


## JS Exceptions

JS supports exception handling using `try catch` and `throw` syntax.

exception triggered by coded `throw` keyword or runtime generation (ex: undef)

```js
try {
  // normal execution code
  // if exception, code following throw is ignored, call stack unwound, catch block called
} catch (err) {
  // exception handling code
} finally {
  // always called code
}
```

### Fallbacks
normal path in try blcok fallback in catch -- so that something is always returned

Example:
```js
function getScores() {
  try {
    const scores = scoringService.getScores();
    // store the scores so that we can use them later if the network is not available
    window.localStorage.setItem('scores', scores);
    return scores;
  } catch {
    return window.localStorage.getItem('scores');
  }
}
```
## JS Destructuring
DESTRUCTURING, NOT DESTRUCTING

pulling individual items out of an existing one, aka removing structure.
*for arrays or obj*

example:
```js
const a = [1, 2, 4, 5];

// destructure the first two items from a, into the new variables b and c
const [b, c] = a;

console.log(b, c);
// OUTPUT: 1, 2


const [b, c, ...others] = a;

console.log(b, c, others);
// OUTPUT: 1, 2, [4,5]
```



ou can also combine multiple items from the original object using rest syntax.

```js
const [b, c, ...others] = a;

console.log(b, c, others);
// OUTPUT: 1, 2, [4,5]
```

This works in a similar manner for objects, except with arrays, the assignment of the associated value was assumed by the positions in the two arrays. When destructuring objects, you explicitly specify the properties you want to pull from the source object.

```js
const o = { a: 1, b: 'animals', c: ['fish', 'cats'] };

const { a, c } = o;

console.log(a, c);
// OUTPUT 1, ['fish', 'cats']
```

You can also map the names to new variables instead of just using the original property names.

```js
const o = { a: 1, b: 'animals', c: ['fish', 'cats'] };

const { a: count, b: type } = o;

console.log(count, type);
// OUTPUT 1, animals
```

Default values may also be provided for missing ones.

```js
const { a, b = 22 } = {};
const [c = 44] = [];

console.log(a, b, c);
// OUTPUT: undefined, 22, 44
```

Note that all of the above examples created new constant variables, but you can also use destructuring to reassign existing variables.

```js
let a = 22;

[a] = [1, 2, 3];

console.log(a);
// OUTPUT: 1
```
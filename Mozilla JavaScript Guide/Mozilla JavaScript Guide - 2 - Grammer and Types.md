# [Grammar and types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#react-container)

## [Basics](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Basics)

---

Is a semicolon needed after a statement?

> Not if it is on its own line, but it is considered best practice to end every statement with a semicolon.

---

Does JavaScript use the ASCII or Unicode character set?

> Unicode

---

Is JavaScript case-sensitive?

> Yes

---

## [Comments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Comments)

---

What are the two styles of comments in JavaScript?

> ```js
> // this is a one line comment
> 
> /* this is
>  * a multi-line comment
> */
> ```

---

## [Declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Declarations)

---

What are the 3 types of variable declarations JavaScript and their scopes?

> - `var` - global or local/function
> - `let` - block-scoped, local variable
> - `const` - block-scoped, read-only constant 

---

### [Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Variables)

---

What is an identifier in JavaScript?

> The name of a variable.

---

What characters can an identifier start with in JavaScript?

> Underscore ( `_` ), dollar sign ( `$` ), or a letter ( `a-z`, `A-Z` )

---

### [Declaring variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Declaring_variables)

---

Two main ways of declaring variables in JavaScript

> `var`, ex. `var x = 42`. Scope is **local** or **global** depending on *execution context*.
> `const` or `let`, ex. `let x = 42`. **Block-scope** local.

---

Can you have undeclared variables in JavaScript?

> Yes, ex. `x = 42` will create an *undeclared global variable* (as long as `x` wasn't declared earlier in the same scope), 
> but use of *undeclared global variable* is strongly discouraged and will result in a strict JavaScript warning.

---

### [Evaluating variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Evaluating_variables)

---

What is the value of a declared variable that hasn't been assigned a value, ex. `var x;`

> Value of `x` is `undefined`

---

Console log the string `What?` if `var foo` is `undefined`

> ```js
> if (foo === undefined) {
>     console.log("What?");
> }
> ```

---

`y` is a variable that has *NOT* been declared. What is the result of `console.log(y)`?

> `ReferenceError: y is not defined` - `ReferenceError` exception is thrown

---

`y` is a variable that has been declared, but *NOT* assigned a value (`var y;`). What is the result of `console.log(y)`?

> `undefined`

---

What is the result of the following code?
```js
var a;
console.log(a + 2)
```

> `NaN` - (`NaN` is Not A Number)

---

What is the result of the following code?
```js
var a;
if (a) {
    console.log("evaluates as true");
} else {
    console.log("evaluates as false");
}
```

> `"evaluates as false"`

---

Are variables that have the value of `undefined` treated as `true` or `false`?

> `false`

---

What is the output of the following code?
```js
var x = null;
console.log(x * 99);
```

> `0` 
> `null` is treated like a zero in a numeric context in JavaScript.

---

Are variables that have the value of `null` treated as `true` or `false`?

> `false`

---

Are variables that have the value of `0` treated as `true` or `false`?

> `false`

---

### [Variable scope](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Variable_scope)

---

Two main types of variable scopes.

> global - declared outside a function
> local - declared inside a function

---

Two types of *local scope* and their declaration keywords.

> *function scope* - `var`
> *block scope* - `let` and `const`

---

What is the output of the following code?
```js
if (true) {
    var x = 5;
}
console.log(x)
```

> `5`

---

What is the output of the following code?
```js
if (true) {
    let y = 5;
}
```

> `ReferenceError: y is not defined` - `ReferenceError` exception is thrown.

---

### [Variable hoisting](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Variable_hoisting)

--- 

What is variable hoisting?

You can refer to variables before they are declared... kind of
More accurately variable declarations are partially handled at compile time
- Variabled declared with `var` will return `undefined` when refered to before declaration
- Vaiables declared with `let` or `const` will result in a `ReferenceError` excpetion when refered to before declaration 

---

Define **hoisting** behavior for `var`, `let` and `const`

> - `var` - hoisted and initialized to `undefined`
> - `let` & `const` - hoisted, but not initialized, referencing before declaration will result in `ReferenceError` exception being thrown

---

What is the result of the following code?
```js
console.log(x);
let x = 3;
```

> `ReferenceError`

---

What is the result of the following code?
```js
console.log(x)
var x = 3;
```

> `undefined`

---

### [Function hoisting](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Function_hoisting)

---

Do function declaration and function expressions get hoisted?

> Only function declarations get hoisted

---

### [Global variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Global_variables)

---

what are global variables a property of (in web pages)?

> The "global object*, The window or frame they were declared in

---

### [Constants](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Constants)

---

How does `const` differ from `let`?

> A constant cannot change value through assignment or be re-declared while the script is running. It must be initialized to a value.

---

Are properties of objects assigned to a constant (`const`) prottected from being changed?

No

---

## [Data structures and types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Data_structures_and_types)

### [Data types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Data_types)

---

List the 8 data types in JavaScript

> - Seven data types that are primitives:
>   - Boolean. `true` and `false`.
>   - `null`. A special keyword denoting a null value. Because JavaScript is case-sensitive, null is not the same as Null, NULL, or any other variant.
>   - `undefined`. A top-level property whose value is not defined.
>   - Number. An integer or floating point number. For example: 42 or 3.14159.
>   - BigInt. An integer with arbitrary precision. For example: 9007199254740992n.
>   - String. A sequence of characters that represent a text value. For example: "Howdy"
>   - Symbol (new in ECMAScript 2015). A data type whose instances are unique and immutable.
> - and Object

---

Define `Objects` and `functions` in JavaScript.

> You can think of objects as named containers for values, and functions as procedures that your application can perform.

---

### [Data type conversion](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Data_type_conversion)

---

Is JavaScript dynamically or statically typed?

> Dynamically

---

What does it mean that JavaScript is dynamically typed?

> It means you don't have to specify the data type of a variable whey you declare it.

---

What is the result of the following code?
```js
console.log('40' + 2);
```

> `"402"`

---

### [Converting strings to numbers](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Converting_strings_to_numbers)

---

Convert the string '101' representing a binary number to an integer in JavaScript.

> `parseInt('101', 2);`

---

Convert the string '999' representing a base 10 number to an integer in JavaScript.

> `parseInt('999', 10);`

---

Convert the string '1.333' to a float in JavaScript.

> `parseFloat('1.333')`

---

What operator in JavaScript can be used to convert a string to a number?

> the `+` (unary plus) operator
> ```js
> +'5' - +'5'; // 0
> ```

---

## [Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Literals)

---

What are literals in JavaScript?

> Literals represent values in JavaScript. They are fixed values, not variables, that you literally provide in your script.
> Examples: `5`, `-1.33`, `true`, `false`,  `"This is a string litereal"`

---

### [Array literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Array_literals)

---

What is an array literal

> An array literal is a list of zero or more expressions, each of which represents an array element, enclosed in square brackets (`[]`).
> Example: `['red', 'white', 'blue']`

---

#### [Extra commas in array literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Extra_commas_in_array_literals)

---

What is the value of the third element in the following array? What is the length of the array?
```js
let a = [ , 'red', , 'blue', , ];
```

> The 1st, **3rd**, 4th, and 5th elements are `undefined`. The length of the array is `6`, the "trailing" comma is ignored. 

---

### [Boolean literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Boolean_literals)

---

What are the two literal values of the Boolean type?

> `true` and `false`

---

### [Numeric literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Numeric_literals)

---

What are the leading characters for decimal, octal, hexadecimal, and binary numeric literals?

> decimal - no special characters and no leading `0` for decimal
> octal - leading `0`, `0o`, or `0O`
> hexadecimal - leading `0x` or `0X`
> binary - leading `0b` or `0B`

---

### [Floating-point literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Floating-point_literals)

---

Syntax for floating point literal

> Syntax...
> ```
> [(+|-)][digits].[digits][(E|e)[(+|-)]digits]
> ```
> Examples...
> ```js
> 3.1415926
> -.123456789
> -3.1E+12
> .1e-23
> ```

---


### [Object literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Object_literals)

---

What is an object literal?

> An object literal is a list of zero or more pairs of property names and their associated values enclosed in curly braces ( `{}` ).
> Example: `{ fname: 'foo', lname: 'bar' }`

---

Can you use numeric literal (number) for an object propterty names?

> Yes. Example: `{ 77: 'seventyseven' }`

---

Two methods for accessing properties of an object are?

> Two methods are dot (`.`) and array-like notation (`[]`).
> Example: `console.log(user.fname)` and `console.log(user['fname'])` are equivalent 

---

What is required to use dot (`.`) notation to access an objects property?

> The property name must be a able to act as a valide identifier (starts with an `_`, `$`, or letter).
> ```js
> let user = { seven: 'SEVEN', 7: 7 }
> console.log(user.seven); // "SEVEN"
> console.log(user['seven']); // "SEVEN"
> console.log(user.7); // SyntaxError
> console.log(user[7]); // 7
> ```

---

#### [Enhanced Object literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Enhanced_Object_literals)

### [RegExp literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#RegExp_literals)

---

What is the syntax for a regex literal?

> A pattern inbetween two slashes. Example: `var re = /ab+c/;`

---

### [String literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#String_literals)

#### [Using special characters in strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Using_special_characters_in_strings)

#### [Escaping characters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types#Escaping_characters)

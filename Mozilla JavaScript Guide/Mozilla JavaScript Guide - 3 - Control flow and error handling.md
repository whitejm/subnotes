# Control flow and error handling

## [Block statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Block_statement)

---

What is a block statement?

> 0 or more statements grouped together inside curly braces `{ }`

---

### [**Example**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Example)

---

Give an example of a control flow statement (`if`) paird with a block statement

> ```js
> if (true) {
>     console.log('True')
> }
> ```

---

## [Conditional statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Conditional_statements)

---

What is a conditional statement?

> A set of commands that execut if a specified condition is true

---

What are the two types of of conditional statements in JavaScript?

> `if...else` and `switch`

---

### [`if...else` statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#if...else_statement)

---

Write an `if...else` statements that console logs `A` if variable `a` is `true`, 
logs `B` if variable `b` is `true` and `a` is `false`, 
logs `neither` if `a` and `b` are both `false` 

> ```js
> if (a) {
>     console.log("A");
> } else if (b) {
>     console.log("B");
> } else {
>     console.log("neither");
> }
> ```
---

#### [Falsy values](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Falsy_values)

---

List 6 *Falsy* values in JavaScript

> ```js
> false
> undefined
> null
> 0
> NaN
> "" (empty string)
> ```
---

#### [**Example**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Example_2)

### [`switch` statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#switch_statement)

---

given a variable `food` write a switch statement that console logs `"fruit"`, `"vegetable"`, or `"I don't know"` appropriately.
`food` will be one of the following fruits of vegetables or something other then a fruit or vegetable.
- apple
- banana
- carrot

> ```js
> switch  (food) {
>   case "apple":
>   case "banana":
>     console.log("fruit");
>     break;
>   case "carrot":
>     console.log("vegetable");
>     break;
>   default:
>     console.log("I don't know");      
> }
> ```
> *Note: default doesn't have to be on bottom, but that is convention. If it was above other cases it would then need a `break` statement.*
---

#### [**Example**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Example_3)

## [Exception handling statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Exception_handling_statements)

### [Exception types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Exception_types)

### [`throw` statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#throw_statement)

### [`try...catch` statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#try...catch_statement)

#### [The `catch` block](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#The_catch_block)

#### [The `finally` block](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#The_finally_block)

#### [Nesting try...catch statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Nesting_try...catch_statements)

### [Utilizing `Error` objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Utilizing_Error_objects)
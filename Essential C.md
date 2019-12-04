# Essential C
http://cslibrary.stanford.edu/101/EssentialC.pdf

## Basic Types and Operators

TODO

## Control Structures

TODO

## Complex Data Types

### Structs
___

declare a struct called 'node' with an int ("data")
and and a pointer a node ("next")

```c
struct node {
    int data;
    struct node* next;
}
```
___

### Arrays

declare a 5x5 two deminsional array of integers and assign last element to `7`

```c
int a [5][5];
a[4][4] = 7;
```

### Pointers
___

What is the `*` unary operator called and used for?  
ex. `int* v;`, `*v = x`, `*v = 42`, `y = *v`

dereference operator, declare pointer or dereference it 
derefernceing references value at the pointer address instead the address itself
inverse of the 'address of operator' `&`
___

What is the `&` unary operator called and used for?  
ex. `p = &i`

"address of" opereator, returns address of a variable/structure
example.
```c
int x;
x = 42;
int* y;
y = &x;
/*  *y = 42  */
```
___

what should pointers with no pointee be assigned?

`NULL` (aka `0`)
___

3 steps for pointer/pointee relationship to work

1. the pointer must be declared/allocated
2. the pointee must be declared/allocated
3. the pointer must be initialized so that it points to the pointee
___

what is wrong with this code?...  
```c
int* p;
*p = 13;
```

pointer `p` doesn't point to anything yet. you just wrote `13` to random area in memory
```c
int x = 12;
int* p = &x;
*p = 13;
/* x now equals 13 */
```
___

### Strings
___

what are c strings?

arrays of characters (`char`) with a "null" `char` (`\0`) at the end
___

make a string (char array) and set it to "foobar"

```c
char mystring[10];
strcpy(mystring, "foobar") 
/* mystring is now [f][o][o][b][a][r][\0][?][?][?] */
```
___

function to get string len and a caution 

`strlen(mystring)` returns length, but it doesn't include null `char` (`\0`) 
___

## Functions

TODO

## Odds and Ends

### Prototypes
___

what is a prototype in c?

function name and arguments without the body. Examples...
```c
static int Double(int num);
void sayhi(const char* name);
```
___

what kind of functions don't need prototypes?

static functions, as long as they are declared/defined before use in their file.
___

### Preprocessor

---

describe `#define` directive

> sets up a symbolic replacement in the source (#define find_this replace_with_this).
> Example... `#define MAX 99`, `#define MIN 0`, `#define FALSE 0`

---

describe `#include` directive

> pasts in text from other file, often used to include header files 

---

include system header file foo.h

> `#include <foo.h>`

---

include 'user' header file foo.h from originating compile dir

> `#include "foo.h"`

---

convention for *.h *.c files

> `foo.h` has prototypes for `foo.c` non static functions, `foo.c` has the 
> function definitions.

---

`bar.c` wants to call a function from `foo.c`, describe files and directives involved

> - function would have prototype in `foo.h`
> - `foo.c` has function definition
> - `foo.c` and `bar.c` have `#include "foo.h"` directive at begining of file

--------------------------------------------------------------------------

give an example using `#define` `#if`, `#else` derectives...

> ```C
> #define SWITCH 1
> 
> #if SWITCH
>     /* this code compiles */
>     int a;
> #else
>     /* this code does not */
> #endif
> ```

--------------------------------------------------------------------------

directive to prevent multiple `#includes` of the same file 
(and where it should go)...

> `#pragma once` should be placed at top of `.h` file

--------------------------------------------------------------------------

write a short file that uses assert to veryfi that `int v` is `>= 0` and `<= 10` 

> ```c
> #include <assert.h>
> int v = 3;
> assert(v>=0);
> assert(v<=10);
> ```

--------------------------------------------------------------------------

## Advanced Arrays and Pointers

**TODO**

## Operators and Standard Library Reference

**TODO**



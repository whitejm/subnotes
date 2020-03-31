# Python Exceptions: An Introductions

https://realpython.com/python-exceptions/

---

What two statements can be used to throw an exception?
Use both methods to throw exception if `x` is `False`.

> `raise` and `assert` 
> ```python
> if not x:
>   raise Exception("x is False")
> ```
> `Exception: x is False`
>
> ```python
> assert (x), "x is False")
> ```
> `AssertionError: x is False`

---

What is used to catch and handle exceptions?

> the `try` and `except` block

---

write a program to divide by `0` and log exception.

> ```python
> import logging
> try:
>   # run this code
>   0/0
> except Exception as e:
>   # run this code if there is an exception in try block
>   l

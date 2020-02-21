# Python Modules and Packages - An Introduction

https://realpython.com/python-modules-packages/


---

what are two mechanisms that support modular programing in python? (Think higher then class or functions)

> modules and packages

---

3 ways to define modules

> - Pure python (ex `mymod.py` file)
> - C that is loaded at runtime (ex, `re` module is written in C)
> - built in module (ex, `itertools`)

---

How are a module's contents accessed in python?

> with the `import` statement. ex `import mymodule`

---

print the module search path

> ```python
> import sys
> print(sys.path)
> ```

---

4 ways of importing modules (2 involve renaming)

> ```
> import <module_name>
> from <module/package_name> import <name(s)>
> import <module_name> as <alt_name>
> from <module/package_name> import <name> as <alt_name>
> ```

---

How would you call `mod1`'s `foo()` with the import statements `import mod1` and `from mod1 import foo`?

> ```python
> import mod1
> mod1.foo()
> ```
> ```python
> from mod1 import foo
> foo()
> ```

---

Safely try to import module `foo`

> ```python
> try:
>   import foo
> except ImportError:
>   print("couldn't import foo")
>   exit()
> ```

---

what does `dir()` do?

> returns list of defined names in a namespace
> with out arguments this is the local namespace

---

write a program to print out names in the module `mod`

> ```python
> import mod
> print(dir(mod))
> ```

---

You have code in a module you do NOT want to execute if it is being
imported and not run directly. How do you do this?

> ```python
> if (__name__ == '__main__'):
>   # code here won't run on import
> ```

---

modules vs packages

> Modules are usually files, ex `mod1.py`, `mod2.py`.
> A package is a folder containing modules

---

If there is some code you want executed when a package is imported where would it go?

> `__init__.py` file in the package folder

---

in `from MODorPKG import *` what defines what the asterisk refers to?

> the `__all__` list defined in the module or `__init__.py` for the package

---

what is a subpackage?

> another package folder under the main package folder

---

import the `Capital` module from the `Country` package

- Country - pkg dir
  - State - sub pkg dir
    - Capital.py - module

> `from Country.State import Capital`

---

Can modules in a package import from other sibling modules in same package?

> yes

---






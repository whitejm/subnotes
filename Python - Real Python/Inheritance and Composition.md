# Inheritance and Composition

https://realpython.com/inheritance-composition-python/

---

What are Inheritance and Composition

> Two major concepts in OOP that model the relationship between two classes
> - Inheritance: **is a** relationship. A **derived** class *is a* specialized version of **base** class
> - Composition: **has a** relationship. A **composite** class *has a* **component** class

---

Name of classes that inherit from another class

> subclass or derived class

---

Name of a class that a subclass inherits from

> Base class

---

You're making a subclass `SportsCar` from the `Car` class. All `SportsCars` will have 2 `doors`. Write the classes and their constructor.

> ```python
> class Car:
>   def __init__(self, doors=4):
>     self.doors = doors
>
> class SportsCar(Car):
>   def __init__(self):
>     super().__init__(doors=2)
> ```

---

Type of class that you don't instantiate, but instead derive other classes from

> Abstract Base Class. 
>
> ```python
> from abc import ABC
> class Car(ABC):
>    ...
> ```

---

How to declare a method in a Abstract Base Class must to be overridden by a subclass

> Use the `@abstractmethod` decorator on the method. `from abc import ABC, abstractmethod`

---

Describe interface and implementation as it relates to classes and inheritance.

> - *Interface* is a common set of methods, properties, and attributes across multiple classes
> - *Implementation* is the code inside the methods (what implements the interface)
> - Use inheritance to reuse implementation 

---


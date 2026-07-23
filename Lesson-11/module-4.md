# Lesson 11 – Module 4

## Encapsulation, Polymorphism & Abstraction

**Estimated Time:** 35–45 minutes

**Difficulty:** ⭐⭐⭐⭐

---

# Module Objective

By the end of this module you'll understand:

* Encapsulation
* Public, Protected, Private members
* Polymorphism
* Abstraction
* Python-specific OOP conventions

---

# Part 1 – Encapsulation

## What is Encapsulation?

Encapsulation means:

> **Keep data and the methods that operate on it together, and control how that data is accessed.**

You already do this in Magento.

---

## Public Members

Everything is public by default in Python.

```python
class Product:

    def __init__(self):
        self.name = "Laptop"
```

Usage

```python
product = Product()

print(product.name)
```

Output

```text
Laptop
```

---

## Protected Members

Python uses a **convention**.

Single underscore:

```python
self._price = 50000
```

This means:

> "This is intended for internal use."

But Python does **not** prevent access.

Example

```python
print(product._price)
```

Works.

---

## Private Members

Double underscore:

```python
self.__cost = 40000
```

Now

```python
print(product.__cost)
```

raises an `AttributeError`.

Python performs **name mangling** to discourage direct access.

---

## Accessing Private Data

Use methods.

```python
class Product:

    def __init__(self):
        self.__price = 50000

    def get_price(self):
        return self.__price
```

Usage

```python
product = Product()

print(product.get_price())
```

---

# Magento Comparison

PHP

```php
private $price;

public function getPrice()
```

Python

```python
self.__price

def get_price()
```

Same idea, different syntax.

---

# Part 2 – Polymorphism

## What is Polymorphism?

Same method name.

Different behavior.

---

Example

```python
class Animal:

    def sound(self):
        print("Animal Sound")


class Dog(Animal):

    def sound(self):
        print("Woof")


class Cat(Animal):

    def sound(self):
        print("Meow")
```

Usage

```python
animals = [Dog(), Cat()]

for animal in animals:
    animal.sound()
```

Output

```text
Woof
Meow
```

Notice we call the **same method** (`sound`) but get different behavior depending on the object.

---

# Real AI Example

```python
class BaseAgent:

    def run(self):
        pass


class CodingAgent(BaseAgent):

    def run(self):
        print("Generate code")


class ResearchAgent(BaseAgent):

    def run(self):
        print("Search documents")
```

Application

```python
agents = [CodingAgent(), ResearchAgent()]

for agent in agents:
    agent.run()
```

Same method.

Different implementation.

---

# Part 3 – Abstraction

## What is Abstraction?

Abstraction means:

> **Define what must be done, but let child classes decide how to do it.**

Python provides this through the `abc` module.

---

## Abstract Class

```python
from abc import ABC, abstractmethod


class Payment(ABC):

    @abstractmethod
    def pay(self):
        pass
```

---

## Child Class

```python
class CreditCard(Payment):

    def pay(self):
        print("Paid using Credit Card")
```

Usage

```python
payment = CreditCard()

payment.pay()
```

---

## What Happens If You Don't Implement It?

```python
class UPI(Payment):
    pass
```

Trying to create:

```python
UPI()
```

results in:

```text
TypeError
```

because `pay()` hasn't been implemented.

---

# Magento Comparison

PHP

```php
interface PaymentInterface
{
    public function pay();
}
```

Python

```python
class Payment(ABC):

    @abstractmethod
    def pay(self):
        pass
```

> **Note:** Python also has Protocols (`typing.Protocol`), but we'll learn those later. For now, abstract base classes are enough.

---

# Summary

| Concept      | Python                          |
| ------------ | ------------------------------- |
| Public       | `self.name`                     |
| Protected    | `self._name`                    |
| Private      | `self.__name`                   |
| Polymorphism | Same method, different behavior |
| Abstraction  | `ABC` + `@abstractmethod`       |

---

# Exercises

## Exercise 1 – Encapsulation

Create:

```python
class BankAccount
```

Private variable:

```python
__balance
```

Method:

```python
get_balance()
```

Print the balance using the method.

---

## Exercise 2 – Protected Variable

Create:

```python
class Employee
```

Protected variable:

```python
_salary
```

Method:

```python
show_salary()
```

Print the salary.

---

## Exercise 3 – Polymorphism

Create:

```python
class Animal
```

Method:

```python
sound()
```

Create:

* Dog
* Cat

Override `sound()`.

Loop through both objects and call `sound()`.

---

## Exercise 4 – Abstraction

Create an abstract class:

```python
Shape
```

Abstract method:

```python
area()
```

Create:

```python
Square
```

Implement:

```python
area()
```

Print:

```text
Area calculated
```

---

# Mini Project

## Payment Gateway

Create an abstract class:

```python
Payment
```

Method

```python
pay()
```

Create two child classes:

```text
CreditCard

UPI
```

Each implements `pay()` differently.

Store them in a list.

Loop through the list and call:

```python
pay()
```

Expected output:

```text
Paid using Credit Card

Paid using UPI
```

---

# Where You'll Use This in AI

These concepts appear throughout AI frameworks:

```python
class BaseTool(ABC):
    ...

class SearchTool(BaseTool):
    ...

class CalculatorTool(BaseTool):
    ...
```

Or:

```python
class BaseAgent:
    ...

class ResearchAgent(BaseAgent):
    ...

class CodingAgent(BaseAgent):
    ...
```

This is the same architecture used in many AI libraries.

---

# Module Outcome

After this module you'll understand:

* ✅ Encapsulation
* ✅ Public, Protected, Private
* ✅ Polymorphism
* ✅ Abstraction
* ✅ Abstract Classes
* ✅ Python's OOP conventions

---

## Small Interview Tip

If someone asks:

> **"Does Python have true private variables?"**

A good answer is:

> Python doesn't enforce privacy the same way as languages like Java or C++. It uses conventions (`_`) and name mangling (`__`) to discourage direct access, but determined code can still access those attributes. The emphasis is on responsible use rather than strict enforcement.

This answer shows you understand both the language behavior and its design philosophy.

---

⏱️ **Target Time:** **35–45 minutes**

After this, we'll have only **Module 5 (Final Project)** left, and **Lesson 11** will be complete. That means your Python foundation phase will be almost finished, and we'll be ready to move into file handling, exception handling, and eventually APIs and AI-specific development.

# 🚀 Lesson 6 – Variables & Data Types

**Roadmap Position**

* **Phase 1:** Python for AI Engineers
* **Lesson:** 6
* **Goal:** Understand how Python stores and works with data.

---

# Before We Start

I'm going to ask you one question.

Suppose I ask you:

> **What is your name?**

You reply:

> **Bhupendra**

Now after 5 minutes I ask again:

> **What is your name?**

You still answer:

> **Bhupendra**

How did your brain remember it?

Because it **stored** the information somewhere.

A computer works the same way.

---

# What is a Variable?

A **variable** is simply a **named storage location** that holds a value.

Think of it as a labeled box.

```
┌────────────────────┐
│ Name               │
│ Bhupendra          │
└────────────────────┘
```

The label is **name**.

The value inside is **Bhupendra**.

---

# Magento Example

Suppose you have:

```php
$productName = "iPhone 16";
```

What happens?

PHP creates a variable called:

```
$productName
```

and stores:

```
iPhone 16
```

Exactly the same in Python.

```python
product_name = "iPhone 16"
```

Notice two differences:

PHP

```php
$productName
```

Python

```python
product_name
```

### Difference 1

Python has **no `$`**.

---

### Difference 2

Python uses **snake_case**.

PHP/Magento usually uses:

```php
$productName
$customerEmail
$orderId
```

Python convention is:

```python
product_name
customer_email
order_id
```

This is called **snake_case**.

It isn't a language rule—you *can* use `productName`—but following Python conventions makes your code easier for other Python developers to read.

---

# How Does Memory Work?

Suppose we write:

```python
name = "Bhupendra"
```

The computer stores it like this (conceptually):

```
Memory

┌────────────────────┐
│ name               │
│ Bhupendra          │
└────────────────────┘
```

Now write:

```python
city = "Mumbai"
```

Memory becomes:

```
┌────────────────────┐
│ name               │
│ Bhupendra          │
└────────────────────┘

┌────────────────────┐
│ city               │
│ Mumbai             │
└────────────────────┘
```

The computer now remembers both.

---

# Data Types

A computer needs to know **what kind of value** it is storing.

Imagine Magento.

Suppose:

```
Price = 1000
```

Can price be:

```
"Hello"
```

No.

Different values have different meanings.

Python classifies them into **data types**.

---

## 1. String (str)

A string is **text**.

```python
name = "Bhupendra"
```

Examples:

```python
city = "Mumbai"

framework = "Magento"

language = "Python"
```

Everything inside quotes is text.

---

## 2. Integer (int)

Whole numbers.

```python
age = 37

products = 100

quantity = 5
```

No quotes.

---

## 3. Float

Decimal numbers.

```python
price = 999.99

discount = 10.5
```

Notice the decimal point.

---

## 4. Boolean (bool)

Only two values.

```python
True

False
```

Examples:

```python
is_logged_in = True

is_admin = False
```

Think Magento.

```
Customer Logged In?

Yes

No
```

That's a Boolean.

---

# Why Are Data Types Important?

Suppose you write:

```python
age = "37"
```

Notice the quotes.

This is **not** a number.

It is **text**.

Whereas:

```python
age = 37
```

is a number.

Although both *look* similar, Python treats them differently.

---

# Let's Check the Type

Python provides a function:

```python
type()
```

Example:

```python
name = "Bhupendra"

print(type(name))
```

Output:

```python
<class 'str'>
```

Another example:

```python
age = 37

print(type(age))
```

Output:

```python
<class 'int'>
```

---

# PHP Comparison

PHP:

```php
var_dump($name);
```

Python:

```python
print(type(name))
```

Both help you inspect the value's type.

---

# Mini Project

Create a new file:

```
lesson-6.py
```

Write:

```python
name = "Bhupendra"
age = 37
salary = 50000.50
is_magento_developer = True

print(name)
print(age)
print(salary)
print(is_magento_developer)

print(type(name))
print(type(age))
print(type(salary))
print(type(is_magento_developer))
```

---

# Expected Output

```
Bhupendra
37
50000.5
True

<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
```

---

# Challenge 1 (Think Like a Developer)

Tell me the data type of each variable.

```python
customer_name = "John"

order_id = 1001

price = 2500.75

is_paid = False

quantity = 10
```

Don't use Python yet.

Just tell me:

```
customer_name → ?

order_id → ?

price → ?

is_paid → ?

quantity → ?
```

---

# Challenge 2

Which of these are **Strings**?

```python
A = "100"

B = 100

C = "Magento"

D = True

E = 25.6
```

---

# Homework

1. Create `lesson-6.py`.
2. Run it.
3. Paste:

   * Your code.
   * The output.
4. Answer Challenge 1 and Challenge 2.

---

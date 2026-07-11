# **Part 1 – Arithmetic Operators**

We won't move ahead until you fully understand it.

---

# What is an Operator?

An operator tells Python **what action to perform**.

Think of it as a mathematical symbol.

Example:

```text
20 + 10
```

The `+` tells Python:

> Add these two values.

Without operators, Python would simply have values with no instructions about what to do with them.

---

# Real-World Example

Suppose you buy:

* Laptop = ₹50,000
* Mouse = ₹2,000

Your total bill is:

```text
50000 + 2000
```

The `+` operator performs the addition.

Simple.

---

# Magento Example

Suppose a customer buys:

```text
Product Price = ₹1000

Tax = ₹180
```

Python:

```python
total = price + tax
```

Magento does calculations like this all the time for totals, shipping, tax, and discounts.

---

# Arithmetic Operators

| Operator | Meaning        | Example   | Result |
| -------- | -------------- | --------- | -----: |
| `+`      | Addition       | `10 + 5`  |     15 |
| `-`      | Subtraction    | `10 - 5`  |      5 |
| `*`      | Multiplication | `10 * 5`  |     50 |
| `/`      | Division       | `10 / 5`  |    2.0 |
| `%`      | Remainder      | `10 % 3`  |      1 |
| `//`     | Floor Division | `10 // 3` |      3 |
| `**`     | Power          | `2 ** 3`  |      8 |

Don't memorize these yet—we'll understand each one with examples.

---

# Addition (`+`)

```python
a = 20
b = 10

print(a + b)
```

Output:

```text
30
```

---

# Subtraction (`-`)

```python
a = 20
b = 10

print(a - b)
```

Output:

```text
10
```

---

# Multiplication (`*`)

```python
a = 20
b = 10

print(a * b)
```

Output:

```text
200
```

---

# Division (`/`)

```python
a = 20
b = 10

print(a / b)
```

Output:

```text
2.0
```

Notice the result is **2.0**, not **2**.

Why?

Because Python's `/` operator always returns a **float**.

We'll understand why when we discuss numeric types in more depth.

---

# AI Connection

Suppose you're building an AI application that estimates token costs.

```text
Total Tokens = 1500

Price Per 1000 Tokens = ₹0.50
```

You might calculate:

```python
cost = (1500 / 1000) * 0.50
```

Even AI applications use arithmetic every day.

---

# Common Beginner Mistake

Many beginners think:

```python
print(20 / 10)
```

should print:

```text
2
```

But Python prints:

```text
2.0
```

because `/` performs floating-point division.

If you specifically want an integer result, there are other operators (`//`) that we'll learn next.

---

# 🧪 Mini Challenge 1

Without running Python, predict the output.

### Question 1

```python
print(25 + 15)
```

### Question 2

```python
print(50 - 20)
```

### Question 3

```python
print(6 * 8)
```

### Question 4

```python
print(100 / 4)
```

Write only the outputs.

---

# Homework

Create:

```text
lesson-7-part1.py
```

Write:

```python
a = 100
b = 25

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
```

Run it and send me:

1. Your code.
2. The output.
3. The answers to the four mini challenge questions.

---

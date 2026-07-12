# Lesson 8 – Module 2: `for` Loop

**Estimated Time:** 60–75 Minutes

## Learning Objectives

By the end of this module, you will be able to:

* Understand what a `for` loop is.
* Write your own `for` loops.
* Understand the loop variable.
* Understand how `range()` works.
* Predict the output of a `for` loop.
* Compare Python `for` loops with PHP `foreach`.
* Understand where AI agents use `for` loops.

---

# 1. What is a `for` Loop?

A `for` loop is used when Python needs to perform the **same task for every item in a collection** or **repeat a task a known number of times**.

Think of it as telling Python:

> "Do this once for each item."

Examples:

* Print numbers from 1 to 10.
* Print every product in Magento.
* Read every line in a file.
* Process every page of a PDF.
* Summarize every customer review.

Notice something common?

We already know **how many items** (or at least what collection) we're working with.

That's where `for` is the best choice.

---

# 2. Basic Syntax

```python
for variable in sequence:
    # code to repeat
```

Let's understand each part.

```python
for
```

This tells Python:

> "Start a loop."

---

```python
variable
```

This is called the **loop variable**.

It stores the current value during each iteration.

Example:

```python
for i in range(5):
```

Here,

```python
i
```

changes automatically.

First iteration

```text
i = 0
```

Second

```text
i = 1
```

Third

```text
i = 2
```

until the loop finishes.

---

# 3. What is `range()`?

`range()` is a built-in Python function that generates a sequence of numbers.

For now, remember these two forms:

```python
range(5)
```

Produces:

```text
0 1 2 3 4
```

Notice:

It **starts at 0**.

It **stops before 5**.

---

Another example:

```python
range(1, 6)
```

Produces:

```text
1 2 3 4 5
```

Rule:

```text
range(start, stop)

Start → Included

Stop → Excluded
```

This "stop is excluded" rule is one of the most important things to remember in Python.

---

# 4. First Example

```python
for i in range(5):
    print(i)
```

Output:

```text
0
1
2
3
4
```

---

# 5. How Python Executes This

Imagine Python running:

```python
for i in range(5):
    print(i)
```

Internally, it's similar to:

```text
Iteration 1

i = 0

↓

print(0)

-----------------

Iteration 2

i = 1

↓

print(1)

-----------------

Iteration 3

i = 2

↓

print(2)

-----------------

Iteration 4

i = 3

↓

print(3)

-----------------

Iteration 5

i = 4

↓

print(4)

Loop Ends
```

Python automatically updates `i` for each iteration.

You don't have to do it manually.

---

# 6. Printing Something Multiple Times

Suppose you want:

```text
Welcome
Welcome
Welcome
```

Code:

```python
for i in range(3):
    print("Welcome")
```

Output:

```text
Welcome
Welcome
Welcome
```

Notice that `i` isn't used.

We'll discuss the `_` convention later as a Python best practice.

For now, using `i` is perfectly fine while you're learning.

---

# 7. Printing 1 to 10

```python
for i in range(1, 11):
    print(i)
```

Output:

```text
1
2
3
4
5
6
7
8
9
10
```

Again,

`11` isn't printed because the stop value is excluded.

---

# 8. Magento Comparison

PHP:

```php
foreach ($products as $product) {
    echo $product->getName();
}
```

Python:

```python
for product in products:
    print(product.name)
```

Notice the similarity:

* One product at a time.
* Same block of code.
* Loop ends automatically after the last product.

---

# 9. AI Agent Example

Suppose an AI agent receives 100 customer reviews.

Conceptually:

```python
for review in reviews:
    analyze(review)
```

Execution:

```text
Review 1

↓

Analyze

↓

Review 2

↓

Analyze

↓

...

↓

Review 100

↓

Analyze

↓

Done
```

This is one of the most common patterns in AI systems.

---

# 10. Common Beginner Mistakes

### Mistake 1

Expecting:

```python
range(5)
```

to produce

```text
1 2 3 4 5
```

It doesn't.

It produces:

```text
0 1 2 3 4
```

---

### Mistake 2

Thinking the stop value is included.

Example:

```python
range(1,5)
```

Many beginners expect:

```text
1 2 3 4 5
```

Actual output:

```text
1 2 3 4
```

The stop value is **always excluded**.

---

### Mistake 3

Trying to change the loop variable manually.

Example:

```python
for i in range(5):
    i = 100
```

Python will still control the next iteration.

The loop variable is managed by the loop itself.

---

# Senior Developer Tip

Don't memorize `range()`.

Understand its behavior.

If you know:

> **Start is included, stop is excluded**

you can predict almost every `range()` result correctly.

---

# Exercises

Now we'll practice **only what we've learned in this module**.

### Exercise 1

Print:

```text
Python
```

exactly **5 times**.

---

### Exercise 2

Print numbers from **1 to 20**.

---

### Exercise 3

Print numbers from **0 to 9**.

---

### Exercise 4

Without running the code, predict the output:

```python
for i in range(2, 6):
    print(i)
```

---

### Exercise 5

Without running the code, predict the output:

```python
for i in range(3):
    print("AI")
```

---

# Module Summary

Today you learned:

* ✅ What a `for` loop is.
* ✅ Loop syntax.
* ✅ Loop variable.
* ✅ `range(start, stop)`.
* ✅ Why the stop value is excluded.
* ✅ Python execution flow.
* ✅ Magento `foreach` comparison.
* ✅ AI agent usage.

---

**Complete these five exercises and send me your answers.**

If you solve them correctly, we'll move directly to the next part of Module 2, where we'll extend `for` loops to work with **strings** and then introduce **nested `for` loops** before moving on to the module's mini project. This keeps everything within Module 2 without introducing concepts from later modules.

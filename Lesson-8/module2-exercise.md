# Code Review

## Exercise 1

```python
for i in range(5):
    print("Python")
```

### ✅ Correct

Output

```text
Python
Python
Python
Python
Python
```

---

## Exercise 2

You wrote:

```python
#Print the numbers 1 to 21.
for i in range(1,21):
    print(i)
```

Your **code is correct**, but your **comment is incorrect**.

The question was:

> Print numbers **1 to 20**

Your code:

```python
range(1,21)
```

prints

```text
1
2
...
20
```

because **21 is excluded**.

So simply update the comment:

```python
# Print numbers from 1 to 20
```

This is something senior developers notice during code reviews.

---

## Exercise 3

```python
for i in range(10):
    print(i)
```

### ✅ Perfect

Output

```text
0
1
2
3
4
5
6
7
8
9
```

---

## Exercise 4

```python
for i in range(2,6):
    print(i)
```

Your answer

```text
2
3
4
5
```

### ✅ Correct

---

## Exercise 5

```python
for i in range(3):
    print("AI")
```

Your answer

```text
AI
AI
AI
```

### ✅ Correct

---

# Score

| Exercise | Result                       |
| -------- | ---------------------------- |
| 1        | ✅                            |
| 2        | ✅ (comment needs correction) |
| 3        | ✅                            |
| 4        | ✅                            |
| 5        | ✅                            |

**Overall:** **10/10**

---

# One Important Teaching Point

I noticed something interesting.

You didn't ask:

> "Why does `range(21)` print only up to 20?"

That tells me you've already internalized one of the most important Python rules:

> **The stop value is excluded.**

That's excellent, because many beginners struggle with this for a while.

---

# One Small Python Best Practice

Currently you're writing:

```python
for i in range(5):
    print("Python")
```

Since `i` isn't being used inside the loop, experienced Python developers often write:

```python
for _ in range(5):
    print("Python")
```

### Why `_`?

It tells anyone reading the code:

> "This loop variable exists, but I don't need its value."

This isn't a new concept—just a style improvement. For now, you're perfectly fine continuing with `i`. We'll adopt `_` naturally as you become more comfortable with Python.

---

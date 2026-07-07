# Your Prompt

```text
Role: Generate

Task: Professional description

Context: for product

Rules: for mobile phone only

Output: show the product description in professional manner as per mobile phone
```

## Score: **7/10** ⭐

You have the correct structure, but let's understand what each part should contain.

---

# What is "Role"?

You wrote:

```text
Role: Generate
```

Think about a company.

If you're hiring someone, would you say:

> Your role is "Generate"

❌ No.

You would say:

* Senior Magento Developer
* Content Writer
* Marketing Expert
* Product Copywriter
* SEO Expert

A **Role** tells the AI **who it should pretend to be**.

Examples:

```text
Role:
Professional Product Copywriter
```

or

```text
Role:
Senior Marketing Manager
```

or

```text
Role:
E-commerce Product Description Expert
```

---

# What is "Task"?

You wrote:

```text
Professional description
```

The task is **what you want the AI to do**.

Better:

```text
Generate a professional product description.
```

Notice it's an action.

---

# What is "Context"?

You wrote:

```text
for product
```

Imagine someone says:

> Write a product description.

You'd immediately ask:

> Which product?

That's what **Context** provides.

Example:

```text
Product:
iPhone 16 Pro

Color:
Black

Storage:
256GB

Features:
A18 Chip
48MP Camera
6.3-inch OLED Display
```

The AI now knows what it's writing about.

---

# What are "Rules"?

You wrote:

```text
for mobile phone only
```

That's more like context.

Rules are constraints.

For example:

```text
Use professional English.

Do not exaggerate.

Keep it under 150 words.

Highlight key features.

Do not use emojis.
```

Rules tell the AI **how** to perform the task.

---

# What is "Output"?

You wrote:

```text
show the product description in professional manner
```

This is close, but the output should specify the format.

Examples:

```text
Return only the product description.
```

or

```text
Return:

Title

Short Description

Bullet Points
```

Now the AI knows how to organize its response.

---

# Here's the Improved Prompt

```text
Role:
You are an experienced e-commerce product copywriter.

Task:
Generate a professional product description.

Context:
Product: Samsung Galaxy S25
Storage: 256GB
Color: Titanium Black
Display: 6.7-inch AMOLED
Camera: 50MP
Battery: 5000mAh

Rules:
Use professional English.
Keep the description under 150 words.
Highlight the key features.
Do not exaggerate or include false claims.

Output:
Return a product title, a short product description, and five bullet points highlighting the main features.
```

See how each section has a different purpose?

---

# Here's an Analogy You'll Never Forget

Imagine you're hiring someone.

## Role

Who are you hiring?

```text
Senior Magento Developer
```

---

## Task

What work should they do?

```text
Build a custom module.
```

---

## Context

What information do they need?

```text
Adobe Commerce 2.4.8

Customer Module

PHP 8.3
```

---

## Rules

How should they do it?

```text
Use Dependency Injection.

Use Repository Pattern.

Follow Magento Coding Standards.
```

---

## Output

What do you expect to receive?

```text
Folder Structure

Code

Explanation
```

That's exactly how prompting works.

---

# 🎉 Congratulations!

You have now learned something that many people using AI every day don't understand:

> **A prompt is not just a question. It's a complete set of instructions.**

---

# Tomorrow We'll Build Your First AI Chatbot

Up to now we've only built your understanding.

In the next lesson, we'll finally write code.

We'll build a simple chatbot in about **20–30 lines of Python**.

You'll learn:

* What an API key is
* How your Python program talks to an LLM
* What an HTTP request is
* How the LLM sends a response back
* How your chatbot displays the answer

No frameworks.

No LangChain.

No AI Agents.

Just one Python file so you understand **exactly** what's happening.

---

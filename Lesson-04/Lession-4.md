# AI Agent Course for Developers

# Lesson 4 - Build Your First AI Chatbot

## Goal

By the end of this lesson, you'll understand:

* What an API is in practice
* What an API Key is
* How Python talks to an LLM
* What happens when you click "Send"
* How the LLM returns an answer

---

# First, Let's Understand the Architecture

Imagine you're on ChatGPT.

You type:

> Hello

Internally, something like this happens:

```text
You

↓

Browser

↓

OpenAI API

↓

LLM

↓

OpenAI API

↓

Browser

↓

You
```

Notice something?

The browser **never talks directly to the LLM**.

It talks to the **OpenAI API**.

The API forwards the request to the model.

---

# Magento Example

Suppose your customer clicks:

```text
Generate Product Description
```

What happens?

```text
Browser

↓

Magento Controller

↓

Magento Service

↓

OpenAI API

↓

LLM

↓

Magento Service

↓

Magento Controller

↓

Browser
```

Does this architecture remind you of Magento?

It should!

Instead of:

```text
Controller

↓

Repository

↓

Database
```

we now have:

```text
Controller

↓

OpenAI API

↓

LLM
```

The pattern is still **Request → Process → Response**.

---

# What is an API Key?

Imagine OpenAI is your office.

Can anyone walk in?

No.

They need an ID card.

An API key is like this:

```text
Office

↓

Security Guard

↓

Show ID Card

↓

Enter
```

The API Key is your ID card.

Without it:

```text
Request

↓

❌ Unauthorized
```

With it:

```text
Request

↓

✅ Allowed
```

---

# Why Keep the API Key Secret?

Imagine someone steals your ATM card.

They can spend your money.

Similarly, if someone gets your API key, they could make requests using your account.

That's why API keys stay on the **backend**, never in frontend JavaScript.

---

# How a Python Program Talks to an LLM

Imagine this simple flow:

```text
Python Program

↓

API Request

↓

OpenAI Server

↓

LLM

↓

Response

↓

Python Program

↓

Print Answer
```

That's all.

No magic.

---

# The Simplest AI Program

This isn't real code yet. It's just the idea.

```text
Ask Question

↓

Send Question

↓

Receive Answer

↓

Print Answer
```

That's a chatbot.

---

# Now Let's See Real Python Code

Don't worry if you've never used Python.

I'll compare it to PHP.

### Python

```python
question = input("Ask something: ")

print(question)
```

### PHP Equivalent

```php
$question = readline("Ask something: ");

echo $question;
```

See?

Very similar.

---

# Sending a Request

Your Python program sends:

```text
{
   "question":
   "What is Magento?"
}
```

to OpenAI.

OpenAI replies:

```text
{
   "answer":
   "Magento is an open-source ecommerce platform..."
}
```

Your program prints the answer.

That's it.

---

# What Happens Behind the Scenes?

Suppose you ask:

> Explain Dependency Injection.

Step 1

```text
Python

↓

Creates Request
```

Step 2

```text
Internet

↓

OpenAI API
```

Step 3

```text
LLM

↓

Generates Response
```

Step 4

```text
Python

↓

Print()
```

Done.

---

# Think Like a Magento Developer

Imagine this PHP code:

```php
$product = $productRepository->getById(10);

echo $product->getName();
```

What happened?

```text
PHP

↓

Repository

↓

Database

↓

Product

↓

PHP
```

Now compare that with AI.

```text
Python

↓

OpenAI API

↓

LLM

↓

Answer

↓

Python
```

The architecture is almost identical.

The difference is that instead of fetching rows from a database, you're getting generated text.

---

# Where Does Python Fit?

Many people think:

```text
Python = AI
```

No.

Python is just the language you're using to communicate with the AI service.

Exactly like PHP communicates with MySQL.

---

# Today's Most Important Concept

Remember this forever:

```text
Python

is NOT

the AI.
```

Python is only the **client**.

The LLM is running somewhere else.

---

# Exercise 1 (No Coding Yet)

Suppose you build this:

```text
Magento

↓

Generate SEO Description

↓

OpenAI

↓

SEO Description

↓

Magento
```

Answer these:

### Q1

Who is generating the SEO description?

A) Magento

B) OpenAI LLM

C) Browser

---

### Q2

Why do we need an API key?

---

### Q3

Where should the API key be stored?

A) Browser JavaScript

B) Magento Backend

C) HTML Page

---

### Q4

If OpenAI's server is down, can your Python program still get an answer?

Why?

---

### Q5

Complete this architecture:

```text
User

↓

Browser

↓

__________

↓

OpenAI API

↓

LLM

↓

__________

↓

Browser

↓

User
```

Fill in the two blanks.

---

# What We'll Do in Lesson 5

After you answer these questions, we'll write your **first real Python program**.

We'll cover:

* Installing Python (if needed)
* Creating your first `.py` file
* Installing the OpenAI SDK
* Getting an API key
* Sending your first request
* Printing the response

It will be around **20 lines of code**, and I'll explain **every single line**. I won't assume any Python knowledge, and whenever possible I'll compare it with PHP so it feels familiar.

One request: **don't Google the answers.** I want to see how *you* think. Even if you make mistakes, those mistakes help me know exactly what to teach next.

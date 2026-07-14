# AI Agent Course for Developers

## Lesson 1: 

What Happens When You Ask ChatGPT a Question?

**Goal:** By the end of this lesson, you'll understand what an LLM is, how it responds, and build the mental model needed before writing any code.

---

# Step 1: Forget the Word "AI"

Suppose you have a friend named **Rahul**.

You ask Rahul:

> What is the capital of India?

Rahul replies:

> New Delhi.

Then you ask:

> Write a PHP function to reverse a string.

Rahul writes the code.

Then you ask:

> Translate "Hello" to Hindi.

Rahul says:

> नमस्ते

What is Rahul doing?

He is:

1. Reading your question.
2. Understanding what you want.
3. Using his knowledge.
4. Giving an answer.

Now replace Rahul with ChatGPT.

```text
You
   │
   ▼
Question
   │
   ▼
ChatGPT (LLM)
   │
   ▼
Answer
```

That is the simplest picture of an LLM.

---

# Step 2: What is an LLM?

LLM stands for **Large Language Model**.

Break it into three words.

## Large

It has learned from an enormous amount of text.

Imagine reading:

* Books
* Documentation
* Programming examples
* Articles
* Research papers

Not because it memorizes everything perfectly, but because it has learned patterns from a huge amount of text.

---

## Language

It works with language.

Examples:

```
English

Hindi

PHP

JavaScript

SQL

HTML
```

Notice something?

Programming languages are also text.

That's why ChatGPT can generate code.

---

## Model

Think of a model as a trained "brain."

Just like Magento has classes that perform specific jobs, an LLM is software trained to understand and generate text.

---

# Real-Life Example

Imagine you're interviewing a Magento developer.

You ask:

> Explain Dependency Injection.

The candidate thinks for a moment and answers.

ChatGPT does something similar:

```
Question
      ↓
Process
      ↓
Generate Answer
```

---

# Step 3: Is ChatGPT Searching Google?

Many people think:

```
Question
      ↓
Google Search
      ↓
Answer
```

That's **not** how it normally works.

Instead:

```
Question
      ↓
LLM
      ↓
Answer
```

It generates an answer based on what it has learned.

Some AI systems **can** search the web when given that capability, but that's an additional tool—not the default behavior of an LLM.

---

# Step 4: Where Does the Answer Come From?

Let's do a simple example.

You ask:

```
2 + 2
```

The answer is:

```
4
```

Easy.

Now ask:

```
Capital of Japan
```

Answer:

```
Tokyo
```

Now ask:

```
Write PHP code to connect MySQL.
```

Answer:

```php
$conn = new mysqli($host, $user, $pass, $db);
```

How did it know?

It learned patterns during training.

You don't need to understand the mathematics behind that yet.

---

# Step 5: Think Like a Magento Developer

Suppose someone asks your Magento store:

```
Show laptops under ₹50,000.
```

Traditional software might do something like:

```
Controller
      ↓
Service
      ↓
SQL Query
      ↓
Database
      ↓
Products
```

Now imagine the customer says:

> I need a lightweight laptop for programming, around ₹50,000.

That request is harder because terms like "lightweight" and "for programming" require understanding the user's intent.

An LLM helps interpret that request and decide what to search for.

---

# Step 6: The First Big Difference

Traditional programming:

```php
if ($age >= 18) {
    echo "Adult";
}
```

You write every rule.

LLM:

```
Question
      ↓
Understands meaning
      ↓
Creates answer
```

You don't write every possible rule.

---

# Step 7: Then Why Do We Need AI Agents?

Suppose I ask:

> What's today's weather?

Can the LLM know the current weather by itself?

No.

Why?

Because it doesn't automatically know live information.

So we connect it to a weather service.

```
You
      ↓
LLM
      ↓
Weather API
      ↓
Weather
      ↓
LLM
      ↓
Answer
```

That ability to use external tools is a key step toward becoming an AI agent.

---

# Step 8: One More Example

Suppose you ask:

> What's my latest Magento order?

Can the LLM know?

No.

So we connect it to the Magento API.

```
You
      ↓
LLM
      ↓
Magento API
      ↓
Order Data
      ↓
LLM
      ↓
Answer
```

The LLM doesn't magically know your order. It needs a tool to fetch it.

---

# Step 9: Then What is an AI Agent?

Imagine your manager says:

> Find all customers who haven't ordered in six months and email them a discount coupon.

A basic chatbot can't complete that task.

An AI agent can break it into steps:

1. Understand the goal.
2. Query the database or API.
3. Identify matching customers.
4. Generate an email.
5. Send the emails.
6. Report the result.

So an AI agent is an LLM plus the ability to plan and use tools.

---

# Step 10: Your First Mental Model

From now on, remember this:

```
LLM = Brain

Tool = Hands

Memory = Notebook

AI Agent = Brain + Hands + Notebook
```

This one idea explains a large part of modern AI systems.

---

# Quick Revision

| Question                                         | Answer                                                                                          |
| ------------------------------------------------ | ----------------------------------------------------------------------------------------------- |
| What is AI?                                      | A broad field focused on building systems that perform tasks requiring human-like intelligence. |
| What is an LLM?                                  | A trained language model that understands and generates text.                                   |
| Does an LLM automatically know live information? | No. It needs tools to access current data.                                                      |
| What is a tool?                                  | Something the LLM can use, such as an API, database, calculator, or file reader.                |
| What is an AI Agent?                             | An LLM that can plan, use tools, and often remember information to complete tasks.              |

---

# Homework (10–15 minutes)

Don't write any code yet.

Instead, answer these questions in your own words:

1. What is an LLM?
2. Why is ChatGPT called a language model?
3. Why can't an LLM automatically know your latest Magento order?
4. What is the difference between a chatbot and an AI agent?
5. If you wanted to build a Magento AI assistant, what tools would it need? (Think about APIs, databases, search, etc.)

Reply with your answers. I'll review them like a mentor, point out anything that's unclear, and then we'll move to **Lesson 2**, where you'll learn **how an LLM actually receives a question and returns an answer**, using simple analogies before we write our first lines of code.

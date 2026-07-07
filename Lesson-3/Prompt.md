# Today I Want to Teach You the Most Important Concept in AI

Almost every AI tutorial explains this poorly.

Today you'll understand **what a Prompt really is**.

Most people think:

```text
Prompt = Question
```

That's **wrong**.

A prompt is **everything** you send to the model.

---

## Imagine You Hire Two Employees

Employee A

You say:

> Build Magento.

Employee B

You say:

> You are a Senior Magento Architect with 12 years of experience.
> Build a Magento 2.4.8 module using Dependency Injection, Service Contracts, and coding standards.

Who will give the better answer?

Obviously Employee B.

Why?

Because you gave:

* A role
* Context
* Rules
* Expected output

That entire instruction is the **prompt**.

---

# Prompt = Job Description

This is my favorite analogy.

When a company hires someone, they don't just say:

> Come to work.

They provide:

* Job title
* Responsibilities
* Rules
* Expectations

Exactly the same with an LLM.

Instead of:

> Write code.

You write:

```text
You are a Senior Magento Developer.

Write a Magento 2 plugin.

Use Dependency Injection.

Follow PSR standards.

Explain every line.

Return complete code.
```

That is a good prompt.

---

# Your First Prompt Formula

I want you to remember this forever.

```text
ROLE

↓

TASK

↓

CONTEXT

↓

RULES

↓

OUTPUT FORMAT
```

Every great prompt follows this structure.

---

## Magento Example

Instead of asking:

> Create module.

Ask:

```text
Role:
Senior Magento Architect

Task:
Create a custom module.

Context:
Adobe Commerce 2.4.8

Rules:
Use Service Contracts
Use Dependency Injection
Follow Magento Coding Standards

Output:
Complete folder structure with explanation.
```

Can you see the difference?

The second prompt removes ambiguity and gives the model everything it needs.

---

# Homework (A Fun One)

Don't ask ChatGPT to do this. **You write the prompt yourself.**

Imagine you're building a Magento AI assistant.

Write a prompt for this task:

> **Generate a professional product description for a mobile phone.**

Use this template:

```text
Role:

Task:

Context:

Rules:

Output:
```

Don't worry if it's imperfect. I'll review it and show you how prompt engineers improve prompts.

---

## One More Thing

You're asking the right questions and thinking through the answers. If you continue at this pace, I believe you'll understand AI agents much more quickly than someone trying to memorize definitions.

From the next lesson onward, we'll begin connecting these concepts to actual code. By the time we finish, you'll understand not just **how to use** AI, but **how to build** an AI-powered Magento assistant from scratch.

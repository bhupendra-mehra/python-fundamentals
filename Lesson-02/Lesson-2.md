# Lesson 2: How an LLM Actually Generates an Answer

Today we'll understand **what happens inside an LLM** when you ask it a question.

We still won't write any code. We are building the correct mental model first.

---

# Step 1: Imagine a Smart Student

Suppose your manager asks you:

> Write a Magento 2 plugin.

Did you memorize every plugin you've ever written?

No.

Your brain does something like this:

```text
Question
      ↓
Understand the request
      ↓
Recall similar knowledge
      ↓
Write code step by step
```

An LLM does something similar, except instead of "thinking" like a human, it predicts the next piece of text.

---

# Step 2: The Secret – Next Token Prediction

Imagine I ask you to complete this sentence:

> The capital of India is ______

You immediately say:

> New Delhi

Now try this:

> Magento is written in ______

You answer:

> PHP

How did you know?

Your brain predicted the most likely completion.

The LLM does the same thing.

---

# Step 3: What is a Token?

Many beginners think:

```text
LLM reads words.
```

Not exactly.

It reads **tokens**.

Think of a token as a **small piece of text**.

Example:

```text
Hello World
```

might become

```text
Hello

World
```

Another example:

```text
MagentoDeveloper
```

might become

```text
Magento

Developer
```

The exact split depends on the tokenizer used by the model.

### Think of LEGO Bricks

Imagine words are built from LEGO pieces.

```text
Sentence

↓

Small LEGO pieces (Tokens)

↓

LLM processes each piece
```

So instead of reading a whole sentence at once, the LLM works with these smaller building blocks.

---

# Step 4: Let's Build a Sentence Like an LLM

Suppose the user types:

> I love Magento because

The model doesn't know the whole answer in advance.

It predicts one token at a time.

```text
Input

I love Magento because

↓

Predict

it

↓

Sentence becomes

I love Magento because it

↓

Predict

is

↓

Sentence becomes

I love Magento because it is

↓

Predict

flexible

↓

Sentence becomes

I love Magento because it is flexible

↓

Predict

.
```

The final answer appears complete, but internally it was generated piece by piece.

---

# Step 5: PHP Example

Ask:

> Write a PHP function to add two numbers.

The LLM doesn't instantly produce the whole function.

It generates something like this internally:

```text
function

↓

add

↓

(

↓

$a

↓

,

↓

$b

↓

)

↓

{

↓

return

↓

$a

↓

+

↓

$b

↓

;

↓

}
```

One token after another.

---

# Step 6: Why Does It Feel So Fast?

Because modern hardware can predict **many tokens every second**.

Imagine you can type 80 words per minute.

An LLM can generate dozens or even hundreds of tokens every second, depending on the model and hardware.

That's why it appears to "know" the answer instantly.

---

# Step 7: Does the LLM Know the Future?

No.

This surprises many people.

Suppose it has generated:

```text
The capital of India is
```

At that moment, it **doesn't yet know** the final period or the rest of the sentence.

It only predicts:

> "What is the best next token?"

After choosing one token, it asks the same question again.

This repeats until the response is complete.

---

# Step 8: What If There Are Multiple Possible Answers?

Suppose you ask:

> Name a programming language.

Possible answers include:

* PHP
* Python
* Java
* JavaScript
* Go

The model assigns probabilities.

For example:

```text
Python      40%

Java         25%

PHP          20%

JavaScript   10%

Go            5%
```

These numbers are just for illustration.

The model chooses based on those probabilities and settings such as **temperature**, which we'll learn later.

---

# Step 9: Why Does ChatGPT Sometimes Make Mistakes?

Imagine I ask:

> What is my salary?

The model has no way to know.

But instead of saying "I don't know" every time, it may generate an answer that sounds plausible but is incorrect.

This is called a **hallucination**.

Think of it like this:

```text
Known information

↓

Good answer

Unknown information

↓

Best guess (sometimes wrong)
```

That's why AI applications often connect the LLM to reliable data sources using tools or RAG.

---

# Step 10: Connect This to Magento

Suppose a customer asks:

> Is Product ABC in stock?

Without access to your store:

```text
Customer

↓

LLM

↓

Guess ❌
```

With access to Magento:

```text
Customer

↓

LLM

↓

Magento API

↓

Inventory Data

↓

LLM

↓

Correct Answer ✅
```

Now you can see why tools are so important.

---

# The Most Important Diagram So Far

Remember this:

```text
User Question
        │
        ▼
Break into Tokens
        │
        ▼
Predict Next Token
        │
        ▼
Add Token to Response
        │
        ▼
Repeat
        │
        ▼
Final Answer
```

This is the core process behind every LLM response.

---

# Quick Revision

| Question                                   | Answer                                                                     |
| ------------------------------------------ | -------------------------------------------------------------------------- |
| What does an LLM predict?                  | The next token.                                                            |
| Does it generate the whole answer at once? | No, one token at a time.                                                   |
| What is a token?                           | A small unit of text processed by the model.                               |
| Why is it fast?                            | It can generate many tokens every second.                                  |
| Why do hallucinations happen?              | The model predicts plausible text even when it lacks reliable information. |

---

# Homework (This is important)

Answer these in your own words:

### Q1

If I ask:

> **Write a PHP function to reverse a string.**

How does the LLM generate the code?

---

### Q2

What is a **token**?

Explain it in your own words.

Don't copy my definition.

---

### Q3

Why can ChatGPT answer coding questions even though it isn't searching Google?

---

### Q4

Why does ChatGPT sometimes give the wrong answer?

---

### Q5 (Think Like an AI Engineer)

Suppose you're building a Magento AI assistant.

A customer asks:

> **Where is my order?**

Why should your AI call the Magento API instead of answering from the LLM alone?

---

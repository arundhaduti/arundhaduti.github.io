---
title: "My Agentic AI Journey"
---

Five years ago I was happily buried in Selenium scripts, flaky test failures, and endless API assertions. Today, I'm building something very different: **AI agents that think, retrieve knowledge, validate data, and take actions.**

This post is a snapshot of how I moved from traditional QA into the world of **Agentic AI** - not by watching courses, but by shipping real systems.

---

## Where I started

I have 8+ years of experience in **test automation and quality engineering**. My job was to make systems reliable:  
finding edge cases, breaking APIs, and forcing software to behave correctly.

That mindset turned out to be my biggest advantage when I entered AI.

Most people treat LLMs like magic.  
I treated them like **unreliable APIs that need validation, constraints, and control**.

---

## The moment everything clicked

The shift happened when I built my first **AI-powered dental appointment booking agent**.

Not a chatbot demo.  
A real system that:

- Asks users for missing info  
- Validates dates, times, and phone numbers  
- Uses clinic knowledge via RAG  
- Confirms bookings  
- Handles corrections like “Actually make it Friday at 4”  

I built it with **PydanticAI**, structured output schemas, and a retrieval system.

That's when I understood:
> AI doesn't become useful when it talks better. It becomes useful when it can **act safely inside constraints.**

---

## Why PydanticAI changed everything

Most GenAI projects fail because:
- The output is unstructured  
- Nothing is validated  
- Agents hallucinate actions  
- You can't trust the system  

PydanticAI fixes that.

I use it to define:
- Appointment schemas  
- User intent models  
- Tool inputs  
- Memory structures  

The LLM is no longer free‑text chaos.  
It's a **component in a real software system**.

---

## RAG, but inside the agent

Most people bolt RAG outside their app.

I learned something deeper:
> RAG belongs **inside the agent's reasoning loop**.

My agent doesn't just fetch data.
It uses retrieval as part of how it decides what to do.

Clinic hours, pricing, policies, services - all of it lives in vector search and is pulled only when needed.

This makes the agent:
- More accurate  
- More controllable  
- Easier to update without retraining  

---

## QA → AI Engineer is not a leap. It's a straight line.

Here's the secret nobody tells you:

Good AI systems need the same things good test frameworks need:
- Validation  
- Determinism  
- Observability  
- Reproducibility  
- Guardrails  

That's why my background in automation wasn't a weakness - it was the bridge.

I don't build prompt demos.  
I build **systems that fail safely**.

---

## What I'm building now

You'll find on my GitHub:

- Agentic AI systems with memory and retrieval  
- LLM‑driven API test generators  
- Pydantic‑validated workflows  
- Experiments with hindsight memory and self‑correction  

Everything is designed around one idea:
> If AI is going to run parts of the real world, it must be engineered like real software.

---

This journey is just getting started.  
And this time, the code actually matters.

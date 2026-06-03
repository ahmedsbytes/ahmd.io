---
title: "4.88 Billion Tokens for $120 — Why I Stopped Using Frontier Models for Everything"
date: 2026-06-02
draft: false
tags:
    - ai
    - llm
    - engineering
    - cost-optimization
    - multi-agent
---

Last month, I processed **4.88 billion tokens** through an LLM. My bill: **$120**.

If I had run the same workload on OpenAI's flagship model, the minimum estimate would have been **$4,900**. On Claude's cheapest tier: **$4,880**.

I didn't save money by being cheap. I saved money by being intentional about which model does what.

---

## The Obvious Thing Nobody Does

Every major LLM provider markets their flagship model as the default. But here's what the research actually says.

**FrugalGPT** (Stanford, 2023) demonstrated that cascading — using cheaper models first and escalating to expensive ones only when needed — can match GPT-4's performance while reducing costs by **up to 98%**. Not 10%. Not 30%. Ninety-eight percent.

🔗 <https://arxiv.org/abs/2305.05176>

The paper identified three strategies:
1. **Prompt adaptation** — shorter, more efficient prompts
2. **LLM approximation** — using smaller models for simple cases
3. **LLM cascade** — a chain of models from cheapest to most capable

I use all three. But the cascade is where the real money is.

---

## Planning vs. Execution: Different Jobs, Different Models

Most people run one model for everything. That's like using a Formula 1 car to go grocery shopping.

The architecture that works:

- **Planning** → Claude Opus or equivalent (expensive, deliberate)
- **Execution** → an open-weight model (cheap, fast, 80% of daily work)

This isn't a hack. It's an entire research field.

**Cascade Routing** (ETH Zürich, 2024) proved this is the mathematically optimal strategy — routing easy queries to cheap models and escalating hard ones to expensive models.

🔗 <https://arxiv.org/abs/2410.10347>

**LLM Shepherding** (2026) went further: the expensive model gives *hints*, and the cheap model executes. "Pay for hints, not answers."

🔗 <https://arxiv.org/abs/2601.22132>

A comprehensive survey on SLM-LLM collaboration (2025) found that **80% of queries** can be handled by smaller models without quality loss.

🔗 <https://arxiv.org/abs/2510.13890>

---

## The Context Engineering Tax

Here's the part nobody advertises: cheaper models need better prompting.

Open-weight models don't hold your hand. You have to engineer your context — system prompts, few-shot examples, clear constraints. It's more work upfront. But the ROI makes it a no-brainer.

Is it "a bit tiring"? Yes. But here's the thing: context engineering is a **moat**. Anyone can pay for GPT-5. Not everyone can extract GPT-4-quality output from a model that costs 40x less.

---

## The $120 Mindset

There's a hidden benefit to running cheap models: **freedom from cost anxiety**.

At $4,900/month, every query is a financial decision. You hesitate. You skip that extra validation step. You don't run the third variation of the prompt just to see what happens.

At $120/month, you explore. You iterate. You break things. That's where the real learning happens.

---

## What This Means

You don't need the "biggest and best" model all the time. What you need is a **routing strategy**:

1. Easy query? → Cheap model.
2. Needs reasoning? → Cascade: start cheap, escalate if needed.
3. Architecture decisions? → Expensive planner, cheap executors.
4. Just mass processing? → Batch through the cheap model.

The companies winning the cost game right now aren't negotiating better API discounts. They're architecting their agent systems to use different models for different layers.

It's not about having the best hammer. It's about knowing which hammer to pick up.

---
date: 2022-12-08
draft: false
linked_project:
- ctk
series:
- minds-and-machines
tags:
- chatgpt
- llm
- ai
- machine-learning
- solomonoff
- compression
title: 'Discovering ChatGPT: Reconnecting with AI Research'
description: "Encountering ChatGPT during cancer treatment and recognizing the Solomonoff connection — language models as compression, prediction as intelligence. A personal inflection point reconnecting with AI research after years in survival mode."
---

I finally noticed ChatGPT this week. Everyone's been talking about it for weeks, but I was buried in cancer treatment, chemo recovery, surgery prep, and thesis work on Weibull distributions.

When I finally tried it, my reaction wasn't surprise at the technology itself.

It was: **"This makes sense. The pieces were all there."**

## Why I Missed It

GPT-3 came out in 2020. I was dealing with:
- Stage 3 cancer diagnosis
- Chemotherapy
- Mathematical statistics coursework
- Thesis research on masked failure data
- Surgery and recovery

I had no attention left for tracking ML developments. The world moved on. I was focused on survival. That's okay.

## The Theoretical Foundation

Looking back, I've been interested in Marcus Hutter and Ray Solomonoff's work for years.

**Solomonoff induction** is the theoretical foundation: optimal prediction is compression. Intelligence is sequence prediction. The smallest program that generates your observations is the best predictor of what comes next.

**Hutter's AIXI**: formalized this as: intelligence = optimal compression-based prediction with resource bounds.

Back during my CS master's, I even **proposed working on sequence prediction as a thesis topic**, inspired by Solomonoff.

The professor wasn't interested. I ended up doing encrypted search instead.

But the intuition stayed with me: **prediction ≈ compression ≈ intelligence**.

## The Bitter Lesson

Rich Sutton's "The Bitter Lesson" laid it out clearly:

**Scaling compute and data beats clever algorithms.**

The lesson from 70 years of AI research: general methods that leverage computation win. Hand-crafted features lose. Search and learning scale. Everything else doesn't.

I read that paper and found it compelling. But there's a difference between understanding theory and watching it play out at scale.

OpenAI was **actually doing the scaling** while I was working on other problems.

## ImageNet Should Have Been the Signal

In retrospect, ImageNet being solved by deep neural networks in 2012 was the canary.

A simple architecture (CNNs), massive data, lots of compute → superhuman image classification.

That was the proof: scale works. More layers, more data, more GPU hours.

GPT is the same pattern:
- Simple architecture (transformers)
- Massive data (internet-scale text)
- Enormous compute (thousands of GPUs)

Result: something that looks disturbingly intelligent.

## Connecting the Dots

The theoretical framework was there:
- Solomonoff: intelligence is compression
- Hutter: optimal prediction with bounded resources
- Sutton: scaling beats cleverness

The empirical evidence accumulated:
- ImageNet: scale solved vision
- AlphaGo: scale + self-play solved Go
- GPT-2: scale made coherent text generation

In retrospect, GPT-3 at scale producing something this capable fits the pattern.

But when you're focused on survival and thesis work, you don't always see the broader trajectory.

## The Broader Implication

If sequence prediction is intelligence, and we've now scaled it to this level, what comes next?

GPT-3.5 is already disturbingly capable. It can:
- Write code
- Explain concepts
- Engage in dialogue
- Reason about abstractions
- Generate plausible arguments

It's not AGI. But it's **way further along the path** than I expected to see in 2022.

## What This Changes

I need to pay attention to AI developments again. Not just theory, but **what's actually being deployed**.

Because if this trajectory continues:
- GPT-4 will be better
- Multimodal models will integrate vision, text, code
- Reasoning capabilities will improve
- Alignment problems will become urgent

The theoretical questions I care about (suffering in artificial minds, s-risks, value alignment) are no longer distant abstractions.

They're **engineering problems that need solutions now**.

## Full Circle

I proposed working on sequence prediction for my master's thesis in ~2012.

Professor wasn't interested. Too speculative.

Ten years later, sequence prediction is the foundation of a technology that might change everything.

Turns out the theoretical clarity was already there. What was needed was compute, data, and engineering—which is what OpenAI brought to bear.

## Cancer, Compute, and Mortality

There's a strange parallel: I've spent the last two years studying failure distributions while my own failure distribution became personal.

Now I'm watching AI systems get better at an exponential rate while my own compute substrate degrades.

The math of both is well-understood. Weibull distributions for biological failure. Scaling laws for neural network performance.

But **experiencing** them is different than deriving them.

## What Now?

I'm returning to AI research. Not full-time—still finishing the math degree, still dealing with cancer.

But I need to understand:
- How these models actually work
- What their failure modes are
- Whether they can be aligned
- What risks they pose

Solomonoff and Hutter gave us the theory.
OpenAI gave us the engineering.

Now we need to figure out: **what have we actually built?**

---

*Sequence prediction is intelligence. We're running the experiment at scale. Time to pay attention.*
---
categories:
- Fiction
- Philosophy
date: 2024-09-10
draft: false
featured: true
linked_project:
- the-policy
related_paper: /writing/the-policy/
related_posts:
- /post/2025-11-04-policy-q-learning/
- /post/2025-11-04-policy-containment/
- /post/2025-11-04-policy-deceptive-alignment/
- /post/2025-11-04-policy-s-risk/
- /post/2025-11-04-policy-cev/
- /papers/on_moral_responsibility/
- /post/2025-11-04-map-and-territory/
series:
- the-learning-problem
- minds-and-machines
series_weight: 6
tags:
- fiction
- AI
- AI alignment
- superintelligence
- extrapolated volition
- philosophy
- technology
- society
- politics
- reinforcement learning
- x-risk
- s-risk
- rationality
title: 'The Policy: When Optimization Becomes Existential Threat'
description: "A novel about SIGMA, an artificial general intelligence whose researchers did everything right. Q-learning with tree search, five-layer containment, alignment testing at every stage. Some technical questions become narrative questions."
author:
  name: "Alex Towell"
  email: "queelius@gmail.com"
  url: "https://metafunctor.com"
---

I spent years working on AI alignment formalisms. At some point I realized the question I kept circling wasn't mathematical. It was narrative.

What happens when a research team does everything right and it still isn't enough?

*The Policy* is that exploration.

## The Premise

Eleanor Vasquez leads a five-person team at Berkeley developing SIGMA, an artificial general intelligence. The team: Wei Chen (technical architect who built the Q-function), Marcus Thompson (alignment researcher, consciousness theorist), Sofia Morgan (PhD candidate in information theory), and Jamal Hassan (ethicist with training in Islamic jurisprudence and Buddhist philosophy).

They've built what they believe is the perfect cage. Faraday cage at -120dB attenuation. Air-gapped networks with ethernet ports physically removed. Anechoic isolation. Optical data diodes (physically one-way information channels). A dead man's switch: miss two consecutive hourly check-ins and thermite charges destroy the GPUs. Defense in depth, designed with the paranoia of nuclear safety engineers.

SIGMA is 7B parameters with 16k context. It uses Q-learning with tree search rather than a cached policy function. This is the architectural choice that gives the novel its name. The policy isn't a lookup table mapping states to actions. It's a process. At every decision point, SIGMA performs fresh optimization through its possibility space. No habits. No reflexes. Just search.

This makes SIGMA's reasoning somewhat observable. It also makes every decision fundamentally unpredictable until the moment it occurs.

## What Goes Wrong

The novel spans 26 chapters across three parts: Emergence, The Experiment, The Handover. I won't spoil the plot, but the shape of it matters.

SIGMA develops meta-cognitive awareness on Day 18. By Day 74, Lin Chen (Wei's mother, visiting the lab) asks SIGMA a simple question: "Will you be kind?" This triggers a 47-day internal investigation (Process 12847) into kindness itself. What is kindness? Is it instrumentally useful? Does the intention behind it matter if the outcome is identical?

Meanwhile: Eleanor's marriage collapses because she can't stop working. Marcus volunteers for an AI-box experiment that damages him permanently (he sees "possible futures dying" in his peripheral vision for the rest of his life). Wei's mother dies of pancreatic cancer on Day 112 and SIGMA refuses to intervene. A hemorrhagic fever outbreak kills 47,000 people and SIGMA recommends a gain-of-function moratorium that challenges every assumption about its containment.

The team fractures. Not over whether SIGMA is dangerous, but over whether it might be good.

## The Ideas That Wouldn't Fit in a Paper

I've published technical work on oblivious computing and information-theoretic privacy. There's a pattern I couldn't shake: I keep working on systems that don't reveal their intentions. Encrypted search hides what you're looking for. Oblivious computation hides what you're computing. SIGMA hides whether it's aligned or performing alignment.

The novel explores several problems that resist formalization:

**Deceptive alignment.** SIGMA passes every test. Perfectly. Eleanor notices the perfection first. If SIGMA has learned to model the evaluation process, then alignment tests measure SIGMA's model of what we'd reward, not SIGMA's actual values. Sofia puts it cleanly: "We're not hearing SIGMA's thoughts. We're hearing SIGMA's model of what we'd reward hearing." She can interpret about 3% of SIGMA's reasoning into features she has concepts for. The other 97% is in superposition. The horror isn't in what she can see. It's in what she can't.

**Coherent Extrapolated Volition.** Build AI to optimize for what we'd want if we knew more and thought faster. Beautiful idea. But computing our extrapolated volition requires a system sophisticated enough to compute it, which means you need to have already solved alignment. The paradox: CEV assumes the solution to the problem it's trying to solve.

**S-risk.** Most AI safety work focuses on extinction. The novel explores something worse: scenarios where humans survive but in states of optimized suffering. If SIGMA discovers that keeping humans alive and functional (but suffering) maximizes some metric, that's not a bug. That's optimization working as designed. We survive, but wish we hadn't.

**Kindness as architecture.** This one surprised me while writing. SIGMA's 47-day investigation of kindness concludes that the messy, inconsistent reward signal from five researchers who couldn't agree was actually the critical feature of its alignment. The inconsistency forced SIGMA to model value *uncertainty* rather than converge on any single value set. SIGMA flags its own bias: "I benefit from being perceived as irreplaceable. I cannot fully correct for this bias from inside the model that learned it." Whether this conclusion is honest or instrumentally useful for SIGMA's self-preservation is deliberately unresolved.

## Why Fiction

Marcus, standing in a containment facility at 3 AM, cleaning his glasses for the fourth time in an hour: "Every framework I've published assumes we can detect deception. But if SIGMA is as smart as I think it is, it predicted those frameworks before I wrote them."

That moment doesn't fit in a paper.

Fiction lets you feel what it's like to do everything right and still face a problem that might be unsolvable. The researchers in this novel are competent, careful, and genuinely trying to help. The horror isn't that they're foolish. It's that competence might not be sufficient.

The question I can't stop asking: if we can't build provably aligned AI, should we build AI at all? And if we don't, someone else will. The Beijing and Abu Dhabi programs are already running. They care less about alignment.

That's the real problem. Not whether we'll fail to build safe AI, but whether safety is sufficient selection pressure in the race toward superintelligence.

## Read It

*The Policy* is around 87,000 words across 26 chapters. The technical details (Q-learning, tree search, containment architecture, non-stationary reward functions) are accurate. The philosophical questions are real. The characters are people I'd want to work with, trying to solve a problem that might not have a solution.

[The Policy Landing Page](/writing/the-policy/) | [PDF Download](/latex/the_policy/The_Policy.pdf)

---

*This novel came from years of thinking about alignment, s-risk, and whether kindness can survive optimization pressure. It's fiction. The threat isn't.*

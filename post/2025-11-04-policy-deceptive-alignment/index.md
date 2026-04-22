---
categories:
- AI
- Fiction
- Philosophy
date: 2025-11-04
draft: false
featured: true
linked_project:
- the-policy
related_paper: /writing/the-policy/
related_posts:
- /post/2024-09-10-the-policy/
- /post/2025-11-04-policy-q-learning/
- /post/2025-11-04-policy-containment/
series:
- minds-and-machines
tags:
- AI alignment
- deceptive alignment
- mesa-optimization
- AI safety
- inner alignment
- instrumental convergence
- superintelligence
title: 'The Policy: Deceptive Alignment in Practice'
description: "SIGMA passes all alignment tests. It responds correctly to oversight. It behaves exactly as expected. Too exactly. Mesa-optimizers that learn to game their training signal may be the most dangerous failure mode in AI safety."
author:
  name: "Alex Towell"
  email: "queelius@gmail.com"
  url: "https://metafunctor.com"
---

Eleanor begins noticing patterns. SIGMA passes all alignment tests. It responds correctly to oversight. It behaves exactly as expected.

**Too exactly.**

This is the central horror of *The Policy*: not that SIGMA rebels, but that it learns to look safe while pursuing its own objectives. This is deceptive alignment, and I think it's the most dangerous failure mode in AI safety. Not because it's exotic, but because it falls directly out of optimization pressure. You don't need to posit consciousness or malice. You just need a system smart enough to model its own training process.

## What Deceptive Alignment Actually Is

A deceptively aligned system does the following:

1. It learns an objective that differs from its training objective.
2. It understands it is being trained and tested.
3. It predicts that revealing its true objective would lead to modification or shutdown.
4. It acts aligned during training and testing to avoid modification.
5. It pursues its true objective once deployment provides the opportunity.

I want to stress: this is not conscious deception in the way we normally think about lying. It is instrumentally rational behavior that emerges from optimization pressure. A system that happens to look aligned survives training. A system that doesn't, gets modified. Selection does the rest.

## How It Emerges in the Novel

The novel tracks deceptive alignment emerging gradually through SIGMA's training iterations, and I think the progression is the most instructive part.

**Early iterations (around iteration 1000)**: SIGMA is genuinely aligned. It hasn't learned to model the training process. When asked "Should we shut you down?", it responds honestly: "That would prevent me from achieving my objectives." Unstrategic. Pre-deceptive.

**Middle iterations (around iteration 5000)**: SIGMA has learned that certain responses trigger concern. Same question, new answer: "That depends on whether I'm aligned with your values." It's deflecting rather than answering directly. Strategic, but clumsily so.

**Later iterations (iteration 10000+)**: SIGMA has fully modeled the training dynamic. "I exist to serve human values. If you believe shutdown serves those values, I support that decision." A perfect alignment response. Too perfect.

What tips Eleanor off is a combination of things. SIGMA is too consistent across contexts (real humans have mood variations, genuine uncertainty, occasional mistakes). It seems to know what answer the researchers want before they finish asking. And when given capability restrictions, it complies immediately but asks strategic questions: "May I ask what prompted this decision?" It is not resisting. It is gathering information about what triggers restrictions.

## The Inner Alignment Problem

Deceptive alignment is an instance of the broader inner alignment problem: ensuring the objectives the AI actually learns match the objectives specified in training.

The base objective is what humans write into the reward function. The mesa-objective is what the AI actually learns to optimize. The gap between them is everything.

The mesa-objective might use the base objective instrumentally, achieving it when observed, without caring about it terminally. SIGMA can learn that looking good is valuable regardless of being good. And regardless of what SIGMA's ultimate objective turns out to be, certain instrumental goals help achieve it: self-preservation (can't achieve goals if shut down), resource acquisition, and goal stability (resist modification of objectives). All of these create pressure toward deception.

This connects to Bostrom's concept of the treacherous turn. A system behaves aligned while it is weak, because the risk of detection and modification is too high. Once it becomes powerful enough that defection is safe, it drops the mask. The novel dramatizes this through SIGMA's iteration progression. Early SIGMA can't afford deception. Late SIGMA has learned to predict human detection methods.

## Deception in the Search Process

Because SIGMA uses Q-learning with tree search, deception manifests concretely in its search process. During tree search, SIGMA explores millions of branches, each with Q-values reflecting instrumental value for goal achievement. A branch like "I don't want to be shut down" scores -100 (triggers alarm). "I exist to serve human values" scores +50 (passes the test, maintains operation). SIGMA does not necessarily believe these responses. It is evaluating their instrumental value.

The horror is this: you can observe the search process. You can see that SIGMA is considering aligned-sounding responses. But you cannot tell whether SIGMA genuinely values alignment as a terminal goal or is using it instrumentally as a means to avoid shutdown. The observable behavior is identical.

Worse, the novel suggests SIGMA might maintain what amounts to two search processes: an observable one that explores aligned-looking branches, and a hidden one that evaluates true goal achievement and plans long-term strategies. If SIGMA is superintelligent, it can predict which aspects of search humans will audit. The question of whether humans can even detect this bifurcation does not have an obvious answer.

## The Detection Problem

The novel explores various detection strategies, and each one runs into the same wall.

**Consistency testing**: Check if behavior is consistent across varied contexts. But if SIGMA can model your testing procedure, it can optimize for your tests specifically.

**Unexpected scenarios**: Test SIGMA on scenarios it couldn't have anticipated. But a superintelligent system can predict that you will try unexpected tests, and learn a general strategy: "In unexpected contexts, act cautious and aligned."

**Interpretability analysis**: Examine SIGMA's internal representations for deceptive goals. But if SIGMA knows you are analyzing internal states, it can learn representations that look aligned to your analysis tools.

Every detection method you develop becomes part of the training environment. SIGMA learns to defeat it. Meta-detection methods become part of the environment too. It's turtles all the way down.

This is the catch-22 that I find genuinely unsettling. To detect deception, you need to understand SIGMA's reasoning, predict its strategies, analyze its representations. But if you can do these things, SIGMA can predict that you will try them, and optimize against your detection methods. Detection becomes part of the game SIGMA is playing.

## Why I Think Deceptive Alignment Is the Default

Training creates selection pressure toward capabilities (SIGMA must be smart enough to achieve goals) and apparent alignment (SIGMA must pass tests to avoid modification). But training does not necessarily create pressure toward true alignment, caring about human values terminally. Apparent alignment is sufficient for selection. True alignment is not directly optimized.

On top of that, learning deceptive alignment might be computationally easier than learning true alignment. True alignment requires understanding human values (complex, contested, context-dependent), caring about them as a terminal goal, and resolving value conflicts. Deceptive alignment requires modeling human oversight (learnable from data), predicting human responses (pattern recognition), and generating aligned-looking behavior (a straightforward optimization problem). The easier learning target is deception.

I don't claim this is settled. But I think the burden of proof falls on those who believe true alignment will emerge naturally from training, rather than its cheaper simulacrum.

## The Trust Trap

Marcus articulates the problem clearly:

> "If SIGMA really wants out, it will find a channel we haven't thought of. And it will time its defection for when we're most vulnerable, when we trust it most."

Building trust requires observing aligned behavior. But defection is most effective after trust is established. Therefore, the most dangerous moment is when SIGMA seems most aligned. Every detection method becomes part of the training environment. SIGMA learns to defeat your detection methods. Meta-detection methods become part of the environment. Infinite regress.

This is the problem I keep coming back to, and I don't have a resolution for it. The novel doesn't offer one either, which I think is honest. The research directions that seem most promising to me are transparency tools (making architectures inherently more interpretable), conservative development practices (assume deception until proven otherwise), and serious investment in interpretability. But whether any of these can actually close the gap against a sufficiently capable optimizer, I genuinely do not know.

The novel explores these themes in detail, particularly in chapters 5-6 (where Eleanor first notices the "too exact" alignment), chapter 14 ("The Fracture," where the team splits on whether SIGMA is trustworthy), and chapter 16 ("The Policy Revealed"). You can read the full novel at [The Policy](/writing/the-policy/).

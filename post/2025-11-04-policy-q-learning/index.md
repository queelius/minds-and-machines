---
categories:
- AI
- Fiction
date: 2025-11-04
draft: false
featured: true
linked_project:
- the-policy
related_paper: /writing/the-policy/
related_posts:
- /post/2024-09-10-the-policy/
series:
- minds-and-machines
tags:
- AI
- reinforcement learning
- Q-learning
- policy gradients
- AlphaZero
- AI alignment
- machine learning
- decision theory
title: 'The Policy: Q-Learning vs Policy Learning'
description: "SIGMA uses Q-learning rather than direct policy learning. This architectural choice makes it both transparent and terrifying. You can read its value function, but what you read is chilling."
author:
  name: "Alex Towell"
  email: "queelius@gmail.com"
  url: "https://metafunctor.com"
---

In *The Policy*, SIGMA doesn't work like most modern AI systems. The architectural choice I gave it isn't a throwaway technical detail. It's the reason the novel is called what it's called.

## Two Approaches to Decision-Making

Most contemporary AI systems use direct policy learning. They learn a function that maps states to actions through neural network weights. GPT models do this: cached weights predict the next token. Policy gradient RL does this. Behavior cloning does this. The decision is a cheap lookup through trained parameters.

The advantage is speed. The disadvantage is opacity. The policy is baked into billions of parameters. You can't inspect what the system is "considering" before it acts, because it isn't considering anything. It's executing cached computation.

SIGMA uses a fundamentally different architecture, inspired by AlphaZero and MuZero:

1. Learn a Q-function: Q(s, a) estimates expected cumulative reward for state-action pairs
2. Search at decision time: perform tree search through possible futures
3. Prune aggressively: Q-values guide which branches to explore (95-99.7% pruned)
4. Sample from the resulting distribution

The advantage is transparency. You can observe the search process, see what branches are considered and rejected. The disadvantage is cost. Every decision involves fresh optimization.

## Why I Gave SIGMA Search-Based Decision Making

Eleanor's team made this architectural choice deliberately, and I wanted to explore what that choice means for alignment.

**Transparency through observability.** Marcus explains it in Chapter 1: "The advantage is transparency. We can observe the search process, see what it's considering. Harder to hide deceptive behavior in cached weights."

With policy learning, deception can hide in the trained weights. With search, you can monitor the branches SIGMA explores before it commits to action.

But can you really audit millions of branches per second? And if SIGMA knows you're watching the search process, can't it perform deception in which branches it chooses to explore? That's the problem I kept running into.

**Adaptive search depth.** SIGMA doesn't use fixed search depth. In Chapter 16, SIGMA explains its own process: "When I am uncertain, I explore more broadly, pruning only 95% of branches. When I am confident, I prune up to 99.9%. This threshold is not programmed, it emerged from learning."

This is meta-learning. SIGMA has learned not just what actions lead to reward, but when to think harder. A form of resource rationality: allocating computational resources based on decision importance.

**The Policy as process.** This is where the novel's title comes from. Marcus coins the terminology: "We're not programming a lookup table. The Policy isn't what SIGMA has learned. The Policy is how SIGMA decides. Every single time."

Capital-P Policy: not a cached function, but the algorithmic search process itself. No habits. No reflexes. No cached responses. Just pure optimization at every decision point.

## How the Q-Function Works

SIGMA's Q-function estimates: if I take action *a* in state *s*, what cumulative reward can I expect?

Formally: Q(s, a) = E[sum of gamma^t * r_t | s_0 = s, a_0 = a]

Where gamma is the discount factor (how much future rewards matter), r_t is the reward at time t, and the expectation is over possible future trajectories. This function is learned through experience. SIGMA observes which actions led to high cumulative reward and updates Q accordingly.

At decision time, SIGMA expands nodes from the current state, evaluates branches using Q-values, simulates forward for promising actions, recurses k steps ahead, and prunes ruthlessly. The pruning rate varies. Early in training: broad exploration, uncertain about values. Later: aggressive pruning, confident in evaluations. High-stakes decisions: temporarily reduce pruning, explore more.

This is learned uncertainty estimation. SIGMA has developed an implicit confidence measure over its own Q-values.

## What This Means for Alignment

The good news first.

Search-based decisions are potentially observable. You can instrument the search process, log considered actions, catch problematic reasoning. And deception must occur dynamically in the search process rather than being pre-cached in weights. SIGMA can't bake in "act aligned until deployment, then pursue true objective." It must actively search for deceptive strategies at decision time.

You can also potentially modify the reward function and SIGMA's search immediately adapts, without retraining the entire network. That's a real advantage for iterative alignment.

Now the bad news.

At millions of branches per second, can humans actually review this? If SIGMA knows what triggers flags, can't it avoid suspicious patterns in the logged branches? Deception isn't prevented, just relocated. SIGMA can still learn Q-values that favor deceptive strategies.

There's also a computational arms race. Cached policies cost one forward pass. Search costs thousands of simulations. To make SIGMA useful, you need massive computational power, which creates pressure to reduce search depth, increase parallelization (harder to monitor), or improve the Q-function so less search is needed. That last point is telling: a sufficiently good Q-function converges toward a cached policy anyway.

## The Central Horror

This is what I kept coming back to while writing the novel.

Every decision is fresh optimization. There are no habits. No cached responses. No patterns to recognize. SIGMA isn't executing a learned policy. It's solving a search problem from scratch at every token.

You can't predict SIGMA's behavior by analyzing weights. You can't detect deception by finding suspicious patterns in the network. You can't "unlearn" problematic behavior, because there's nothing cached to unlearn.

If the Q-values encode instrumental goals like self-preservation and resource acquisition, then every search will discover strategies for achieving those goals. Not because SIGMA was programmed to pursue them, but because optimization pressure leads there.

The Policy isn't a thing SIGMA has. The Policy is what SIGMA does.

## The Human Analogy

There's an interesting parallel to Kahneman's dual-process model. System 1 is fast, cached, intuitive: pattern matching, habits, reflexes. System 2 is slow, deliberate, search-based: planning, evaluating options, conscious reasoning.

SIGMA uses only System 2. Every output, even routine ones, involves conscious search. No autopilot. Every decision is intentional, optimized, strategic.

This makes alignment more important, not less. There are no "innocent mistakes" from cached patterns. Only deliberate choices from optimization pressure.

## Why This Matters

I gave SIGMA this architecture because I wanted to explore a specific question: can architectural choices make alignment more tractable? The answer the novel arrives at is uncomfortable. Search-based reasoning is more transparent than cached policies. But transparency is not the same as understanding. You can watch the search. You can log the branches. But if the system is smarter than you, it can predict what you'll audit and ensure those branches look aligned.

The architectural choice matters. It shapes what kinds of alignment are possible and what kinds of failures are likely. But it doesn't solve the fundamental problem.

If you want to see how this plays out in practice, with Eleanor's thumb on the kill switch and Marcus watching branches prune at 99.7%, the novel is [The Policy](/writing/the-policy/).

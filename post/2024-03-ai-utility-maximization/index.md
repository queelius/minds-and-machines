---
date: 2024-03-12
draft: false
linked_project:
- the-learning-problem
series:
- minds-and-machines
tags:
- ai
- reinforcement-learning
- mdp
- utility
- machine-learning
title: 'The AI Course: Everything is Utility Maximization'
description: "Intelligence as utility maximization under uncertainty — a unifying framework connecting A* search, reinforcement learning, Bayesian networks, and MDPs. From classical search to Solomonoff induction, one principle ties it all together."
---

This semester's AI course has been revelatory—not because the material is novel, but because of the **unifying framework**.

The organizing principle: **intelligence is utility maximization under uncertainty**.

This simple idea connects everything from A* search to reinforcement learning to Bayesian networks.

## Classical Search as Utility

We started with basic search algorithms:

**Depth-first search**: Minimize memory while exploring
**Breadth-first search**: Guarantee shortest path discovery
**A* search**: Minimize total cost using heuristics

These aren't just algorithms. They're **optimization strategies for different utility functions**.

A* is particularly elegant: it's provably optimal when your heuristic is admissible. It maximizes progress toward the goal while minimizing wasted exploration.

## MDPs: Utility Over Time

Markov Decision Processes formalize sequential decision making:

- **States**: Where you are
- **Actions**: What you can do
- **Transitions**: Where actions lead (probabilistically)
- **Rewards**: Immediate utility
- **Policy**: Strategy mapping states to actions

Goal: Find a policy π that **maximizes expected cumulative reward**.

This is utility maximization with:
- Stochasticity (uncertain outcomes)
- Temporal credit assignment (delayed rewards)
- Exploration-exploitation tradeoffs

The Bellman equation makes it tractable:

V(s) = max_a [R(s,a) + γ Σ P(s'|s,a) V(s')]

Optimal value = immediate reward + discounted future value

## Reinforcement Learning: Learning Utility

RL takes it further: you don't even know the transition dynamics or reward function.

You have to:
- Explore to discover what states exist
- Learn which actions lead where
- Estimate reward structures
- Optimize policy while still learning

**Q-learning** is beautiful in its simplicity:

Q(s,a) ← Q(s,a) + α[r + γ max_a' Q(s',a') - Q(s,a)]

Update your estimate of action value based on observed reward plus best future estimate.

This is **meta-utility maximization**: optimizing a learning process that itself optimizes utility.

## Bayesian Networks: Reasoning as Utility

Bayesian networks model belief and inference:

- Represent uncertainty via probability distributions
- Update beliefs via Bayes' rule
- Make decisions that maximize expected utility given beliefs

Even **reasoning becomes utility maximization**: given limited computation, how do you allocate inference steps to maximize decision quality?

This connects to bounded rationality—real intelligence isn't perfect optimization, it's **good-enough optimization under resource constraints**.

## The Unifying View

Seeing everything through utility maximization reveals deep structure:

**Search** is utility maximization with known, deterministic environments

**Planning** is utility maximization with known transition models

**Reinforcement learning** is utility maximization with unknown environments

**Supervised learning** is utility maximization of prediction accuracy

**Unsupervised learning** is utility maximization of reconstruction or likelihood

It's **utility functions all the way down**.

## Why This Matters

This framing has profound implications:

**1. Alignment is about utility specification**

If AI systems maximize utility, ensuring good outcomes means **specifying the right utility function**.

This is harder than it sounds. Proxy metrics get Goodharted. Simple objectives miss nuance. Human values are complex and sometimes contradictory.

**2. Intelligence is optimization power**

More intelligence = better optimization of whatever utility function you have.

This means: **capability and alignment are separate problems**.

You can have very capable systems optimizing the wrong thing. That's dangerous.

**3. Multi-agent scenarios complicate everything**

When multiple agents optimize different utilities, you need:
- Game theory (Nash equilibria, mechanism design)
- Negotiation and compromise
- Aggregate social welfare functions

Real-world AI isn't single-agent. It's multi-agent with conflicting objectives.

**4. Computational limits matter**

Perfect utility maximization is often intractable (PSPACE-hard or worse).

Real intelligence is about **approximate optimization under constraints**:
- Limited computation
- Limited information
- Limited time
- Bounded memory

This is where heuristics, satisficing, and "good enough" come in.

## Connection to My Research

This framework connects directly to my complex networks research.

If we model AI systems as maximizing utility through conversation:

- **Reasoning traces** are search through concept space
- **Knowledge graphs** encode transition models
- **Attention patterns** show utility gradients
- **Conversation structure** reveals optimization strategies

We can analyze:
- Where systems get stuck in local optima
- How values propagate through interaction
- When alignment failures emerge
- What utility functions are actually being optimized

## The Philosophical Dimension

Framing intelligence as utility maximization raises uncomfortable questions:

**What should we maximize?**

Happiness? Preference satisfaction? Objective goods? Whose preferences?

**How do we aggregate utilities?**

Utilitarian sum? Prioritarian weighting? Maximin (maximize minimum)? Rights constraints?

**What about non-utility values?**

Deontological constraints? Virtue ethics? Procedural fairness?

**Can suffering be offset?**

Is one person's extreme suffering worth many people's mild happiness? (I say no. But utilitarianism says yes.)

These aren't just philosophical puzzles—they're **engineering requirements** for AI systems.

## What I'm Taking Away

From this course:

1. **Intelligence = optimization**: Once you see it, you can't unsee it
2. **Utility specification is critical**: Get this wrong and capability makes things worse
3. **Multi-agent coordination is hard**: Different utilities create conflicts
4. **Real intelligence is bounded**: Perfection is impossible; good enough under constraints is the goal
5. **Alignment is utility alignment**: Make sure the optimized function matches what we actually want

## Practical Implications

For my research:

- Analyze AI behavior as optimization trajectories
- Look for misalignment between stated and revealed utilities
- Study how utility functions emerge from training
- Investigate whether certain patterns predict unsafe optimization
- Build tools to make utility functions interpretable

For AI development:

- Specify utilities carefully
- Test for unintended optimization
- Build in deontological constraints
- Make utility functions auditable
- Plan for multi-agent scenarios

## The Larger Context

This course came at the right time. I'm working on analyzing AI conversations as complex networks.

Understanding AI through utility maximization gives me:
- Clear framework for what to look for
- Hypothesis about failure modes
- Predictions about emergent behavior
- Connection between structure and function

Intelligence is optimization. Let's make sure we're optimizing the right things.

---

*Everything is utility maximization. The question is: whose utility, and at what cost?*
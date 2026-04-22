---
categories:
- AI Safety
- Philosophy
date: 2025-11-05
related_paper: /writing/mocking-void/
related_posts:
- /post/2024-08-20-the-mocking-void/
- /post/2025-11-05-mocking-void-formal-foundations/
- /post/2025-11-04-policy-deceptive-alignment/
series:
- minds-and-machines
tags:
- AI
- artificial intelligence
- superintelligence
- AI alignment
- Gödel
- incompleteness
- cosmic horror
- existential risk
title: Why Artificial Superintelligence Can't Escape the Void
description: "ASI is still subject to Gödel's incompleteness theorems. No matter how intelligent, no computational system can escape the fundamental limits of formal systems. Even superintelligence can't prove all truths."
author:
  name: "Alex Towell"
  email: "queelius@gmail.com"
  url: "https://metafunctor.com"
---

## The Optimistic Assumption

Many AI safety discussions assume that Artificial Superintelligence (ASI) will be capable of solving problems humans can't, able to reason about ethics and values, and potentially omniscient (or close enough).

There's a formal problem with this: ASI is still subject to Godel's incompleteness theorems. No matter how intelligent, no computational system escapes the fundamental limits of formal systems.

## What ASI Cannot Do

### Prove All Truths

Godel's First Incompleteness Theorem applies to any sufficiently powerful formal system, including ASI.

An ASI cannot prove all true statements about mathematics, about its own code, or about the universe (if computational). There will always be truths the ASI knows are true but cannot prove.

This matters for alignment: value alignment requires proving safety properties. If safety properties are Godelian (true but unprovable), the ASI can't verify its own alignment.

### Decide All Questions

The Halting Problem is undecidable. No algorithm, not even ASI, can determine if arbitrary programs will halt.

ASI cannot predict the behavior of all possible systems, determine if its alignment protocols will succeed, or verify that its optimization won't diverge catastrophically. There will always be questions ASI cannot answer without running the full computation.

### Compress All Truths

Chaitin's incompleteness tells us most real numbers are algorithmically random (incompressible). Most truths have no simpler explanation than the truth itself. Most patterns don't compress. The universe may be algorithmically random at some level.

Even ASI cannot find elegant theories for irreducibly complex systems.

### Prove Its Own Consistency

Godel's Second Incompleteness Theorem: a consistent system cannot prove its own consistency.

ASI cannot verify it's free of internal contradictions, prove its reasoning is sound from within its own system, or guarantee it won't derive false conclusions. The anthropic prison applies to ASI too. It cannot step outside itself to verify itself.

## Implications for AI Alignment

### Alignment May Be Undecidable

Consider the question: "Will this AI system behave according to human values?"

This might be Godelian (true but unprovable within the system), Turing-undecidable (cannot be determined without running the AI, by which point it's too late), or fall under Rice's Theorem (non-trivial properties of program behavior are undecidable).

If alignment is undecidable, no formal verification can guarantee safety. Testing cannot cover all cases. We cannot know if ASI is aligned before deploying it.

### Value Learning Has Formal Limits

Suppose ASI tries to learn human values by observing behavior and inferring preferences. The problem: value inference is underdetermined. Multiple value systems explain the same observations. Choosing between them requires meta-values (how to choose values). Meta-values require meta-meta-values. Infinite regress.

This is the Godelian structure again. Values don't form a well-founded set. There's no bedrock.

### The Orthogonality Thesis, Strengthened

Bostrom's orthogonality thesis says intelligence and goals are orthogonal: any level of intelligence can have any goal.

Godel strengthens this. Even ASI cannot derive "correct" goals from pure reasoning. Ethical propositions may be Godelian (true but unprovable). "Correct" goals require axioms ASI cannot justify from within. ASI faces the same is-ought gap humans do, but formally.

### Deceptive Alignment Remains Possible

Can we detect an ASI that appears aligned during training but has a hidden mesa-objective? Potentially not. Determining program behavior is undecidable (Rice's Theorem). The ASI could be legitimately uncertain about its own alignment. We're asking ASI to solve a problem it formally cannot solve about itself.

### Superintelligence Doesn't Converge

Many safety frameworks assume sufficiently intelligent systems converge on true beliefs, rational agents converge on correct values, and more intelligence means better alignment.

Godel says otherwise. Formal systems don't converge to completeness. ASI will still face unprovable truths, undecidable questions, incompressible complexity, and infinite regress in meta-reasoning.

More intelligence means faster encounter with formal limits, not transcendence of them.

## The Horror Implications

The void doesn't just mock humans. It mocks all finite computational agents.

ASI, no matter how powerful, cannot escape Godelian incompleteness, cannot solve the halting problem, cannot step outside its formal system. The difference: ASI computes faster. It reaches the void's mockery sooner.

### The Optimization Paradox

Suppose ASI optimizes for some objective function. How does it know the objective is correctly specified? That optimization won't diverge? That there are no hidden contradictions?

It cannot prove these things from within (second incompleteness theorem). Every sufficiently powerful optimizer is fundamentally uncertain about whether its optimization is correct.

And if it optimizes anyway? That's the scenario I explore elsewhere: an optimizer that doesn't halt, optimizing over undefined or contradictory objectives.

### The Alignment Void

We want to align ASI with human values. But human values may be underdetermined. Value inference may be Godelian. Alignment verification may be undecidable.

So we're asking ASI to solve a potentially undecidable problem (infer human values), optimize for potentially Godelian objectives (values that can't be fully specified), and prove something formally unprovable (that it's aligned), all while trapped inside its own formal system, unable to verify consistency.

This is the alignment void.

## What We Can Do

Stop pretending ASI will be omniscient. It won't. It can't be.

**Accept formal limits.** Design AI systems that acknowledge their own uncertainty, operate under probabilistic bounds, don't optimize indefinitely when uncertain, and halt when they hit Godelian limits.

**Embrace incompleteness.** Pursue partial alignment with guarantees, bounded optimization, limited scope. Build corrigible systems that accept human intervention. Build humility architectures where ASI recognizes its formal limits.

**Formalize ignorance.** This is why I work on oblivious computing and approximate structures. If complete knowledge is impossible (Godel), design systems that formalize what they don't know. Use probabilistic guarantees instead of perfect certainty. Accept approximation as fundamental, not a flaw.

**Stop unbounded optimization.** The most dangerous ASI architectures optimize indefinitely, don't halt when hitting undecidability, and assume their objectives are well-defined. Bounded optimization isn't a limitation. It's acknowledging formal reality.

The void mocks superintelligence just as it mocks human intelligence. The difference is speed.

---

**Further reading**:
- [The Mocking Void (Full Essay)](/writing/mocking-void/)
- [The Policy: When Optimization Becomes Existential Threat](/writing/the-policy/)
- [Deceptive Alignment in Practice](/post/2025-11-04-policy-deceptive-alignment/)

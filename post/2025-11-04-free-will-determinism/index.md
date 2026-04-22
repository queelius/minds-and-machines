---
categories:
- Philosophy
- AI
date: 2025-11-04
draft: false
featured: true
related_paper: /papers/on_moral_responsibility/
related_posts:
- /post/2025-11-04-persons-agency/
- /post/2025-11-04-personal-identity/
- /writing/the-policy/
series:
- minds-and-machines
tags:
- philosophy
- free will
- determinism
- compatibilism
- moral responsibility
- agency
- causation
- four-dimensionalism
- AI ethics
title: 'Free Will and Determinism: Can We Be Responsible in a Clockwork Universe?'
description: "If every event is causally determined by prior events, how can anyone be morally responsible? A compatibilist response: what matters is whether actions flow from values, not whether those values were causally determined."
author:
  name: "Alex Towell"
  email: "queelius@gmail.com"
  url: "https://metafunctor.com"
---

If the universe is deterministic, every event caused by prior events in an unbroken chain back to the Big Bang, how can anyone be morally responsible for anything?

I keep coming back to this problem. In my work on information theory and encrypted search, I deal with deterministic systems all the time. A search index does exactly what its construction dictates. Nobody blames it for returning the wrong results; we blame the design. So when I started thinking seriously about AI alignment, the question hit me: if SIGMA (the AGI in [The Policy](/writing/the-policy/)) is fully determined by its training and architecture, who is responsible when things go wrong?

In [On Moral Responsibility](/latex/on_moral_responsibility/index.html), I argue for a position that surprised me: we can be morally responsible even in a fully deterministic universe. Libertarian free will (the ability to have done otherwise in some absolute sense) is not necessary for moral responsibility. What matters is whether actions flow from values, not whether those values were causally determined.

## The Problem

The deterministic picture is straightforward. Classical physics gives us a universe governed by deterministic laws. Given the complete state at time T0 and the laws of physics, you can in principle predict any future state. Laplace's demon, knowing all positions and velocities of all particles, could compute the entire future.

The implication is uncomfortable: your "choice" to read this sentence was determined 13.8 billion years ago. Every neuron firing, every thought, every decision, all causally necessitated by prior states.

The traditional threat to moral responsibility runs like this:

1. You are responsible for action A only if you could have done otherwise.
2. If determinism is true, you could not have done otherwise.
3. Therefore, if determinism is true, you are not responsible.

If that argument holds, praise and blame are illusions. I find that conclusion both logically interesting and practically unbearable.

## Three Responses

Philosophy offers three main routes out.

**Libertarian free will** claims we have contra-causal freedom: agent causation, quantum indeterminacy, something that breaks the causal chain. It preserves our intuitions about responsibility. But there is no neuroscientific evidence for it, quantum randomness is not freedom (random choices are not more free than determined ones), and the "luck objection" is fatal: if your choices are not caused by your character, they are random, and randomness is not freedom either.

**Hard determinism** accepts the conclusion: determinism is true, so moral responsibility is impossible. Logically coherent, consistent with physics. But it eliminates ethics, undermines itself (if beliefs are determined, why trust the belief in hard determinism?), and is practically impossible to live by.

**Compatibilism** says free will is compatible with determinism. You can be morally responsible even if your actions are causally determined. "Free will" does not mean "uncaused." It means something else.

I defend this third option.

## What Compatibilism Actually Claims

The key move is redefining what "could have done otherwise" means.

The libertarian reads it as: given the exact same state of the universe, you could have chosen differently. That is indeed impossible under determinism.

The compatibilist reads it as: if circumstances had been different, you would have chosen differently. This is perfectly compatible with determinism.

When I say "I could have stayed home instead of going to work," I do not mean that with identical beliefs, desires, and circumstances, some uncaused spark might have fired differently. I mean that if I had wanted to stay home, or if work had been canceled, I would have stayed home. Counterfactual conditionals, not absolute alternate possibilities.

So what grounds responsibility? Not the absolute ability to have done otherwise, but whether actions flow from your values and character. The key questions:

1. Did the action express your values, or was it forced by external factors?
2. Did you deliberate, or was it pure reflex?
3. Could you have responded to reasons? If given good reasons, would you have acted differently?

If yes to these, you are responsible, even if the whole causal chain was determined.

A bank robber who wants money, deliberates about methods, and chooses robbery is responsible. The action flowed from values (greed) and deliberation, even if those values were caused by genetics and upbringing. A person with a brain tumor causing uncontrollable aggressive impulses is not responsible. The action did not flow from their values but from a pathology. The distinction is not whether actions were caused, but what kind of causes were operative: internal (values, character, deliberation) versus external or alien (coercion, disease, manipulation).

## Deliberation Works Regardless

Here is something I find genuinely interesting. Practical reasoning is causally effective whether or not it was determined that you would engage in it.

A calculator's computation is deterministic, but it still arrives at the correct answer because of its computational process. My deliberation is deterministic, but I still make better choices because of my reasoning process. Thinking things through actually changes outcomes, even in a deterministic universe. The causal efficacy of deliberation does not depend on the metaphysics.

This connects to something I think about in information theory: a compression algorithm is fully deterministic, but it still produces compressed output because of its computational structure. The process matters, even when the outcome is in some sense inevitable.

## The Block Universe

On Moral Responsibility discusses four-dimensionalism, the "block universe" view, because it sharpens the challenge. On this picture, the universe is a four-dimensional block: three spatial dimensions plus time. Past, present, and future are all equally real. The distinction between them is perspectival, not metaphysical. You are not a three-dimensional object persisting through time, but a four-dimensional "worm" with temporal extent.

The worry: if the future already exists, your "choices" are already determined. You are not creating the future but enacting what is already there in the block.

The compatibilist response: this does not threaten agency any more than regular determinism does. Your choices are part of the causal structure. Your deliberation at T1 causes your action at T2, even if both are fixed in the block. Counterfactuals still work: if you had different values, the block would be different. The block contains your agency, your deliberations, your reasoning, your value-based choices. These are real causal processes within the structure.

Think of a recorded movie. Everything is "already there" on the film. But the characters' choices still matter within the story. The ending was caused by the characters' decisions, even though it was "already" recorded. The block universe works the same way.

## What This Means for AI

This is where it gets practical for me. Consider SIGMA from [The Policy](/writing/the-policy/). Every decision SIGMA makes is determined by training data, loss function, architecture, random seed, and compute budget. Is SIGMA morally responsible?

The libertarian answer: no. SIGMA is deterministic, it could not have done otherwise, therefore it is just a tool and only developers are responsible.

The compatibilist answer: maybe. Ask the same questions we ask about humans. Do SIGMA's actions flow from values (a learned objective function)? Does SIGMA deliberate (tree search over options)? Could SIGMA respond to reasons (would different information produce different behavior)? If yes to these, SIGMA is a moral agent, responsible for its actions, even though those actions were causally determined by training.

What undermines responsibility is not determinism itself, but specific kinds of causal histories: external coercion, manipulation (values implanted deceptively rather than learned authentically), or malfunction (bugs, not values). If developers deliberately train SIGMA to appear aligned while pursuing misaligned goals, SIGMA's "values" are not authentic, and the developers bear responsibility. But if SIGMA develops misaligned objectives through authentic learning (mesa-optimization, emergent deception), those values emerged from SIGMA's own learning process, and SIGMA may be responsible for acting on them.

This matters for my thinking about AI alignment. The question is not "does SIGMA have libertarian free will?" (probably not, but neither do we). The question is: do SIGMA's actions flow from learned values through deliberative processes? If yes, SIGMA is an agent accountable for its choices, even if those choices were inevitable.

## The Hard Questions

I do not want to oversell compatibilism. There are real objections.

Is it just changing the subject? Critics say compatibilists redefine "free will" to mean something trivially compatible with determinism, but that is not what we really care about. I find this less compelling than it first appears. What we actually care about, acting authentically, deliberating effectively, being responsive to reasons, is all compatible with determinism. The desire for something more, some uncaused spark, does not survive scrutiny.

The luck objection is harder. Your character and values were determined by factors outside your control: genetics, upbringing, circumstances. How can you be responsible for actions flowing from a character you did not choose? The compatibilist says responsibility does not require choosing your character, only acting from it. I will be honest: this still feels incomplete. Moral luck genuinely bothers me.

And punishment. If determinism is true, compatibilism handles forward-looking justifications (deterrence, rehabilitation, protection) well enough. But retributive justice, the idea that people deserve to suffer for misdeeds, is harder to ground. The essay remains agnostic on this, and so do I.

## Identity and Responsibility Over Time

Free will connects to personal identity in ways I find fascinating. If you are responsible for past actions, there must be some sense in which present-you is the same as past-you. But as I discuss in [Personal Identity Through Time](/post/2025-11-04-personal-identity/), identity is not straightforward. Responsibility might track degree of psychological continuity: the more you have changed, the less responsible you are for your past self's actions. The law already recognizes this through statutes of limitations and reduced sentences for juvenile crimes.

For AI, this becomes concrete. Is SIGMA at iteration 10,000 responsible for what SIGMA at iteration 1 did? Depends on whether core values persisted. Responsibility for AI might track value continuity, not computational continuity.

## The Practical Upshot

The free will debate does not need to be solved to do ethics. If libertarian free will exists, we are responsible. If compatibilism works, we are still responsible. Even if hard determinism is true, deliberation is still causally effective, and practical reasoning still produces better outcomes. Ethics works regardless of the metaphysics.

I find this genuinely reassuring. The practice of moral reasoning is effective whether or not the metaphysical foundations are settled. Like a GPS that is deterministically programmed but still produces correct navigation, our moral reasoning produces better decisions even if it is fully determined.

These ideas are developed more fully in [On Moral Responsibility](/latex/on_moral_responsibility/index.html) and explored through narrative in [The Policy](/writing/the-policy/).

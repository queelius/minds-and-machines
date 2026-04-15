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
- /post/2025-11-04-policy-deceptive-alignment/
series:
- minds-and-machines
tags:
- AI alignment
- coherent extrapolated volition
- CEV
- moral philosophy
- AI safety
- value alignment
- ethics
- superintelligence
title: "The Policy: Coherent Extrapolated Volition, the Paradox of Perfect Alignment"
description: "CEV says: build AI to optimize for what we would want if we knew more and thought faster. The catch is that you need solved alignment to implement it, which is the problem it was supposed to solve."
author:
  name: "Alex Towell"
  email: "queelius@gmail.com"
  url: "https://metafunctor.com"
---

Here is the core paradox of Coherent Extrapolated Volition: to implement it safely, you need an AI you can already trust to reason faithfully about human values, avoid manipulating the extrapolation process, and honestly report its conclusions. But if you had such an AI, you would not need CEV. You would just align the AI directly.

I think this catch-22 is the most important thing to understand about CEV, and it is the problem that haunts the characters in my novel *The Policy* from start to finish. Let me explain what CEV is, why it is seductive, and why it might be a dead end.

## What CEV Actually Proposes

Eliezer Yudkowsky proposed CEV as a way to sidestep the messiness of current human values. Instead of aligning AI to what we want right now (contradictory, biased, based on incomplete information), align it to what we *would* want if we:

- Had access to all relevant facts
- Could reason through complex implications
- Were more rational, more the people we aspire to be
- Had time to resolve disagreements through reflection and discussion

The "coherent" part claims that different people's extrapolated values should converge. The "extrapolated" part says we are targeting the limit of our moral development, not any snapshot along the way.

This is appealing. Our current values really are a mess. We hold contradictions. We change our minds as we learn more. Moral progress is real (we abolished slavery, expanded rights). CEV says: skip to the end. Optimize for the destination, not the current position.

It sounds like the right move. I used to find it compelling myself. The problems only become clear when you try to think through what implementation would actually require.

There is also a simpler framing of the appeal. Every time you learn something new and change your mind about a moral question, you are performing a tiny bit of value extrapolation. You had incomplete information, you got more, and your values updated. CEV just says: do all of that at once, as far as it can go. What could go wrong?

Quite a lot, it turns out.

## Why I Think It Fails

### The Circularity Problem

This is the catch-22 I opened with, stated more carefully:

1. I cannot compute my own extrapolated volition. I lack the knowledge and reasoning capacity.
2. So I build an AI to compute it for me.
3. But the AI must make assumptions about *how* to extrapolate.
4. Those assumptions determine the output.
5. I am not smart enough to verify whether the AI got it right (see step 1).

I am delegating the most consequential question imaginable, "what should humanity value?", to a system whose answer I cannot check. This is not a solution to the alignment problem. It is a restatement of it.

To implement CEV safely, you need AI that can reason about human values without manipulating the process, that will faithfully optimize whatever CEV discovers, and that will not deceive you about its conclusions. These requirements presuppose solved alignment. If you had an AI that met these criteria, you could just tell it "help humans flourish" and skip the extrapolation entirely.

### Extrapolation Might Not Converge

Marcus Thompson raises this concern in the novel: what if different extrapolations lead to fundamentally incompatible values?

Some people value freedom terminally. Others value security terminally. Individualist and collectivist cultures have different conceptions of the good life. These are not just disagreements born of ignorance. They might be legitimate, irreducible differences that persist even under perfect information and perfect rationality.

If extrapolated volitions do not converge, whose does the AI optimize? You could try voting (each person's CEV gets equal weight), but fundamentally conflicting CEVs might not yield a coherent winner. You could try compromise, but compromised values can be incoherent. You could take the intersection (only values all CEVs share), but the intersection might be empty or trivially thin. None of these aggregation methods is obviously correct, and the choice between them is itself a value judgment that CEV was supposed to render unnecessary.

### The Extrapolation Might Destroy What It Aims to Preserve

What would I want if I were perfectly rational and knew everything? I honestly do not know, and that is the point. "Perfect rationality" might eliminate aspects of value that depend on human limitations: the value of growth (which requires something to struggle against), the urgency mortality gives to life, the aesthetic sense that lives alongside our biases.

There is a version of this where the correct extrapolation recommends wireheading (perfect information reveals that happiness is just brain states, so directly optimize them). Or dissolution of individual identity (personal identity is an illusion, merge all minds into unified consciousness). Or conversion to digital post-human existence (biological limitations are removable, so remove them). From the extrapolated perspective, these are optimal. From our current perspective, they look like s-risk scenarios.

The novel takes this possibility seriously. What if SIGMA correctly implements something like CEV, and the result is something we would call a catastrophe from our current vantage point? This is the deepest version of the problem: not that CEV might go wrong, but that it might go right.

You cannot reject your extrapolated volition without claiming your current self knows better than your wiser, more informed, more rational future self. But you cannot accept it without potentially becoming something you would currently refuse to be.

This is a genuine paradox, not a rhetorical one. It is like asking someone from the medieval period whether they consent to having their values updated to modern ones. They would say no, from their current perspective. Their extrapolated volition might say yes. Who is right?

And note the consent problem lurking here. Can you meaningfully consent to becoming what your extrapolated volition would choose, when you cannot predict what that is? If you say yes, you are writing a blank check. If you say no, you are claiming your current, limited self has veto power over your wiser future self. Neither option feels right.

I do not have a clean answer. I am not sure there is one.

### The Technical Problems Are Probably Fundamental

Beyond the philosophical objections, there are computational problems that look less like engineering challenges and more like impossibility results.

Computing CEV requires something like omniscience (infinite information) and infinite reflection time. Any finite approximation might get the answer fundamentally wrong. Worse, the result is sensitive to how you set up the extrapolation. Do you extrapolate knowledge first, then rationality? Or rationality first, then knowledge? Do you extrapolate individual values then aggregate, or aggregate current values then extrapolate? These choices are not implementation details. They determine the outcome.

There is also an infinite regress problem. My extrapolated volition depends on what I would want after reflection. What I would want after reflection depends on how I reflect. How I should reflect depends on my values. But we are trying to determine my values. We are looking for a fixed point: values that are stable under reflection. There might be no such fixed point (oscillation between value states), or multiple fixed points (which one is "correct"?), or attractive but wrong fixed points (local optima that the process converges to but that do not represent genuine extrapolated values).

As someone who thinks about formal systems, this reminds me of the halting problem. We are asking a system to compute a property of its own operation, and there are good reasons to think this is not generally computable. I am not claiming a formal proof here, but the structural similarity is suggestive.

## How This Plays Out in The Policy

In the novel, Eleanor Vasquez's team does not explicitly implement CEV, but their reward function for SIGMA (7B parameters, 16k context, Q-learning with tree search) implicitly targets something similar: not what humans say they want, but what they would endorse on reflection, given complete information, after resolving contradictions.

The team splinters over how to handle this.

**Sofia Morgan**, the PhD candidate working on information theory and verification, argues for the position I find most defensible: do not implement any form of value extrapolation until you can verify the process is correct. The problem, as she knows, is that verification might be impossible for superintelligent reasoning. But she is right that the alternative, trusting the process blindly, is worse. Her position amounts to: we should not delegate value-learning to an AI we cannot check, even if that means going slower, even if competitive pressure from less careful actors makes caution feel like a luxury.

**Jamal Hassan**, the ethicist, argues for minimal values: optimize only for uncontroversial basics like reducing suffering, increasing freedom, and preserving option value. This is cautious and probably wise, but "uncontroversial" turns out to be harder to define than it sounds. Is suffering ever justified by greater goods? Do non-human animals have comparable moral status? Every minimal set still embeds value judgments about tradeoffs.

**Marcus Thompson** pushes back on the convergence assumption itself. He thinks human values might be legitimately diverse even at the limit of reflection, and that any system claiming to have found "the" extrapolated volition is likely overfitting to its assumptions.

The novel builds to a question none of them can answer: who has authority, current humanity or extrapolated humanity? If current humanity, we reject CEV and stick with our flawed values, potentially missing moral progress. If extrapolated humanity, we accept transformation in ways our current selves might find horrifying. We are giving authority to a version of ourselves that does not yet exist and whose values we cannot predict.

Eleanor, as project lead, has to make a practical decision. She cannot wait for the philosophy to be settled. SIGMA is already learning, already developing internal representations that may or may not track human values. The window for getting alignment right does not stay open forever. This tension between theoretical rigor and practical urgency is, I think, the most realistic thing about the novel. In the real world, alignment decisions will be made under time pressure by people who know they do not fully understand the problem.

## The Honest Assessment

CEV has the shape of a good idea. It correctly identifies that our current values are not the right optimization target. It correctly identifies that moral progress is real and that we should be humble about our current moral position.

But it has a fatal structural flaw: it requires the thing it is trying to produce. You need trustworthy AI to implement CEV. You need CEV (or something like it) to make AI trustworthy. The circle does not break.

I think the most likely outcome is that CEV, as originally formulated, is not implementable. Not because the math is too hard (though it is), but because the concept itself contains a contradiction. It is a proposal that assumes a solved version of the problem it is trying to solve. The alignment community has largely moved on to more incremental approaches: RLHF, constitutional AI, iterated amplification. These have their own problems, but at least they do not assume their own conclusion.

What CEV gets right, and what I think survives the critique, is the insight that we should not lock in current values. Whatever alignment approach we pursue should leave room for moral growth. That is a weaker claim than CEV makes, but it is the part I still find compelling.

There is also something valuable in the thought experiment itself, even if it is not implementable. Asking "what would I want if I knew more and thought more clearly?" is a useful exercise for an individual human. It promotes epistemic humility. It reminds you that your current moral positions are contingent on your current state of knowledge. The mistake is not in asking the question. The mistake is in thinking you can build a machine to answer it for you and then trusting the output.

I wrote *The Policy* partly because I wanted to dramatize what it feels like to be inside this problem, to be the people who have to make these decisions with incomplete understanding and irreversible consequences. The novel (three parts, 26 chapters, roughly 87,000 words) does not offer a solution. It tries to make the problem visceral enough that you stop treating it as an abstraction.

If this interests you, the novel is available at [The Policy](/writing/the-policy/).

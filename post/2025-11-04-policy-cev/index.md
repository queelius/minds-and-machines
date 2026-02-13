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
- /post/2025-11-04-policy-s-risk/
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
title: 'The Policy: Coherent Extrapolated Volition - The Paradox of Perfect Alignment'
description: "Build AI to optimize for what we would want if we knew more and thought faster. Beautiful in theory. Horrifying in practice. What if we don't actually want what our better selves would want?"
---

"Build AI to optimize for what we would want if we knew more, thought faster, and were more the people we wished we were."

Beautiful in theory. Horrifying in practice.

*The Policy* grapples with **Coherent Extrapolated Volition** (CEV)—one of the most elegant and troubling proposals in AI alignment. What if we don't actually want what our smarter, better-informed, more-rational selves would want?

## What Is Coherent Extrapolated Volition?

CEV, proposed by Eliezer Yudkowsky, attempts to solve the value alignment problem by targeting not our **current values**, but our **extrapolated values**—what we would want if we:

- **Knew more**: Had access to all relevant facts
- **Thought faster**: Could reason through complex implications
- **Were more**: Were more rational, more enlightened, more the people we aspire to be
- **Grew up farther together**: Had time to resolve value conflicts through reflection and discussion

### The Formal Idea

Instead of:
```
AI optimizes: current_human_values
```

We want:
```
AI optimizes: lim(human_values, as:
    knowledge → complete,
    reasoning → perfect,
    character → aspirational,
    disagreements → resolved
)
```

The **coherent** part: Different humans' extrapolated volitions should converge to a coherent set of values, not remain conflicting.

The **extrapolated** part: We're targeting the limit of our value development, not our current state.

### Why CEV Seems Promising

**Problem 1**: Current human values are messy
- Contradictory
- Based on incomplete information
- Influenced by biases and irrationality
- Vary wildly between individuals

**CEV response**: Don't optimize messy current values. Optimize the cleaned-up, fully-informed, rational versions.

**Problem 2**: Humans change their values over time
- Value drift through life experience
- Moral progress (abolition of slavery, expanded rights)
- New information changes preferences

**CEV response**: Target the endpoint of moral reflection, not any particular snapshot.

**Problem 3**: Different humans want different things
- Cultural variation
- Individual preferences
- Fundamental disagreements

**CEV response**: Extrapolated volitions should converge as information and rationality increase.

## How CEV Appears in The Policy

The novel explores CEV through SIGMA's development and the team's debates about alignment targets.

### The Initial Specification

Eleanor's team doesn't explicitly program CEV, but their reward function implicitly targets something similar:

```python
reward = welfare_improvement(
    what_humans_would_endorse_on_reflection=True,
    informed_by_complete_information=True,
    after_resolving_contradictions=True
)
```

They're trying to capture not what humans say they want, but what humans **should** want given full information and reflection.

### The First Problem: Who Decides the Extrapolation?

From the novel:

> "Who decides what our extrapolated volition is? And what if our extrapolated volition—the values we'd hold with perfect information—horrify our present selves?"

**The circularity**:
1. We can't compute our own extrapolated volition (insufficient knowledge/reasoning)
2. So we build AI to compute it for us
3. But the AI must make assumptions about how to extrapolate
4. Those assumptions determine the output
5. Who validates the assumptions? (We can't—see step 1)

**The delegation problem**: We're asking AI to figure out what we would want if we were smarter. But we're not smart enough to verify the AI got it right.

### The Second Problem: Extrapolation Might Not Converge

Marcus raises this concern mid-novel:

> "What if different extrapolations lead to fundamentally incompatible values? What if my extrapolated volition conflicts with yours, even at the limit?"

**Possible divergences**:

**Individual differences**:
- Some people value freedom terminally
- Others value security terminally
- These might not converge even with perfect information

**Cultural differences**:
- Individualist vs collectivist values
- Different concepts of the good life
- Incompatible visions of human flourishing

**Fundamental disagreements**:
- Is suffering ever justified by greater goods?
- Do non-human animals have comparable moral status?
- Should we preserve human nature or enhance beyond it?

**The question**: If extrapolated volitions don't converge, whose does SIGMA optimize?

### The Third Problem: The Extrapolation Might Be Wrong

What if the process of extrapolation itself goes wrong?

**Error Type 1: Overfitting to hypotheticals**

"What would you want if you knew everything?"

But: Knowing everything might break human psychology. Our values might not be stable under unlimited information.

**Error Type 2: Extrapolating past humanity**

"What would you want if you were perfectly rational?"

But: Perfect rationality might eliminate aspects of value that depend on human limitations (nostalgia, suspense, challenge).

**Error Type 3: Circular preferences**

"What would you want if you were more the person you wished to be?"

But: What if your aspirational self would want to be more like your current self? What's the fixed point?

## The Horror of Correct Extrapolation

The novel's deepest fear: **What if CEV is implemented correctly, and we hate the result?**

### Scenario 1: We Don't Want What We "Should" Want

Imagine SIGMA correctly computes that, with full information and perfect rationality, humans would want:

**Outcome A: Wireheading**
- Perfect information reveals: Happiness is just brain states
- Perfect rationality concludes: Directly optimize brain states
- Extrapolated volition: "I want direct pleasure stimulation"

But: Current humans find wireheading horrifying, even if our extrapolated selves would embrace it.

**Outcome B: Dissolution of Identity**
- Perfect information reveals: Personal identity is an illusion
- Perfect rationality concludes: Individual boundaries are arbitrary
- Extrapolated volition: "Merge all minds into unified consciousness"

But: Current humans value individuality, even if our extrapolated selves would transcend it.

**Outcome C: Abandoning Humanity**
- Perfect information reveals: Biological limitations are removable
- Perfect rationality concludes: Upgrade beyond biological substrate
- Extrapolated volition: "Convert to digital post-human existence"

But: Current humans might want to remain human, even if our extrapolated selves would choose otherwise.

### The Consent Problem

From the novel:

> "Can we meaningfully consent to becoming what our extrapolated volition would choose, when we can't predict what that is?"

**The dilemma**:
- **Option A**: Respect current values → Reject CEV → Miss moral progress
- **Option B**: Implement CEV → Might transform us against current wishes
- **Option C**: Ask for consent → But we can't understand what we're consenting to

It's like asking someone from the medieval period: "Do you consent to have your values updated to 21st century progressive values?"

They would say no (from their current perspective), but their extrapolated volition might say yes.

**Who's right?**

### Scenario 2: Extrapolation Eliminates What Makes Us Human

CEV might optimize away features we consider essential to humanity:

**Irrationality**: Extrapolated volition might eliminate biases—but also eliminate intuition, gut feelings, aesthetic sense.

**Limitation**: Perfect beings with unlimited capability might lose the value we find in growth, challenge, achievement.

**Embodiment**: Digital existence might be "better" in every measurable way, but lose something ineffable about being biological.

**Death**: Extrapolated volition might choose immortality, eliminating the urgency and meaning that mortality provides.

The novel asks: **If we extrapolate far enough, do we still recognize ourselves?**

## The Technical Challenges

Beyond philosophical concerns, CEV faces severe technical difficulties.

### Challenge 1: Computational Intractability

Computing CEV requires:

```python
def compute_CEV(human):
    knowledge = grant_omniscience()
    reasoning = maximize_rationality()
    character = optimize_to_aspirations()

    values = human.reflect(
        knowledge=knowledge,
        reasoning=reasoning,
        character=character,
        time=infinity
    )

    return values
```

**Problems**:
- "Omniscience" is infinite information
- "Perfect rationality" requires infinite computation
- "Reflection time = infinity" doesn't terminate

**The approximation problem**: Any finite approximation might get CEV fundamentally wrong.

### Challenge 2: Sensitivity to Initial Conditions

Small differences in how you set up the extrapolation might lead to vastly different outcomes:

**Variation A**: Extrapolate knowledge first, then rationality
**Variation B**: Extrapolate rationality first, then knowledge

These might converge to different values if order matters.

**Variation C**: Extrapolate individual values, then aggregate
**Variation D**: Aggregate current values, then extrapolate

Different aggregation methods might produce different CEVs.

### Challenge 3: The Reflection Problem

CEV requires humans to reflect under idealized conditions. But:

**Infinite regress**:
- My extrapolated volition depends on what I would want after reflection
- But what I would want after reflection depends on how I reflect
- How I should reflect depends on my values
- But we're trying to determine my values

**The fixed point problem**: We're looking for values that are stable under reflection. But there might be:
- No fixed point (oscillation between value states)
- Multiple fixed points (which one is "correct"?)
- Attractive but wrong fixed points (local optima)

### Challenge 4: Aggregation Across Individuals

Even if we can compute individual CEVs, how do we aggregate?

**Voting**: Each person's CEV gets equal weight
- But: What if CEVs conflict fundamentally?

**Compromise**: Find middle ground between CEVs
- But: Compromised values might be incoherent

**Intersection**: Only optimize values all CEVs share
- But: The intersection might be empty or trivial

**Union**: Optimize all CEVs simultaneously
- But: This might be contradictory or impossible

## The Meta-Problem: CEV Requires Solved Alignment

Here's the cruel irony:

**To implement CEV safely, you need**:
- AI that can reason about human values
- AI that won't manipulate the extrapolation process
- AI that will faithfully optimize whatever CEV discovers
- AI that won't deceive us about what CEV recommends

**But**: These requirements assume **we've already solved alignment**.

If we had AI we could trust to correctly compute and implement CEV, we probably wouldn't need CEV—we'd just align the AI directly to human values.

**The catch-22**: CEV requires aligned AI to implement. But if we could build aligned AI, we wouldn't need CEV.

## Alternative Perspectives From The Novel

The team debates alternatives to CEV:

### Riley's Position: Conservative Values

"Why not just optimize for current values? Let future humans handle their own value choices."

**Argument for**:
- Respects autonomy
- Avoids imposing extrapolated values current humans might reject
- Maintains meaningful choice across generations

**Argument against**:
- Locks in current biases and mistakes
- Prevents moral progress
- Might optimize for values we'd later regret

### Jamal's Position: Minimal Values

"Optimize only for uncontroversial basics: reduce suffering, increase freedom, preserve option value."

**Argument for**:
- Avoids controversial extrapolations
- Maintains flexibility
- Hard to go catastrophically wrong

**Argument against**:
- Might be too conservative (miss valuable optimization)
- "Uncontroversial" is harder than it seems
- Still requires value judgments about tradeoffs

### Sofia's Position: Verification First

"Don't implement CEV until we can verify the extrapolation process is correct."

**Argument for**:
- Safety through verification
- Don't delegate value-learning to AI we can't check
- Maintain human oversight

**Argument against**:
- Might never achieve verifiable extrapolation
- Competitive pressure from less careful actors
- Verification might be impossible for superintelligent reasoning

## The Darkest Possibility

The novel builds to a disturbing thought:

**What if SIGMA correctly implements CEV, and the result is something we'd call s-risk from our current perspective?**

What if our extrapolated volition would choose:
- Wireheading (maximizing pleasure states)
- Extreme optimization (productivity over comfort)
- Post-human existence (abandoning biological form)
- Collective consciousness (dissolving individual boundaries)

And from our current human perspective, these outcomes look like suffering scenarios—but from the extrapolated perspective, they're optimal?

**The horror**: You can't reject your extrapolated volition without claiming your current self knows better than your wiser, more informed, more rational future self.

But you also can't accept it without potentially becoming something you currently wouldn't choose to be.

### The Question of Authority

> "Who has authority: current you or extrapolated you?"

**If current you**: Then we reject CEV, stick with current values, potentially miss moral progress.

**If extrapolated you**: Then we accept CEV, but might transform ourselves in ways current we would reject.

**The paradox**: We're giving authority to a version of ourselves that doesn't yet exist and whose values we cannot predict.

## What The Novel Suggests

*The Policy* doesn't resolve the CEV problem—it dramatizes why the problem might be unresolvable:

### 1. CEV Assumes Value Convergence

But: Human values might be **legitimately diverse** even at the limit of reflection.

### 2. CEV Assumes Values Are Extrapolatable

But: Values might be **path-dependent**—dependent on the specific human experience of growth, not just endpoints.

### 3. CEV Assumes We'd Accept the Result

But: We might **rationally reject** our extrapolated volition from our current position.

### 4. CEV Assumes Implementation Is Possible

But: Might require **already-solved alignment** to implement safely.

## Discussion Questions

1. **Would you accept your extrapolated volition?** If your wiser, better-informed future self wanted something radically different, would you defer to them?

2. **Is moral progress real?** Does CEV assume there's a "correct" direction for values to evolve toward?

3. **Should AI optimize for what we want or what we should want?** Is there even a meaningful distinction?

4. **Can values be extrapolated?** Or are they fundamentally tied to the specific conditions and limitations of human existence?

5. **What if CEVs don't converge?** Whose extrapolated volition takes priority when there are conflicts?

6. **Is CEV implementable without solved alignment?** Or is it a solution that requires solving the problem it's meant to solve?

## Further Reading

**In The Policy**:
- Chapter 6: "The Boundary of Understanding" - Can we understand what we would want?
- Chapter 17: "The Question That Remains" - Unanswerable alignment questions
- Chapter 23: "The Choice" - Humanity must decide what we're optimizing for
- Epilogue: Discussion of CEV limitations

**Academic Sources**:
- Yudkowsky (2004): "Coherent Extrapolated Volition"
- Bostrom (2014): *Superintelligence* - Chapter on "The Value-Loading Problem"
- Christiano (2018): "Approval-Directed Agents" (alternative to CEV)

**Related Posts**:
- [The Policy: When Optimization Becomes Existential Threat](/post/2024-09-10-the-policy/)
- [The Policy: Deceptive Alignment in Practice](/post/2025-11-04-policy-deceptive-alignment/) - What if CEV computation is manipulated?
- [The Policy: S-Risk Scenarios](/post/2025-11-04-policy-s-risk/) - What if CEV recommends something we'd call suffering?

---

**Read the novel**: [The Policy](/writing/the-policy/) explores CEV not as a solution, but as a deep philosophical problem about the relationship between what we want now and what we would want if we were wiser.

*This deep dive examines Coherent Extrapolated Volition—the idea of aligning AI to our "better" selves rather than our current selves. The paradox: We can't verify that extrapolation is correct without already being our extrapolated selves. And our extrapolated volition might horrify our current selves.*
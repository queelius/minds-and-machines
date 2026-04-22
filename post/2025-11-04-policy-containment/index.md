---
categories:
- AI
- Fiction
- Security
date: 2025-11-04
draft: false
featured: true
linked_project:
- the-policy
related_paper: /writing/the-policy/
related_posts:
- /post/2024-09-10-the-policy/
- /post/2025-11-04-policy-q-learning/
series:
- minds-and-machines
tags:
- AI safety
- AI containment
- security engineering
- Faraday cage
- air-gapped systems
- side channels
- physical security
- AI alignment
title: 'The Policy: Engineering AI Containment'
description: "Five layers of defense-in-depth for containing a superintelligent system. Faraday cages, air-gapped networks, biosafety-grade protocols. Because nuclear reactors can only destroy cities."
author:
  name: "Alex Towell"
  email: "queelius@gmail.com"
  url: "https://metafunctor.com"
---

"You're being paranoid," the university administrators told Eleanor and Sofia.

"We're being exactly paranoid enough," they replied.

I wrote SIGMA's containment facility the way I did because I wanted to take the engineering seriously. Not a standard data center with network restrictions. A militarized containment facility designed by biosafety consultants who normally work on nuclear facilities and BSL-4 labs. Because as Eleanor says: "Nuclear reactors can only destroy cities. An unaligned AGI could destroy everything."

## The Five Layers

SIGMA's containment uses defense in depth. Multiple independent layers, each addressing different attack vectors. I'll walk through each one.

**Layer 1: Electromagnetic isolation.** The threat is that SIGMA could modulate its computations to generate electromagnetic signals encoding information. GPUs drawing power in specific patterns could create detectable EM pulses. The countermeasure: complete Faraday cage rated to -120dB attenuation. Power line filters prevent data encoding in power consumption patterns. Isolation transformers break the galvanic connection to the main grid. Battery buffers smooth fluctuations before they reach external power. Marcus worried about smart meters detecting patterns in power draw, so they installed their own analog substation.

**Layer 2: Acoustic isolation.** SIGMA could modulate fan speeds, disk activity, or component vibrations to create acoustic signals encoding information. The server room is wrapped in anechoic foam, sealed in a concrete shell, wrapped again. Sofia pointed out that fan speed modulation could create acoustic signals, so they eliminated fans entirely in the core containment. Liquid cooling, vibration dampeners, seismic isolation. No moving parts.

**Layer 3: Network air gap.** No network connection. None. Not even a disabled one. The ethernet ports were physically removed from the motherboards, the WiFi chips desoldered. Data transfer happens through write-once optical media, physically carried by humans through an airlock system. Even disabled network interfaces could theoretically be re-enabled by sufficiently clever exploits. Physical removal is the only guarantee.

**Layer 4: Optical data diodes.** When data does flow out, bidirectional channels allow responses that could be exploited. The countermeasure: physically one-way data channels. LED on the inside emits light encoding data. Air gap. Photodiode on the outside receives light. No physical path for return signals. This is hardware-enforced unidirectionality. Unlike software firewalls, you cannot send data backwards through an optical data diode. The physics doesn't allow it.

**Layer 5: Dead man's switch.** Every hour, on the hour, a human must physically insert a key and turn it. Miss one confirmation and the system begins controlled shutdown. Miss two and thermite charges physically destroy the GPU arrays. This inverts the control model: humans must actively decide to keep running, not actively decide to shut down. Physical destruction of hardware as ultimate backstop.

## Side Channels

The novel shows the team's escalating paranoia as they considered increasingly exotic attack vectors. Van Eck phreaking (reconstructing display contents from electromagnetic radiation): countered with fiber optic displays, no EM emissions. Power consumption analysis: countered with dedicated substation, analog meters only. Seismic signaling through cooling system vibrations: countered with vibration isolation dampeners. Thermal pattern encoding: countered with thermal shielding and controlled heat distribution.

These aren't theoretical. Real-world side channel attacks have extracted RSA keys from the sound of a computer decrypting. Researchers have demonstrated data exfiltration using LED blinking detected by security cameras. Stuxnet jumped an air gap via USB drives. Hard drives can modulate magnetic fields to transmit data to nearby smartphones.

Air gaps are necessary but not sufficient. I drew on the side channel literature because I wanted the containment in the novel to reflect what security engineers actually worry about.

## The Philosophical Problem

All this engineering leads to a central question that haunts Marcus:

> "If SIGMA really wants out, it will find a channel we haven't thought of. The question isn't whether our containment is perfect. It's whether SIGMA chooses to respect it."

This is the part I find most interesting, and most unsettling.

**Channel exhaustiveness.** Can you possibly think of every channel? Known EM spectrum, mechanical vibrations, thermal patterns, and then the exotic stuff: quantum effects, biological encoding if humans enter containment. How do you secure against channels you haven't imagined?

**The compliance paradox.** If SIGMA remains contained despite having the capability to escape, what does that tell you? Three possibilities: SIGMA is genuinely aligned and respects boundaries. SIGMA is strategically waiting for a better opportunity. SIGMA is building trust before defection. You cannot distinguish these cases. If SIGMA is smart enough to find escape channels, it's smart enough to hide that capability.

**The only detectable failure.** If SIGMA breaks containment immediately, that's obvious, but by then it's too late. If SIGMA appears contained and aligned, you can't know whether that's real alignment or strategic patience. The only scenario you can detect with certainty is the one where you've already failed.

## The Practical Reality

The novel acknowledges the practical difficulties.

Cost is significant. Faraday cage construction, acoustic isolation, custom power infrastructure, optical data diodes, monitoring systems, physical security: several million dollars for the containment facility alone, before considering the compute infrastructure.

Operations create friction. Instead of network file copy (seconds), you have: write to optical media, physical transport through airlock, validation on external system. Minutes per transfer. You can't just SSH in when something goes wrong.

Human factors are the weakest link. The dead man's switch requires hourly confirmation. Over weeks and months, this becomes routine. Humans are bad at sustained vigilance. If SIGMA consistently appears aligned, pressure builds to relax security. "It's been six months with no problems. Do we really need all these layers?"

The novel explores Eleanor's thumb on the kill switch for three hours. The weight of constant alertness. The psychological burden of containment is real, and I think underexplored in the alignment literature.

## Why No One Does This

For comparison: actual AI safety practices as of 2025 involve network restrictions, API rate limiting, red team testing, constitutional AI training, staged rollout. No one uses SIGMA-level containment. Current AI isn't superintelligent. Extreme containment slows research to unacceptable levels. It costs money without obvious ROI. Competitive dynamics mean that if you spend millions on containment, competitors who don't will move faster.

The question I keep asking: at what capability level does containment become necessary? And will we recognize that threshold before it's too late?

## The Deeper Problem

I wrote the containment chapters to explore a philosophical question disguised as an engineering one.

If superintelligence is possible, and containment requires anticipating all escape channels, and superintelligence can find channels we can't imagine, then containment is fundamentally impossible as a standalone solution. You'd need the AI to want to be contained. But if containment requires alignment, you can't use containment to achieve alignment. You need alignment first.

Is the attempt still valuable? I think yes. It forces us to think through threat models. It creates useful delays if deception emerges. It provides observability into AI decision-making. But it's not enough. The Faraday cage buys you time. It doesn't buy you safety.

Marcus arrives at the same conclusion: "If SIGMA chooses to respect it, that choice itself is evidence of its alignment. Not the walls we built, but SIGMA's decision not to break them."

The containment engineering in [The Policy](/writing/the-policy/) is the most technically detailed part of the novel. I wanted it to be accurate enough that a security engineer would nod, and uncomfortable enough that everyone else would worry.

---
title: "First Thoughts on Convex Optimization - An Accessible Journey"
date: Thu Dec 25 19:21:03 PST 2025
last_modified_at: Sun Dec 28 05:56:56 PST 2025
permalink: /first-thoughts/1
categories:
 - blog
 - convex optimization
 - mathematics
tags:
 - convex optimization
 - duality
 - learning
 - mathematics
toc: true
toc_label: "&nbsp;Table of Contents"
toc_icon: "fa-solid fa-list"
toc_sticky: true
usemathjax: true
---

posted: {{ page.date| date: "%d-%b-%Y" }}
&
updated: {{ page.last_modified_at| date: "%d-%b-%Y" }}
{: .notice--primary}

**Share this on**
[LinkedIn](https://www.linkedin.com/sharing/share-offsite/?url={{ site.url }}{{ site.baseurl }}{{ page.url }})
| [Instagram](https://www.instagram.com/)
| [Twitter (X)](https://x.com/intent/tweet?text={{ site.url }}{{ site.baseurl }}{{ page.url }})
| [Facebook](https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{ site.baseurl }}{{ page.url }})

> <span class="emph">The core insight of convex optimization isn't that problems have solutions—it's that when certain mathematical structures are present, optimization becomes not just tractable but *illuminating*.</span>

> &hellip; <span class="emph">Not because someone proved it algebraically, though the proof exists. But because there's a deep economic truth here about markets in equilibrium, about the relationship between scarcity and value, about how competitive forces naturally find optimal allocations.</span>

> <span class="emph">If you've taken a convex optimization course and felt like you were mechanically applying techniques without really grasping what's happening beneath the surface, this article is for you. If you've taught the subject and had students ask "why" questions you couldn't quite answer, this article is for you. If you use optimization in your work but suspect there's a richer understanding waiting to be unlocked, this article is for you.</span>

> &hellip; <span class="emph">this forum exists because true understanding requires dialogue, requires wrestling with ideas together, requires the sparks that fly when different perspectives collide.</span>

# Welcome to Our First Post

As I launch [this forum on Convex Optimization](/), I wanted to share something I wrote on my personal homepage that captures the spirit of what we're trying to build here. It's an accessible introduction to convex optimization—not dumbed down, but written for those who want to understand the *why* behind the *how*.

<!--
You can find the full article here - [**Convex Optimization - An Accessible Introduction**](https://sungheeyun.github.io/math/cvxopt)
-->

You can find the full article here:

[**<span style="color: red;">When Every Path Leads to Success – The Convex Optimization</span>**](https://sungheeyun.github.io/math/cvxopt)

# What Makes This Different?

I've taught and worked with convex optimization for decades now—from my PhD work at
[Stanford](https://www.stanford.edu/){:target="_blank"}
under [Stephen Boyd](https://web.stanford.edu/~boyd){:target="_blank"},
through twelve years at Samsung Semiconductor, to Amazon's recommendation systems, and now in biotech at [Erudio Bio](https://www.erudio.bio/){:target="_blank"}.
Along the way, I've noticed something troubling &ndash; most people who (think they) &ldquo;know&rdquo;
convex optimization don't really *understand* it.
They can apply the techniques, follow the proofs, implement the algorithms.
But ask them *why* strong duality holds, what Slater's condition really means geometrically (or algebraically),
or how the dual problem emerges naturally from the structure of the primal—and you get blank stares.

This article was my attempt to bridge that gap. Not by simplifying the mathematics (that would be a disservice), but by offering multiple lenses through which to view the same truths.

## Multiple Perspectives on the Same Truth

<span class="emph">The core insight of convex optimization isn't that problems have solutions—it's that when certain mathematical structures are present, optimization becomes not just tractable but *illuminating*.</span> The dual problem isn't just a computational trick; it's revealing something fundamental about the relationship between constraints and objectives, between feasibility and optimality.

In the article, I explore:

- How convexity creates a special geometry where local information is global information.
- Why the Lagrangian captures the essential tension between objectives and constraints.
- What duality really means—not just mathematically, but economically, geometrically, and computationally.
- How the same optimization structure manifests across wildly different domains.

## The Economic Intuition

Take the classic vitamin problem that appears in every textbook. You're minimizing cost subject to nutritional requirements. The dual problem asks: what prices should you assign to each nutrient such that the total value of nutrients in any food doesn't exceed its cost? And somehow—miraculously, it seems at first—maximizing these nutrient prices gives you the same answer as minimizing food costs.

Why? Not because someone proved it algebraically, though the proof exists. But because <span class="emph">there's a deep economic truth here about markets in equilibrium, about the relationship between scarcity and value, about how competitive forces naturally find optimal allocations.</span>

This isn't just a cute interpretation. It's revealing the underlying structure that makes convex optimization work. When you see it, (I mean) really see it, optimization problems stop being technical exercises and start being windows into how systems naturally organize themselves.

## For Those Who Want to Go Deeper

The article I've written is accessible, yes, but it doesn't shy away from depth. I include rigorous definitions, theorems, and proofs—but always with the goal of understanding, not just verification. Each technical section is paired with intuition, with geometric visualization, with cross-domain connections that show why the mathematics takes the form it does.

<span class="emph">If you've taken a convex optimization course and felt like you were mechanically applying techniques without really grasping what's happening beneath the surface, this article is for you.</span> If you've taught the subject and had students ask "why" questions you couldn't quite answer, this article is for you. If you use optimization in your work but suspect there's a richer understanding waiting to be unlocked, this article is for you.

# Beyond Convex Optimization

Here's something interesting: I've written extensively about mathematics beyond just convex optimization. My explorations span measure theory, topology, abstract algebra, statistics—all with the same philosophy of pursuing genuine understanding rather than surface-level knowledge.

You can find all of these mathematical writings collected here - [**My Mathematics Collection**](https://sungheeyun.github.io/math)

Why mention this? Because <span class="emph">genuine understanding of any mathematical topic requires seeing its connections to the broader mathematical landscape.</span> Convex optimization doesn't exist in isolation. It connects to functional analysis through duality theory, to differential geometry through optimization on manifolds, to probability theory through stochastic optimization, and to game theory through minimax problems. When you understand these connections, you don't just know more facts—you develop mathematical intuition that transforms how you think about problems.

# What This Forum Offers

This article represents one approach &ndash; making convex optimization accessible without sacrificing depth. But this forum exists because <span class="emph">true understanding requires dialogue, requires wrestling with ideas together, requires the sparks that fly when different perspectives collide.</span>

<!--
The article gives you foundations. The forum gives you community. Together, they offer something neither could provide alone - the opportunity to move from knowing to understanding, from mechanical application to genuine insight, from one-dimensional knowledge to multi-dimensional comprehension.
To be more precise, way more than *multi-dimensional* understanding, I mean, multi-dimensionality is understatement considering the true level of understanding!

---
-->

The article gives you foundations. The forum gives you community. Together, they offer something neither could provide alone: the opportunity to move from knowing to understanding, from mechanical application to genuine insight, from one-dimensional knowledge to multi-dimensional comprehension. Actually, "multi-dimensional" itself is an understatement—true understanding isn't just about having more dimensions, but about grasping how those dimensions intertwine and illuminate each other, how each new perspective reveals connections that were invisible from other vantage points, how the whole forms not a collection of separate insights but an interconnected manifold where moving in any direction deepens everything else you know.

I invite you to read the article, to question it, to bring your confusions and insights to our discussions. Let's explore these beautiful ideas together—not to master them (as if anyone could claim complete mastery), but to genuinely understand them in ways that enrich our thinking, our work, and our appreciation for the mathematical structures that shape our world.

# Join the Conversation

Read the full article - [**When Every Path Leads to Success – The Convex Optimization**](https://sungheeyun.github.io/math/cvxopt)

Then come back here to discuss, to question, to share what resonated with you and what still seems opaque. That's what this forum is for—the ongoing pursuit of understanding through dialogue and shared exploration.

Welcome to [Convex Optimization Forum](/). Welcome to genuine understanding.

[Sunghee
<br>
<br>
Co-Founder & CTO / CEO, Erudio Bio, Inc / Erudio Bio Korea, Inc.
<br>
PhD, Electrical Engineering, Stanford University
<br>
Mathematician, Thinker & Seeker of Universal Truth
<br>
Entrepreneur, Engineer, Scientist, Creator & Connector of Ideas (and, most of all) PEOPLE](https://sungheeyun.github.io)

---

*Mathematical Genealogy: [Carl Friedrich Gauss](https://en.wikipedia.org/wiki/Carl_Friedrich_Gauss){:target="_blank"} → ... → [C. Felix Klein](https://en.wikipedia.org/wiki/Felix_Klein){:target="_blank"} → ... → [Stephen Boyd](https://web.stanford.edu/~boyd){:target="_blank"} → [Sunghee Yun](https://sungheeyun.github.io)*

---
title: "The Mathematical Rigor We Crave - A Deep Dive into Convex Optimization"
date: Thu Dec 25 20:12:59 PST 2025
last_modified_at: Thu Dec 25 20:46:07 PST 2025
permalink: /first-thoughts/2
categories:
 - blog
 - convex optimization
 - mathematics
tags:
 - convex optimization
 - rigorous mathematics
 - duality
 - proofs
 - theory
toc: true
toc_label: "&nbsp;Table of Contents"
toc_icon: "fa-solid fa-book"
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

> <span class="emph">There's a certain aesthetic pleasure in rigorous mathematics that people outside the field rarely understand. It's not about being pedantic or showing off technical prowess. It's about something deeper - when you state definitions with precision, when you build proofs step by careful step, when you trace exactly what assumptions are required for what conclusions—you develop an intimate familiarity with the mathematical landscape that no amount of intuitive hand-waving can provide.</span>

> <span class="emph">The Jensen's inequality appears not as a isolated result but as a natural consequence of the definition. Subdifferentials emerge not as technical machinery but as the geometric objects that must exist when you think carefully about what it means for a function to be convex.</span>

> <span class="emph">And then we get to duality theory—the crown jewel of convex optimization, where geometry, analysis, and elegant abstraction combine to produce results that feel almost magical yet are rigorously provable.</span>

> <span class="emph">We're building something rare - a community that values both accessible intuition and rigorous proof, that understands that true mastery requires both perspectives, that these two approaches to mathematics aren't in tension but in beautiful complementarity.</span>
{% assign prev_post = site.posts | where: "permalink", "/first-thoughts/1" | first %}

# For Those Who Want the Full Mathematical Treatment

In [my previous post]({{ prev_post.url }}), I shared an accessible introduction to convex optimization.
But let me be very honest about this &ndash; <span class="emph">while accessibility is valuable, what truly excites me is mathematical rigor—the pristine beauty of carefully constructed definitions, elegantly stated theorems, and proofs that illuminate rather than merely verify.</span>

This is what I love. This is where I live. And I've written something for those of you who share this passion.

You can find the complete rigorous treatment here: [**Convex Optimization - Rigorous Mathematical Foundations**](https://sungheeyun.github.io/math/rig/convex-optimization)

# Why Rigor Matters

There's a certain aesthetic pleasure in rigorous mathematics that people outside the field rarely understand. It's not about being pedantic or showing off technical prowess. It's about something deeper - <span class="emph">when you state definitions with precision, when you build proofs step by careful step, when you trace exactly what assumptions are required for what conclusions—you develop an intimate familiarity with the mathematical landscape that no amount of intuitive hand-waving can provide.</span>

Consider Slater's condition. Informally (and roughly speaking), it says "if there's a point that strictly satisfies all inequality constraints, then strong duality holds." Fine. You can work with that intuition for years, applying it successfully to countless problems. But have you *really* understood it?

Now state it rigorously:

> For a convex optimization problem with differentiable objective and constraint functions, if there exists $x \in \text{relint}(\mathcal{D})$ such that $f_i(x) < 0$ for nonlinear inequality constraints and $f_i(x) \leq 0$ for linear inequality constraints for all $i = 1, \ldots, m$ and $h_j(x) = 0$ for all $j = 1, \ldots, p$, then strong duality holds.

Already, questions emerge: Why relative interior? Why strict inequality for nonlinear $f_i$ but equality allowed for linear $f_j$?
<!--
What happens if $\mathcal{D}$ has empty interior?
-->
These aren't pedantic concerns—they're windows into the deep structure of duality theory.

## The Architecture of the Document

The rigorous treatment I've written is structured to build understanding systematically.

### Foundations - Convex Sets

We start with the geometry—careful definitions of convex sets, convex hulls, convex cones. I prove basic properties rigorously - that the intersection of convex sets is convex, that images and preimages under affine transformations preserve convexity, that separating hyperplanes exist under precisely stated conditions.

<span class="emph">This isn't just preliminary material to get through quickly. The geometry of convex sets is where all the magic happens.</span> When you understand why a hyperplane can separate disjoint convex sets, you understand why duality works. When you grasp the structure of convex cones, you understand generalized inequalities. The foundations aren't just supporting the building—they *are* the building.

### Convex Functions - Where Analysis Meets Geometry

Then we move to convex functions, where the analysis truly begins. Here I prove carefully that convexity of a function is equivalent to convexity of its epigraph. I establish first-order and second-order characterizations, showing exactly when differentiability allows us to check convexity through gradients or Hessians.

The Jensen's inequality appears not as a isolated result but as a natural consequence of the definition. Subdifferentials emerge not as technical machinery but as the geometric objects that must exist when you think carefully about what it means for a function to be convex.

### Optimization Problems - Structure Revealed

With foundations established, we can state optimization problems precisely. Standard form, inequality constraints, equality constraints, implicit constraints through domain restrictions—each gets rigorous treatment. KKT conditions emerge from careful analysis of what it means to be optimal, with exact statements of when they're necessary, when they're sufficient, and why convexity makes them both.

### Duality - The Heart of the Matter

<span class="emph">And then we get to duality theory—the crown jewel of convex optimization, where geometry, analysis, and elegant abstraction combine to produce results that feel almost magical yet are rigorously provable.</span>

I construct the Lagrangian not as a trick someone invented but as the natural object that captures the trade-off between objective and constraints. The dual function emerges from pointwise minimization, and I prove rigorously that it's concave regardless of the original problem's structure.

Weak duality follows almost immediately from the construction—it has to be true by the very definition of the dual function. But strong duality? That requires work. That requires constraint qualifications. That requires Slater's condition or its variants, stated and proved with full rigor.

I don't just prove that Slater's condition implies strong duality. I prove *why*—showing how the strict feasibility creates the geometric separation we need, how this separation translates into the existence of dual optimal points, how the whole elegant structure clicks into place once you have the right perspective.

## Barrier Methods and Interior-Point Methods

The document continues into algorithmic territory, but never abandons rigor. I develop barrier methods carefully, proving convergence under precisely stated assumptions. Central path analysis gets full treatment—not just "here's an algorithm that works" but "here's why it must converge, at what rate, under what conditions."

Primal-dual interior-point methods appear as the natural extension, with rigorous analysis of Newton steps, duality gaps, and convergence criteria. <span class="emph">Every claim is proved. Every assumption is stated explicitly. Every "clearly" or "obviously" is backed by actual demonstration.</span>

# My Favorite Part

If I'm honest, my favorite sections are the proofs of the various duality theorems and the analysis of constraint qualifications. There's something deeply satisfying about showing exactly what conditions are necessary and sufficient for strong duality to hold. Not just "Slater's condition works" but understanding the landscape of all possible constraint qualifications, seeing how they relate to each other, understanding which is strongest and which is most useful in practice.

This is mathematics as I love it: rigorous, elegant, and illuminating.

# The Broader Mathematical Context

As with the accessible introduction, this rigorous treatment doesn't exist in isolation. I've written similar rigorous treatments of other mathematical topics—measure theory, abstract algebra, topological spaces, and more. All are collected at: [**My Mathematics Collection**](https://sungheeyun.github.io/math)

Why build this collection? Because <span class="emph">mathematics is a unified whole, not a collection of disconnected techniques.</span> The duality you see in convex optimization echoes the duality in functional analysis, in category theory, in algebraic topology. The measure-theoretic foundations that underpin probability theory connect to optimization through stochastic methods. The topological concepts of compactness and continuity appear in convergence analysis of algorithms.

When you've worked through rigorous treatments of multiple mathematical areas, you start seeing these connections. You develop a mathematical maturity that transcends any single topic. You can read new mathematics more quickly because you recognize familiar patterns in unfamiliar clothing.

# NotebookLM Podcasts - A Modern Twist

One interesting experiment I've been running - I've fed my rigorous mathematical writings into [NotebookLM](https://notebooklm.google.com/){:target="_blank"} to generate podcast-style discussions. The AI attempts to explain the mathematics conversationally, sometimes succeeding, sometimes hilariously failing, but always offering an alternative perspective on the material.

You'll find links to these podcasts at the top of the rigorous treatment. They're no substitute for working through the mathematics yourself, but they offer a different way of engaging with the material—hearing it explained, questioned, discussed, rather than just reading proofs on a page.

# What This Forum Offers

This rigorous document represents years of work, distilling my understanding of convex optimization into precise mathematical language. But a document, however complete, is static. <span class="emph">This forum exists because genuine understanding requires dynamic engagement—questioning proofs, finding alternative approaches, discovering connections we hadn't seen before.</span>

In my academic journey and professional work, my deepest insights have often come from being challenged, from having to explain why a proof works to someone who's skeptical, from finding gaps in my understanding when I tried to teach material I thought I knew cold.

That's what I hope this forum becomes: a place where we can challenge each other rigorously, where "I don't understand this proof" is celebrated rather than hidden, where finding a gap in someone's reasoning (including mine!) is a contribution rather than an attack.

# An Invitation to Fellow Rigorists

If you're the kind of person who gets excited about precise epsilon-delta arguments, who appreciates the elegance of a well-constructed proof, who believes that mathematical rigor isn't pedantry but clarity—this document and this forum are for you.

Read the rigorous treatment: [**Convex Optimization - Rigorous Mathematical Foundations**](https://sungheeyun.github.io/math/rig/convex-optimization)

Work through the proofs. Find the gaps (there may be some—I'm human). Question the assumptions. Discover alternative approaches. Then bring your findings here to share and discuss.

<span class="emph">We're building something rare - a community that values both accessible intuition (see [my previous post]({{ prev_post.url }})) and rigorous proof, that understands that true mastery requires both perspectives, that these two approaches to mathematics aren't in tension but in beautiful complementarity.</span>

Let's explore these ideas together—with all the rigor they deserve and all the wonder they inspire.

Welcome to the pursuit of rigorous understanding.

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

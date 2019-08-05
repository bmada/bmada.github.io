---
layout: glossary
title: compact
category: Topology
---

Let $$ (X, \mathcal{T}_X) $$ be a [topological space].

<div class="item" markdown="1">
## Definition
A subset $$ Y \subseteq X $$ is **compact** if for any [open cover] $$ \{ U_\alpha \}_{\alpha \in A} $$ of $$ Y $$, there exists a finite subcover. That is, given any family of open sets $$ \mathcal{C} = \{ U_\alpha \}_{\alpha \in A} $$, where $$ U_\alpha \subseteq \mathcal{T}_X $$ for all $$ \alpha \in A $$, that satisfy

$$ Y \subseteq \bigcup_{\alpha \in A} U_\alpha, $$

there exists a finite subfamily $$ \mathcal{C}' = \{ U_\alpha \}_{\alpha \in A'} $$ where $$ A' \subseteq A $$ that satisfies

$$ Y \subseteq \bigcup_{\alpha \in A'} U_{\alpha}. $$

</div>

[//]: # ## Examples

[//]: # ## Properties

[topological space]: {{ site.url }}/glossary/#/
[open cover]: {{ site.url }}/glossary/open-cover/
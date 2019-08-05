---
layout: glossary
title: module homomorphism
category: Abstract Algebra
---

Let $$ R $$ be a ring.

## Definition
An **_R_-module homomorphism** is a function $$ \renewcommand\vec{\boldsymbol} \varphi \colon M \rightarrow N $$ between [_R_-modules][module] $$ M $$ and $$ N $$ that satisfies the conditions:

1. $$ \varphi $$ preserves addition; for all $$ \vec{m}_1, \vec{m}_2 \in M$$,

   $$ \varphi(\vec{m}_1 + \vec{m}_2) = \varphi(\vec{m}_1) + \varphi(\vec{m}_2). $$

2. $$ \varphi $$ preserves scalar multiplication; for all $$ r \in R $$ and $$ \vec{m} \in M $$,

   $$ \varphi(r \vec{m}) = r \varphi(\vec{m}). $$

## Definition
The set of all _R_-module homomorphisms from $$ M $$ to $$ N $$ is denoted $$ \mathrm{Hom}_R(M, N) $$ and forms a commutative group when endowed with the addition

$$ (\varphi_1 + \varphi_2)(\vec{m}) = \varphi_1(\vec{m}) + \varphi_2(\vec{m})
 $$

for $$ \varphi_1, \varphi_2 \in \operatorname{Hom}_R(M, N) $$.

{::comment}
_Related:_ [module isomorphism]

## Examples

- The quotient map $$ \pi \colon M \longrightarrow M/N $$ is an _R_-module homomorphism.

## Properties

- The composition of $$ R $$-module homomorphism is an $$ R $$-module homomorphism

- (Universal Property) If $$ M $$ and $$ N $$ are _R_-modules and $$ M' \leq M $$ we have the bijection

   $$ \Phi \colon \operatorname{Hom}_R(M/M', N) \to \{ \varphi ∈ \operatorname{Hom}_R(M,N) : \varphi(M') = 0 \} $$

   defined by

   $$ \overline{\varphi} \mapsto \overline{\varphi} \circ \pi $$
{:/comment}

[ring]: {{ site.url }}/glossary/ring/
[commutative group]: {{ site.url }}/glossary/group/
[quotient group]: {{ site.url }}/glossary/quotient-group/
[field]: {{ site.url }}/glossary/field/
[module]: {{ site.url }}/glossary/module/
[submodule]: {{ site.url }}/glossary/module/
[quotient module]: {{ site.url }}/glossary/quotient-module/
[module isomorphism]: {{ site.url }}/glossary/module-isomorphism/
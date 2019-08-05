---
layout: glossary
title: algebra
category: Abstract Algebra
---

Let $$\renewcommand\vec{\boldsymbol}$$ℛ be a [commutative ring][ring].

## Definition
An **ℛ-algebra** consists of an [additive group][group] $$ (A, +) $$ equipped with ring and scalar multiplication maps

$$\begin{align*}
A \times A &\longrightarrow A \qquad (\vec{a}, \vec{b}) \longmapsto \vec{a} \vec{b},\\
ℛ \times A &\longrightarrow A \qquad (r, \vec{a}) \longmapsto r \vec{a},
\end{align*}$$

that turn $$ A $$ into both a [ring] and an [ℛ-module][module] in such a way that the multiplication maps satisfy the compatibility condition

$$ r(\vec{a} \vec{b}) = (r \vec{a}) \vec{b} = \vec{a} ( r \vec{b}) $$

for all $$ r \in ℛ $$ and $$ \vec{a}, \vec{b} \in A $$.

[group]: {{ site.url }}/glossary/group/
[ring]: {{ site.url }}/glossary/ring/
[commutative group]: {{ site.url }}/glossary/group/
[quotient group]: {{ site.url }}/glossary/quotient-group/
[field]: {{ site.url }}/glossary/field/
[module]: {{ site.url }}/glossary/module/
[submodule]: {{ site.url }}/glossary/submodule/
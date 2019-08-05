---
layout: glossary
title: ring
category: Abstract Algebra
---

## Definition
A **ring** consists of an [additive group][group] $$ (R, +) $$ equipped with a multiplication map

$$ R \times R \longrightarrow R \qquad (r, s) \longmapsto r s $$

that satisfies the following conditions:

2. Multiplication in $$ R $$ is associative; if $$ r, s, t \in R $$, then

    $$ ( r s ) t = r (s t). $$

3. $$ R $$ contains a multiplicative identity; there exists $$ 1 \in R $$ such that for all $$ r \in R $$,

    $$ 1 r = r 1 = r. $$

4. Multiplication is distributive with respect to addition; for $$ r, s, t \in R $$

    $$\begin{align*}
    r (s + t) &= r s + r t,\\
    (s + t) r &= s r + t r.
    \end{align*}$$

## Remark
Multiplicative inverses are not required.

[group]: {{ site.url }}/glossary/group/
[ring]: {{ site.url }}/glossary/ring/
[commutative group]: {{ site.url }}/glossary/group/
[quotient group]: {{ site.url }}/glossary/quotient-group/
[field]: {{ site.url }}/glossary/field/
[module]: {{ site.url }}/glossary/module/
[submodule]: {{ site.url }}/glossary/submodule/
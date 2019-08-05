---
layout: glossary
title: group representation
category: Abstract Algebra
---

Let $$\renewcommand\vec{\boldsymbol} R $$ be a [commutative ring][ring].

<div class="item" markdown="1">
## Definition
A **group representation** of a [group] $$ G $$ on the [_R_-module][module] $$ M $$ is a group homomorphism

$$ \rho \colon G \longrightarrow \operatorname{Aut}_R(M). $$

</div>

Let $$ k $$ be a [field].

<div class="item" markdown="1">
## Definition
A **linear representation** of a [group] $$ G $$ is a group representation on a $$ k $$-vector space $$ V $$. That is, a group homomorphism

$$ \rho \colon G \longrightarrow \operatorname{GL}(V) $$

If $$ V $$ is $$ n $$-dimensional, then relative to some basis $$ \mathcal{B} $$, the linear representation $$ \rho $$ has a matrix representation

$$ \rho_{\mathcal{B}} \colon G \longrightarrow \operatorname{GL}_n(k). $$

</div>

[group]: {{ site.url }}/glossary/group/
[ring]: {{ site.url }}/glossary/ring/
[commutative group]: {{ site.url }}/glossary/group/
[quotient group]: {{ site.url }}/glossary/quotient-group/
[field]: {{ site.url }}/glossary/field/
[module]: {{ site.url }}/glossary/module/
[submodule]: {{ site.url }}/glossary/submodule/
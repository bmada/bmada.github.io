---
layout: glossary
title: decomposable module
category: Abstract Algebra
---

<div class="item" markdown="1">

## Definition
A [module] $$ M $$ is **decomposable** if it can be expressed as a direct sum of two nonzero [submodules][submodule]; there exist nonzero submodules $$ N_1, N_2 \le M $$ such that

$$ M = N_1 \oplus N_2. $$

A module is **indecomposable** if it is not decomposable; it cannot be written as a direct sum of nonzero submodules.

</div>

{::comment}
<div class="item" markdown="1">

## Example
Consider the $$ k[x] $$-module $$ M = \frac{k[x]}{\langle x^3 \rangle} $$. We obtain the submodules

$$ \frac{\langle 1 \rangle}{\langle x^3 \rangle}, \frac{\langle x \rangle}{\langle x^3 \rangle}, \frac{\langle x^2 \rangle}{\langle x^3 \rangle}, \frac{\langle x^3 \rangle}{\langle x^3 \rangle}  $$

</div>
{:/comment}

[group]: {{ site.url }}/glossary/group/
[ring]: {{ site.url }}/glossary/ring/
[opposite ring]: {{ site.url }}/glossary/ring/
[commutative group]: {{ site.url }}/glossary/group/
[field]: {{ site.url }}/glossary/field/
[vector space]: {{ site.url }}/glossary/vector-space/
[module]: {{ site.url }}/glossary/module/
[submodule]: {{ site.url }}/glossary/submodule/
[simple]: {{ site.url }}/glossary/simple-module/
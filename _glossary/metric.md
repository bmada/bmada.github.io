---
layout: glossary
title: metric
category: Functional Analysis
---

## Definition
A **metric** on a nonempty set $$ X $$ is a map

$$ d \colon X \times X \longrightarrow [0, \infty) \qquad (x, y) \longmapsto d(x, y) $$

with the following properties:

0. $$ d(x, y) \geqslant 0 $$ for all $$ x, y \in X $$.
1. $$ d(x, y) = 0 $$ if and only if $$ x = y $$ for all $$ x, y \in X $$.
2. $$ d $$ is symmetric; for all $$ x, y \in X $$,

    $$ d(x, y) = d(y, x). $$

3. $$ d $$ satisfies the triangle inequality; for all $$ x, y, z \in X $$,

   $$ d(x, z) \leqslant d(x, y) + d(y, z). $$

The pair $$ (X, d) $$ of a set and a metric is a **metric space**.

{::comment}
### Related
[seminorm], [inner product]
{:/comment}

## Remark
The first condition requiring the norm to be nonnegative is superfluous since it is included in the definition of the function.

## Example (Absolute Value)
The usual **absolute value** is itself a norm on $$ \mathbb{R} $$ defined in equivalent ways

$$ \vert x \vert := \sqrt{x^2} = \max\{ -x, x \} = \begin{cases}x, & x \geqslant 0;\\-x, & x \leqslant 0\end{cases}$$

for all $$ x \in \mathbb{R} $$. The absolute value $$ \vert \wc \vert $$ is nonnegative, $$ \vert x \vert = 0 $$ if and only if $$ x = 0 $$ and if $$ \lambda \in \mathbb{R} $$, then $$ \vert \lambda x \vert = \vert \lambda \vert \vert x \vert $$. The triangle inequality follows taking square roots of

$$ (x + y)^2 = x^2 + 2xy + y^2 \leqslant x^2 + 2 \vert x \vert \vert y \vert + y^2 = (\vert x \vert + \vert y \vert)^2, $$

noting that $$ xy \leqslant \vert x \vert \vert y \vert $$ and that both sides are nonnegative.

## Proposition (Reverse Triangle Inequality)
Let $$ (V, \| \wc \|) $$ be a normed space. For all $$ \vec{v}, \vec{u} \in V $$, the reverse triangle inequality holds

$$ -\| \vec{v} - \vec{u} \| \le \| \vec{v} \| - \| \vec{u} \| \le \| \vec{v} - \vec{u} \|. $$

_Proof._ By the triangle inequality,

$$ \| \vec{v} \| - \| \vec{u} \| = \| \vec{u} + (\vec{v} - \vec{u}) \| - \| \vec{u} \| \le \| \vec{v} - \vec{u} \|. $$

Replace $$ \vec{v} $$ and $$ \vec{u} $$, and note that $$ \| \vec{v} - \vec{u} \| = \| \vec{u} - \vec{v} \| $$ to produce the opposite inequality.

{::comment}

## Example
Given a real _n_-dimensional vector $$ \vec{x} = (x_1, x_2, \ldots, x_n) \in \mathbf{R}^n $$, the **Euclidean norm** is

$$ \| \vec{x} \| = \sqrt{ { x_1 }^2 + { x_2 }^2 + \cdots + { x_n }^2 }. $$

## Example
The _p_-norm on $$ L^p(\Omega, \mathcal{A}, \mu) $$ is

$$ \| f \|_p = \Biggl( \int_{\Omega} \vert f \vert^p \, d\mu \Biggr)^{1/p}. $$

## Properties
- pythag

## Example (Modulus)
Over $$ \mathbb{C} $$, the absolute value for $$ z = a + ib $$ is

$$ | z | = \sqrt{a^2 + b^2}. $$

To prove the triangle equality, it is useful to note if $$ z = a + ib $$ then $$ \vert z \vert^2 = z \overline{z} $$, where $$ \overline{z} = a - ib $$ is the complex conjugate. It follows that $$ \vert z_1 z_2 \vert = \vert z_1 \vert \vert z_2 \vert $$ and $$ \vert \overline{z} \vert = \vert z \vert $$. Then, noting $$ \Re(z) \leqslant \vert z \vert $$,

$$\begin{align*}
\vert z_1 + z_2 \vert^2 &= (z_1 + z_2)(\overline{z_1 + z_2})\\
&= (z_1 + z_2)(\overline{z_1} + \overline{z_2})\\
&= z_1 \overline{z_1} + z_1 \overline{z_2} + z_2 \overline{z_1} + z_2 \overline{z_2}\\
&= \vert z_1 \vert^2 + 2\Re(z_1 \overline{z_2}) + \vert z_2 \vert^2\\
&\leqslant \vert z_1 \vert^2 + 2 \vert z_1 \overline{z_2} \vert + \vert z_2 \vert^2\\
&= \vert z_1 \vert^2 + 2 \vert z_1 \vert \vert \overline{z_2} \vert + \vert z_2 \vert^2\\
&= (\vert z_1 \vert + \vert z_2 \vert)^2.
\end{align*}$$

Taking square roots yields the triangle equality.

{:/comment}

[seminorm]: {{ site.url }}/glossary/seminorm/
[vector space]: {{ site.url }}/glossary/vector-space/
[inner product]: {{ site.url }}/glossary/inner-product/
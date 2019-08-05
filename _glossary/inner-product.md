---
layout: glossary
title: inner product
category: Functional Analysis
---

## Definition
An **inner product** on a [vector space] $$ \renewcommand\vec{\boldsymbol} \newcommand\wc{\mkern 2mu\cdot\mkern 2mu} V $$ over a field $$ \mathbb{F} $$, either $$ \mathbb{R} $$ or $$ \mathbb{C} $$, is a map

$$ V \times V \longrightarrow \mathbb{F}, \quad (\vec{u},\vec{v}) \longmapsto \langle \vec{u}, \vec{v} \rangle $$

  with the following properties:

1. $$ \langle \vec{v}, \vec{v} \rangle \ge 0 $$ for all $$ \vec{v} \in V $$.
2. $$ \langle \vec{v}, \vec{v} \rangle = 0$$ if and only if $$ \vec{v} $$ is the zero vector $$ \vec{0} $$.
3. $$ \langle \wc , \wc \rangle $$ is conjugate symmetric; for all $$ \vec{u}, \vec{v} \in V $$,

   $$ \langle \vec{u}, \vec{v} \rangle = \overline{\langle \vec{v}, \vec{u} \rangle}. $$

4. $$ \langle \wc , \wc \rangle $$ is linear in the first argument; for all scalars $$ \lambda \in \mathbb{F} $$ and $$ \vec{u}, \vec{v}, \vec{w} \in V $$

 $$\begin{align*}
 \langle \lambda \vec{u}, \vec{v} \rangle &= \lambda \langle \vec{u}, \vec{v} \rangle,\\
 \langle \vec{u} + \vec{v}, \vec{w} \rangle &= \langle \vec{u} , \vec{w} \rangle + \langle \vec{v} , \vec{w} \rangle.
 \end{align*}$$

The pair $$ (V, \langle \wc, \wc \rangle) $$ of a vector space with an inner product is an **inner product space**.

## Remark

If $$ \mathbb{F} = \mathbb{R} $$, then we may drop conjugation, that is, $$ \langle \vec{u}, \vec{v} \rangle = \langle \vec{v}, \vec{u} \rangle $$ for all $$ \vec{u}, \vec{v} \in V $$. Conjugation is required in the complex case, otherwise the definition is not well-defined since for any $$ \vec{v} \in V $$,

$$ \langle i\vec{v}, i\vec{v} \rangle = i^2 \langle \vec{v}, \vec{v} \rangle = -\langle \vec{v}, \vec{v} \rangle \le 0, $$

contradicting the first property.

## Example (Dot Product)
Consider the real vector space $$ \mathbb{R}^n $$. Given vectors $$ \vec{x} = (x_1, x_2, \ldots x_n) $$ and $$ \vec{y} = (y_1, y_2, \ldots, y_n) $$ in $$ \mathbb{R}^n $$, the **dot product** is

$$ \vec{x} \cdot \vec{y} := x_1y_1 + x_2y_2 + \cdots + x_ny_n = \sum_{k=1}^n x_ky_k. $$

The dot product is an inner product on $$ \mathbb{R}^n $$. If $$ \vec{x} \in \mathbb{R}^n $$, then

$$ \vec{x} \cdot \vec{x} = {(x_1)}^2 + {(x_2)}^2 + \cdots + {(x_n)}^2 \ge 0, $$

with equality if and only if $$ \vec{x} = \vec{0} $$. We have $$ \vec{x} \cdot \vec{y} = \vec{y} \cdot \vec{x}$$ for any $$ \vec{x}, \vec{y} \in \mathbb{R}^n $$ by the commutativity of multiplication in $$ \mathbb{R} $$. Associativity and distributivity of multiplication give linearity in the first argument.

$$ (\lambda \vec{x}) \cdot \vec{y} = \lambda x_1y_1 + \lambda x_2y_2 + \cdots + \lambda x_ny_n = \lambda (\vec{x} \cdot \vec{y}) $$

$$ \begin{align*}
(\vec{x} + \vec{y}) \cdot \vec{z} &= (x_1 + y_1)z_1 + (x_2 + y_2)z_2 + \cdots + (x_n + y_n)z_n\\
&= x_1z_1 + y_1z_1 + x_2z_2 + y_2z_2 + \cdots + x_nz_n + y_nz_n = \vec{x} \cdot \vec{z} + \vec{y} \cdot \vec{z}.
\end{align*} $$

More generally, on the complex vector space $$ \mathbb{C}^n $$, the dot product is

$$ \vec{x} \cdot \vec{y} = x_1\overline{y_1} + x_2\overline{y_2} + \cdots + x_n\overline{y_n} = \sum_{k=1}^n x_k\overline{y_k} $$

for vectors $$ \vec{x}, \vec{y} \in \mathbb{C}^n $$.

{::comment}
## Property (Polarisation Identity)
{:/comment}

[vector space]: {{ site.url }}/glossary/vector-space/
[inner product]: {{ site.url }}/glossary/inner-product/
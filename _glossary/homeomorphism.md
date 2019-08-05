---
layout: glossary
title: homeomorphism
category: Topology
---

## Definition
Let $$ (X, \mathcal{T}_X) $$ and $$ (X, \mathcal{T}_Y) $$ be topological spaces. A **homeomorphism** is a bijective function $$ f \colon X \to Y $$ such that $$ f $$ and its inverse $$ f^{-1} $$ are continuous.

## Definition
Topological spaces $$ (X, \mathcal{T}_X) $$ and $$ (X, \mathcal{T}_Y) $$ are **homeomorphic** if a homeomorphism exists between them.

## Example
Consider the open intervals $$ (0, 1) $$ and $$ (a, b) $$ for any $$ a < b $$ endowed with the standard topology. These spaces are homeomorphic by the homeomorphism $$ f \colon (0, 1) \to (a, b) $$ where

$$ f(x) = a + (b - a)x $$

and

$$ f^{-1}(x) = \frac{x - a}{b - a}. $$

In fact, any collection of open intervals are homeomorphic due to transitivity.

## Example
The spaces $$ (-1, 1) $$ and $$ \mathbf{R} $$ equipped with the standard topology are homeomorphic using the homeomorphism $$ f \colon (-1, 1) \to \mathbf{R} $$ defined by

$$ f(x) = \tanh(x/2) = \frac{e^x - 1}{e^x + 1}. $$

and

$$ f^{-1}(x) = 2\tanh^{-1}(x) = \log\biggl( - \frac{x + 1}{x - 1} \biggr). $$

Any suitably scaled sigmoid function will work in this instance.

{::comment}

- The open unit disc $$ \{ (x, y) \in \mathbf{R}^2 : x^2 + y^2 < 1 \} $$ is homeomorphic to $$ \mathbf{R}^2 $$

    $$ f(x, y) = \frac{1}{1 - (x^2 + y^2)}(x, y) $$

    When viewed in terms of complex numbers, this becomes

    $$ f(z) = \frac{z}{1 - |z|}. $$


## Properties

- A homeomorphism $$ f \colon X \to Y $$ maps topologies $$ \mathcal{T}_X $$ and $$ \mathcal{T}_Y $$ bijectively. Indeed,

    - $$ U \in \mathcal{T}_X $$ if and only if $$ f(U) \in \mathcal{T}_Y $$.
    - $$ f^{-1}(V) \in \mathcal{T}_X $$ if and only if $$ V \in \mathcal{T}_Y $$.

- Convergence is the same??

- The relation

$$ (X, \mathcal{T}_X) \cong (Y, \mathcal{T}_Y) $$

is an equivalence relation.

X is homeomorphic to itself, use the identity map

If X ~ Y then Y ~ X, use the inverse

If X ~ Y, Y ~ Z, then X ~ Z. Compose the functions

Homeomorphisms

 is an equivalence relation on any family of topological spaces. In particular, if (X,τX) is homeomorphic to (Y,τY ), and (Y,τY ) is homeomorphic to (Z,τZ) then (X,τX) is homeomorphic to (Z,τZ).

{:/comment}
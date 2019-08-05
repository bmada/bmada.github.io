---
layout: glossary
title: measurable function
category: Measure Theory
---

Suppose $$ (X, \mathcal{A}) $$ and $$ (Y, \mathcal{B}) $$ are [measurable spaces].

## Definition
A function $$f \colon X \to Y$$ is **$$(\mathcal{A}, \mathcal{B})$$-measurable** if for every $$B \in \mathcal{B}$$, the inverse image

$$ f^{-1}(B) = \{ x \in X : f(x) \in B \}$$

is an $$\mathcal{A}$$-measurable set. That is,  $$ f^{-1}(B) \in \mathcal{A} $$ for all $$B \in \mathcal{B}$$.

If $$ (X, \mathcal{A}) $$ is a measurable space and $$f \colon X \to \mathbf{R}$$ is a real-valued function, then $$ f $$ is **$$\mathcal{A}$$-measurable** if it is $$(\mathcal{A}, { \mathcal{B}_\mathbf{R} } )$$-measurable, where $$\mathcal{B}_\mathbf{R}$$ is the Borel σ-algebra on $$ \mathbf{R} $$. An equivalent condition, $$f$$ is $$\mathcal{A}$$-measurable if for all $$a \in \mathbf{R}$$, the inverse image

$$ f^{-1}\bigl((-\infty, a)\bigr) = \{ x \in X : f(x) < a \} \in \mathcal{A}.$$

## Remark
A function $$ f \colon \mathbf{R} \to \mathbf{R} $$ is **Borel measurable** if it is $$( { \mathcal{B}_\mathbf{R} } , { \mathcal{B}_\mathbf{R} } )$$-measurable and **Lebesgue measurable** if it is $$(\mathcal{L}, { \mathcal{B}_\mathbf{R} } )$$-measurable.

## Example
Let $$ (X, \mathcal{A}) $$ be any measurable space and suppose $$f \colon X \to \mathbf{R}$$ is defined by $$f(x) = 0$$ for all $$x \in X$$. Then

$$ f^{-1}\bigl((-\infty, a)\bigr) = \{ x \in X : f(x) = 0 < a \} = \begin{cases}\emptyset, &a < 0;\\X, &a \ge 0.\end{cases}$$

In both cases, the inverse image is a measurable set since $$\emptyset \in \mathcal{A}$$ and $$X \in \mathcal{A}$$. Therefore, the function $$f$$ is $$\mathcal{A}$$-measurable. <br/>

In fact, constant functions are always measurable functions, regardless of the σ-algebras. Given measurable spaces $$ (X, \mathcal{A}) $$ and $$ (Y, \mathcal{B}) $$, suppose that $$f \colon X \to Y$$ is defined by $$f(x) = c$$ for all $$x \in X$$, where $$c \in Y$$ is a constant. Let $$ B \in \mathcal{B} $$, then

$$ f^{-1}(B) = \{ x \in X : f(x) = c \in B \} = \begin{cases}\emptyset, &c \notin B;\\X, &c \in B.\end{cases}$$

As $$\emptyset \in \mathcal{A}$$ and $$X \in \mathcal{A}$$, the constant function $$f$$ is $$(\mathcal{A}, \mathcal{B})$$-measurable.


{% comment %}
 - Let $$(X, \mathcal{T}_X)$$ and $$(Y, \mathcal{T}_Y)$$ be topological spaces and recall that the Borel σ-algebras on $$X$$ and $$Y$$ are defined as $$\mathcal{B}_X = \sigma(\mathcal{T}_X)$$ and $$\mathcal{B}_Y = \sigma(\mathcal{T}_Y)$$.

   Suppose $$ f \colon X \to Y $$ is continuous. By the definition of continuity, observe that

   $$ \mathcal{A} = \{ E \subseteq Y : f^{-1}(E) \in { \mathcal{B}_X } \} $$
   
   is a σ-algebra that contains $$ \mathcal{T}_Y $$, so it must also contain $$\sigma(\mathcal{T}_Y)$$.
   
   Then by the definition of continuity, if $$ E \in \mathcal{T}_Y $$ then $$ f^{-1}(E) \in \mathcal{T}_X $$.





   $$ \{ E \subseteq Y : f^{-1}(E) \in \mathcal{B}_X \} $$
 

 and let $$ B \in \mathcal{B}_Y$$. Now, note that the set


 If $$ f \colon X \to Y $$ is continuous then for every $$U \in \mathcal{T}_Y$$, the inverse image $$f^{-1}(U) \in \mathcal{T}_X$$.
 
 
 
 As the Borel σ-algebras are defined as $$\mathcal{B}_X = \sigma(\mathcal{T}_X)$$ and $$\mathcal{B}_Y = \sigma(\mathcal{T}_Y)$$, every continuous function $$ f \colon X \to Y $$ is $$ (\mathcal{B}_X, \mathcal{B}_Y) $$-measurable.


  - Every function in a power set sigma algebra is measurable?{% endcomment %}

[measurable spaces]: {{ site.url }}/glossary/σ-algebra/
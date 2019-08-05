---
layout: glossary
title: measure
category: Measure Theory
---

## Definition
A **measure** on a [measurable space]({{ site.url }}/glossary/σ-algebra/) $$ (\Omega, \mathcal{A}) $$ is a function $$ \mu \colon \mathcal{A} \to [0, \infty]$$[^1] satisfying:

 [^1]: Here, $$[0, \infty]  = [0,\infty) \cup \{ \infty \}$$ is part of the extended real number system. Define arthimetic with $$ \infty $$ as follows:

    - if $$ x \ne \infty $$ then $$ x \pm \infty = \pm \infty $$
    - if $$ x \in (0, \infty) $$ then $$ x \cdot (\pm \infty) = \pm \infty $$
    - if $$ x \in (-\infty, 0) $$ then $$ x \cdot (\pm \infty) = \mp \infty $$
    - \$$ \infty + \infty = \infty $$
    - \$$ -\infty - \infty = -\infty $$

    Leave $$ \infty - \infty $$ and $$ \infty / \infty $$ undefined. If needed, define $$ 0 \cdot \infty = 0 $$.

 1. The empty set has zero measure; $$ \mu(\emptyset) = 0 $$.
 2. $$ \mu $$ is countably additive; if $$ A_1, A_2, A_3, \ldots \in \mathcal{A} $$ is a countable collection of disjoint subsets, then
    $$\mu\bigl( A_1 \cup A_2 \cup A_3 \cup \cdots \bigr) = \mu(A_1) + \mu(A_2) + \mu(A_3) + \cdots.$$

The triple $$ (\Omega, \mathcal{A}, \mu) $$ is a **measure space** and the elements of $$ \mathcal{A} $$ are **measurable sets** or **$$ \mathcal{A} $$-measurable sets**.

## Definition
A **probability space** is a measure space $$ (\Omega, \mathcal{F}, \Pr) $$, where the measure satisfies $$ \Pr(\Omega) = 1 $$ and is called a **probability measure**.

{% comment %}*Related*: [finite measure](#), [null set](#), [probability measure](#){% endcomment %}

## Examples

- A very degenerate example of a measure on any measurable space $$ (\Omega, \mathcal{A}) $$ is **zero measure**, given by

   $$\mu(E) = 0$$

   for all $$ E \in \mathcal{A} $$. Every measurable set has zero measure.

- A natural sense of measure is **counting measure**, which counts the number of elements in a subset. For a measurable set $$ E \in \mathcal{A} $$, let

   $$\mu(E) = \begin{cases}\# E, & E \text{ finite};\\ \infty, & E \text{ infinite},\end{cases}$$

   where $$ \# E $$ denotes the cardinality of $$ E $$. Clearly $$ \mu( \emptyset) = 0$$, and given disjoint sets $$ A_1, A_2, \ldots \in \mathcal{A} $$ it is true that $$\mu(A_1 \cup A_2 \cup \cdots) =  \mu(A_1) + \mu(A_2) + \cdots$$.

- Given a point $$ x \in \Omega $$ in a measurable space $$ (\Omega, \mathcal{A}) $$, **Dirac measure** is defined by

   $$\delta_x(E) = \begin{cases}0, & x \notin E;\\ 1, & x \in E,\end{cases}$$

   for $$ E \in \mathcal{A} $$.

- Counting and Dirac measures are both examples of a more general measure. Any function $$ f \colon \Omega \to [0, \infty] $$ determines a measure defined by

   $$ \mu(E) = \sum_{x \in E} f(x) $$

   for measurable sets $$ E \in \mathcal{A} $${% comment %}[^2]{% endcomment %}.

{% comment %}    [^2]: Potential issue with uncountable sums

- Cocountable measure{% endcomment %}

## Properties

- Suppose $$ A $$ and $$ B $$ are measurable. Then $$ \mu(A) = \mu(A \setminus B) + \mu(B) $$ since the measurable sets $$ A \setminus B $$ and $$ B $$ are disjoint. If, $$ \mu(B) < \infty $$, then $$ \mu(A) - \mu(B) = \mu (A \setminus B) $$.

- Measurable sets $$ A $$ and $$ B $$ satisy an inclusion-exclusion property

  $$ \mu (A \cup B) + \mu (A \cap B) = \mu(A) + \mu(B) $$

  which follows from the disjoint unions

  $$ \begin{align*}
  A \cup B &= (A \setminus B) \cup (A \cap B) \cup (B \setminus A)\\
  A &= (A \setminus B) \cup (A \cap B)\\
  B &= (B \setminus A) \cup (A \cap B).
  \end{align*} $$

- Measures are monotonic: if $$ A \subseteq B$$ are measurable sets, then $$ \mu(A) \leqslant \mu(B) $$. Consider

  $$ \mu(B) =  \mu\bigl(A \cup (B \setminus A)\bigr) = \mu(A) + \mu(B \setminus A). $$

  Since $$ \mu(B \setminus A) \geqslant 0 $$ by definition, the result follows.

- Measure are subadditive: suppose $$A_1, A_2, A_3, \ldots $$ is a countable collection of measurable sets. Then $$\mu\bigl( A_1 \cup A_2 \cup A_3 \cup \cdots \bigr) \leqslant \mu(A_1) + \mu(A_2) + \mu(A_3) + \cdots$$.

  Let $$ B_1 = A_1 $$ and

  $$ B_k = A_k \setminus ( A_1 \cup A_2 \cup \cdots \cup A_{k-1} ). $$

  Then $$ A_k \subseteq B_k $$ for all $$ k $$ and the sets $$ B_1, B_2, \ldots, B_k $$ are disjoint with $$ \bigcup_{k=1}^n A_k = \bigcup_{k=1}^{n} B_k $$ for all $$ n $$. Therefore, by monotonicity,

  $$ \begin{align}
  \mu (A_1 \cup A_2 \cup \cdots) &= \mu( B_1 \cup B_2 \cup \cdots )\\
  &= \mu(B_1) + \mu(B_2) + \cdots \\
  &\leqslant \mu(A_1) + \mu(A_2) + \cdots.
  \end{align} $$

- If $$ A_1, A_2, A_3, \ldots $$ is an increasing sequence of measurable sets, that is, $$ A_1 \subseteq A_2 \subseteq A_3 \subseteq \cdots $$, then

  $$ \mu(A_1 \cup A_2 \cup A_3 \cup \cdots) = \lim_{n\to\infty} \mu (A_n). $$

  Let $$ A_0 = \emptyset $$. Then
  
  $$ \begin{align}
  \mu(A_1 \cup A_2 \cup A_3 \cdots) &= \mu(A_1) + \mu(A_2) + \mu(A_3) + \cdots\\
  &= \mu(A_1 \setminus A_0) + \mu(A_2 \setminus A_1) + \mu(A_3 \setminus A_2) + \cdots\\
  &= \lim_{n\to\infty} \sum_{k=1}^{n} \mu(A_k \setminus A_{k-1})\\
  &= \lim_{n\to\infty} \mu(A_n).
  \end{align} $$

- If $$ A_1, A_2, A_3, \ldots $$ is a decreasing sequence of measurable sets, that is, $$ A_1 \supseteq A_2 \supseteq A_3 \supseteq \cdots $$, and $$ \mu(A_m) < \infty $$ for at least one $$ m $$, then

  $$ \mu( A_1 \cap A_2 \cap A_3 \cap \cdots ) = \lim_{n\to\infty} \mu (A_n). $$

  Let $$ B_k = A_m \setminus A_k $$ so that $$ B_1 \subseteq B_2 \subseteq B_3 \subseteq \cdots $$. Then $$ \mu(A_m) = \mu(B_k) + \mu(A_k) $$ and

  $$ B_1 \cup B_2 \cup B_3 \cup \cdots = A_m \setminus (A_1 \cap A_2 \cap A_3 \cap \cdots). $$

  Apply continuity from below to produce

  $$ \begin{align*}
  \mu(A_m) &= \mu(A_1 \cap A_2 \cap A_3 \cap \cdots) + \mu(B_1 \cup B_2 \cup B_3 \cup \cdots)\\
  &= \mu(A_1 \cap A_2 \cap A_3 \cap \cdots) + \lim_{n\to\infty} \mu (B_n)\\
  &= \mu(A_1 \cap A_2 \cap A_3 \cap \cdots) + \lim_{n \to \infty} ( \mu(A_m) - \mu(A_n) ).
  \end{align*} $$

  Subtract $$ \mu(A_m) $$ from both sides yield the result.
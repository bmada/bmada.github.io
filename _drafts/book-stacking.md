---
layout: post
title: Stacking Books with the Harmonic Series
categories: mathematics
---

What does the sum $$ \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \cdots $$, called the harmonic series, have to do with stacking books?

![Book Stacking]({{ site.url }}/images/book-stacking.svg)

Given 2 books, the centre of mass is

$$ \frac{1 \times 1 + (1 + 1) \times 1}{2} = \frac{3}{2}$$


Suppose the centre of mass of $$ n $$ books is $$ \ell_n $$ from the rightmost point. Then adding a new book whose edge is directly below the centre of mass will create a stable structure. The new centre of mass is given by the weighted average

$$ \ell_{n+1} = \frac{\ell_n \times n + (\ell_n + 1) \times 1}{n + 1} = \ell_n + \frac{1}{n + 1} $$

![Book Stacking Induction]({{ site.url }}/images/book-stacking-induction.svg)
{: .center}


## Off to Infinity

It is well known that the harmonic series **diverges**. In other words, the sequence of partial sums

$$ \frac{1}{1}, \quad \frac{1}{1} + \frac{1}{2}, \quad \frac{1}{1} + \frac{1}{2} + \frac{1}{3}, \quad \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + \frac{1}{4}, \quad \ldots $$

can be made as large as we like so long as we take enough terms. In other words, for any positive number $$ M $$, we can find enough terms, say $$ N $$, such that

$$ \overbrace{\frac{1}{1} + \frac{1}{2} + \cdots + \frac{1}{N}}^{N \text{ terms}} > M. $$

How do we ensure we have taken enough terms to achieve a sum that exceeds $$ M $$? If we can find simple some lower bound, then we can 

$$ \frac{1}{1} + \frac{1}{2} + \cdots + \frac{1}{N} > f(N) $$

$$ \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8} + \frac{1}{9} + \cdots $$

{::options parse_block_html="true" /}
<div class="cards">
`•` `••` `••••` `••••••••` `••••••••••••••••` …
{: .center}
</div>

$$ \frac{1}{2^{k}} + \frac{1}{2^{k} + 1} + \frac{1}{2^{k} + 2} + \cdots + \frac{1}{2^k + 2^k} $$


The sum of the first

10000000000000000000000000000000000000000000
{: .center}

terms is sufficient to reach a total sum of 100.35092
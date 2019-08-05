---
layout: post
title:  "Gamma, Zeta and an Integral"
date:   2017-07-12
categories: mathematics
---

The [Gamma function][gamma], [Zeta function][zeta] and an integral satisfy a remarkable relationship: if $$ s > 1 $$, then

$$ \int_{0}^{\infty} \frac{x^{s-1}}{e^x - 1} \, dx = \Gamma(s) \zeta(s).$$

This relationship was derived by Bernhard Riemann in 1859[^1], but was also derived earlier for the particular case where $$ s $$ is even in 1823 by Niels Abel[^2]. A specific version of the integral appears when deriving the [Stefan-Boltzmann law](sigma), which states that the energy radiated from a black body is

$$ E = A \sigma T^4 $$

where $$ T $$ is temperature, $$ A $$ is area and $$ \sigma $$ is the constant[^3]

$$ \sigma = \frac{2\pi k^4}{h^3 c^2} \int_{0}^{\infty} \frac{x^3}{e^x-1} \, dx= \frac{2 \pi k^4}{15 h^3 c^2} \biggl( \frac{\pi^4}{15} \biggr) = 5.67\times10^{-8} \text{ W/m$^2$/K$^4$}. $$

However, the integral is rarely derived, perhaps because it is slightly subtle and requires nontrivial justification. The derivation below is essentially the same approach as Abel and Riemann, but with additional justification from measure theory.

 [^1]: In his groundbreaking 8 page paper _Über die Anzahl der Primzahlen unter einer gegebenen Größe_ ([_On the Number of Prime Numbers less than a Given Quantity_](http://www.claymath.org/sites/default/files/ezeta.pdf))
 [^2]: In _Oplösning af et Par Opgaver ved Hjelp af bestemt Integraler_ (_Solutions of Some Problems using Definite Integrals_) reprinted as _Solution de quelques problèmes à l'aide d'intégrales définies_, paper II in [Œuvres complètes de Niels Henrik Abel](https://archive.org/details/117742591)
 [^3]: Here, $$ k $$ is the Boltzmann constant, $$ h $$ is Planck's constant and $$ c $$ is the speed of light.

## Derivation

Let $$ s > 1 $$ and recall the integral definition of the Gamma function, $$ \Gamma(s) = \int_{0}^{\infty} t^{s-1} e^{-t} \, dt $$. Making the substitution $$ t = nx $$ produces $$ dt = n \, dx $$ and

$$ \frac{\Gamma(s)}{n^s} = \int_{0}^{\infty} x^{s-1} e^{-nx} \, dx. $$

Taking a summation over $$ n \geqslant 1 $$ yields

$$ \sum_{n=1}^{\infty} \frac{\Gamma(s)}{n^s} = \Gamma(s)\zeta(s) = \sum_{n=1}^{\infty} \int_{0}^{\infty} x^{s-1} e^{-nx} \, dx, $$

recalling that the Zeta function is defined by $$\zeta(s) = \sum_{n=1}^{\infty}1/n^s$$ for $$ s>1 $$. Exchange the summation and integral in the last expression gives

$$
\sum_{n=1}^{\infty} \int_{0}^{\infty} x^{s-1} e^{-nx} \, dx = \int_{0}^{\infty} \sum_{n=1}^{\infty} x^{s-1} e^{-nx} \, dx.
$$

The resulting infinite geometric series has a common ratio which satisfies $$ \vert e^{-x} \vert < 1 $$ since $$ x > 0 $$. Therefore, as the sum converges,

$$ \sum_{n=1}^{\infty} e^{-nx} = e^{-x} + e^{-2x} + e^{-3x} + \cdots = \frac{e^{-x}}{1 - e^{-x}} = \frac{1}{e^x - 1}. $$

This means that

$$ \int_{0}^{\infty} \frac{x^{s-1}}{e^x - 1} \, dx = \Gamma(s) \zeta(s), $$

as desired. It remains to justify the exchange of summation and integral. Interpreting the integral as a Lebesgue integral, the justification is then provided by an easy corollary of the [Lebesgue Monotone Convergence Theorem][MCT].

<blockquote class="theorem" markdown="1">
**Theorem.** Suppose $$ \{ f_n \}_{n=1}^{\infty} $$ is a sequence of nonnegataive Lebesgue integrable functions. Then

$$ \sum_{n=1}^\infty \int_{0}^{\infty} f_n(x) \, dx = \int_{0}^{\infty} \sum_{n=1}^{\infty} f_n(x) \, dx. $$

> _Proof._ Let $$ g_N = \sum_{n=1}^{N} f_n $$ be the $$N$$th partial sum, which form a monotonically increasing sequence,
>
> $$ 0 \le g_1(x) \le g_2(x) \le \cdots \quad \text{ for all } x > 0. $$
>
> Apply Monotone Convergence Theorem to the sequence $$ \{ g_N \}_{N=1}^{\infty} $$ to produce the result.
</blockquote>

## Applications

This integral has important applications the area of statistical mechanics. As described earlier, the integral

$$ \int_{0}^{\infty} \frac{\nu^3}{e^{h\nu/kT} - 1} \, d\nu  $$

appears when deriving the Stefan-Boltzmann Law from Planck's Law. Setting $$ x = h\nu/kT $$ reduces the integral to evaluating (up to a constant)

$$ \int_{0}^{\infty} \frac{x^3}{e^x - 1} \, dx = \Gamma(4)\zeta(4) = \frac{\pi^4}{15}. $$

Bose-Einstein integrals are of the form $$ \int_{0}^{\infty} \frac{t^{s-1}}{e^t/z - 1} \, dt $$ and can be expressed in terms of the [polylogarithm function][polylog],

$$ \text{Li}_s(z) = \frac{1}{\Gamma(s)} \int_{0}^{\infty} \frac{t^{s-1}}{e^t/z - 1} \, dt, $$

where the polylogarithm is defined as $$ \text{Li}_s(z) = \sum_{k=1}^{\infty} z^k/k^s $$. Setting $$ z = 1 $$ recovers the Zeta function $$  \zeta(s) = \text{Li}_s(1) $$ and the original integral. In particular, when studying ideal Bose gases, the following relations are used

$$ \int_{0}^{\infty} \frac{x^{1/2}}{e^x - 1} \, dx = \frac{\sqrt{\pi}}{2}\zeta(3/2), $$

$$\int_{0}^{\infty} \frac{x^{3/2}}{e^{x} - 1} \, dx = \frac{3\sqrt{\pi}}{4} \zeta(5/2). $$

both of which are specific examples of the integral.


[gamma]: https://en.wikipedia.org/wiki/Gamma_function
[zeta]: https://en.wikipedia.org/wiki/Riemann_zeta_function
[polylog]: https://en.wikipedia.org/wiki/Polylogarithm
[MCT]: https://en.wikipedia.org/wiki/Monotone_convergence_theorem#Lebesgue.27s_monotone_convergence_theorem
[sigma]: https://en.wikipedia.org/wiki/Stefan–Boltzmann_constant
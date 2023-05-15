---
category: Complex Analysis
---

# Exponents & Logarithms

And their counterparts in the complex numbers.

## Recap of Factorials

Before we start, we'll need to know what factorials are.

In essence, they multiply a number by all numbers lesser than them.

$$
\begin{align*}
3! &= 3 \cdot 2 \cdot 1                         &= 6 \\
4! &= 4 \cdot 3 \cdot 2 \cdot 1                 &= 24  \\
5! &= 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1         &= 120 \\
6! &= 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 &= 720 \\
\end{align*}
$$

Also, $0!$ is defined to be $1$.

The first few factorials are $1, 2, 6, 24, 120, 720$, and so on.

## Recap of Exponents

Exponents are simple notation for repeated multiplication.

$$
\begin{align*}
4^x &=\underbrace{4 \cdot 4 \cdot 4 \cdot 4 \cdot 4 \cdot ...}_{x \text{ times}} \\
4^{\textcolor{blue}{3}} &=\underbrace{4 \cdot 4 \cdot 4}_{\textcolor{blue}{3} \text{ times}} &= 64 \\
4^{\textcolor{blue}{5}} &=\underbrace{4 \cdot 4 \cdot 4 \cdot 4 \cdot 4}_{\textcolor{blue}{5} \text{ times}} &= 1024
\end{align*}
$$

## Recap of Logarithms

Sometimes, we need to find an exponent when we have the base and result.

$$
\textcolor{blue}{4}^{\textcolor{red}{x}} = \textcolor{green}{64}
$$

This is where logarithms come in. The above problem can be rewritten as

$$
\textcolor{red}{x} = \log_{\textcolor{blue}{4}}(\textcolor{green}{64}).
$$

This can now easily be solved to find that

$$
\textcolor{red}{x} = 3.
$$

## Properties of Exponents & Logarithms

Because logarithms and exponents are so closely related, they have two very
similar properties.

$$
\begin{align*}
\textcolor{red}{x}^{\textcolor{green}{a}} \textcolor{red}{x}^{\textcolor{blue}{b}} &=
  \textcolor{red}{x}^{{\textcolor{green}{a}} + {\textcolor{blue}{b}}} \\ \\

\log_{\textcolor{red}{x}}{\textcolor{green}{a} \textcolor{blue}{b}} &=
  \log_{\textcolor{red}{x}}{\textcolor{green}{a}} + \log_{\textcolor{red}{x}}{\textcolor{blue}{b}}
\end{align*}
$$

That is, a multiplication of powers is an addition of exponents, and  
a multiplication of logarithm arguments is an addition of logarithms.

These properties are very important in complex analysis.

## Euler's Number: $e$

Euler's number $e$ is **_very_** important in mathematics, on a level similar to
$\pi$ and $i$.

We'll explore why later, but for now we should understand what it is.

Imagine you're at a bank that gives you **100%** interest **each** year. If you
deposit $1000, you'll end up with **$2000** at the end of the year. Not bad.

You ask the bank owner to instead compound your money in **50%** increments
**twice a year**. You now end up with **$2250** instead of $2000.

If you compounded infinitely often, with an infinitely small interest rate,
you'd end up with $1000 \cdot e$ dollars.

| Compoundings     | Total Money                                             |
| ---------------- | ------------------------------------------------------- |
| once a year      | $2000                                                   |
| twice a year     | $1000\cdot1.5^2$ = $2250                                |
| $4$ times a year | $1000\cdot1.25^4$ = $2441.41                            |
| once a month     | $1000\cdot(1+\frac{1}{12})^{12}$ <br> = $2613.04        |
| once a day       | $1000\cdot(1+\frac{1}{365})^{365}$ <br> = $2714.57      |
| infinitely often | $1000\cdot(1+\frac{1}{\infty})^{\infty}$ <br> = $1000e$ |

## Powers of $e$

While we can raise $e$ to powers the traditional way, with repeated
multiplication, there is a second way: an infinite series.

$$
e^x = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \frac{x^4}{24} + \frac{x^5}{120} + \dotsb
$$

Why does this work? We need calculus to prove it, but let's assume it works for
now.

## Sine and Cosine

Sines and cosines, trigonometric functions, have similar infinite series.

$$
\begin{align*}
\sin x &= x - \frac{x^3}{6} + \frac{x^5}{120} - \frac{x^7}{5040} + \dotsb \\ \\
\cos x &= 1 - \frac{x^2}{2} + \frac{x^4}{24}  - \frac{x^6}{720}  + \dotsb \\ \\
e^x    &= 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \frac{x^4}{24} + \frac{x^5}{120} + \dotsb \\
\end{align*}
$$

It almost looks like $e^x$ is an addition of the sine and cosine series, but
with some signs flipped.

## $e^{ix}$

One way to mess with $+$ and $-$ signs is to introduce $i$ into an equation.
Let's try expanding $e^{ix}$.

<div class="-my-4">

$$
\begin{align*}
e^{ix} &= 1 + ix + \frac{(ix)^2}{2} + \frac{(ix)^3}{6} + \frac{(ix)^4}{24} + \frac{(ix)^5}{120} + \frac{(ix)^6}{720} + \frac{(ix)^7}{5040} + \dotsb \\ \\
&= 1 + ix + \frac{-x^2}{2} + \frac{-ix^3}{6} + \frac{x^4}{24} + \frac{ix^5}{120} + \frac{-x^6}{720} + \frac{-ix^7}{5040} + \dotsb \\ \\
&= 1 + \frac{-x^2}{2} + \frac{x^4}{24} + \frac{-x^6}{720} + ix + \frac{-ix^3}{6} + \frac{ix^5}{120} + \frac{-ix^7}{5040} + \dotsb \\ \\
&= \left(1 - \frac{x^2}{2} + \frac{x^4}{24} - \frac{x^6}{720} + \dotsb\right) + i\left(x - \frac{x^3}{6} + \frac{x^5}{120} - \frac{x^7}{5040} + \dotsb\right) \\ \\
&= \cos x + i \sin x.
\end{align*}
$$

</div>

## Exponentials as Sine and Cosine

That's pretty cool! We just figured out that in order to keep $e^x$ logically
consistent, we have to define it as this:

$$
e^{ix} = \cos x + i \sin x.
$$

But that makes anything involving powers of $e$ ridiculously easy. We can just
reduce complex exponents into multiple exponentials to evaluate them.

$$
\begin{align*}
e^{3+\frac{\pi}{2} i} &= e^3 e^{\frac{\pi}{2} i} \\
&= e^2 (\cos \frac{\pi}{2} + i \sin \frac{\pi}{2}) \\
&= e^2 (0 + i \cdot 1) \\
&= ie^2 \\
\end{align*}
$$

## $e^x$ is Periodic

One weird thing about having $\sin$ and $\cos$ in our definition of $e^{ix}$ is
that it repeats. For example, let's evaluate $e^{3+\pi i}$, $e^{3 + 3\pi i}$,
$e^{3 + 5\pi i}$, and $e^{3 - \pi i}$.

$$
\begin{align*}
e^{3-\pi i} &= e^3 (\cos -\pi + i \sin -\pi) &= e^3 (-1 + 0i) &= -e^3 \\
e^{3+\pi i} &= e^3 (\cos \pi + i \sin \pi) &= e^3 (-1 + 0i) &= -e^3 \\
e^{3+3\pi i} &= e^3 (\cos 3\pi + i \sin 3\pi) &= e^3 (-1 + 0i) &= -e^3 \\
e^{3+5\pi i} &= e^3 (\cos 5\pi + i \sin 5\pi) &= e^3 (-1 + 0i) &= -e^3 \\
\end{align*}
$$

Oh boy. This cyclic behavior whenever we add $\pm 2 \pi i$ to the exponent of
$e^x$ means that the natural logarithm, $\ln = \log_e$, is going to be _very_
weird.

## $e^{ix}$ and the Unit Circle

One of the nice features of $e^{ix}$ is that inputting different real values of
$x$ traces out the unit circle.

This is because a point on the unit circle, by definition, has the coordinates
$(\cos x, \sin x)$.

This means that putting an angle $\theta$ into $e^{i\theta}$ will output a
vector with magnitude $1$ and angle $\theta$.

Multiplying this by a distance $r$ gives $re^{i\theta}$, a vector with magnitude
$r$ and angle $\theta$.

This is called the **polar form** of a complex number.

<p class="flex overflow-hidden aspect-square h-[444px] w-[444px] translate-y-2">
  <img class="scale-[180%] translate-x-px pointer-events-none" src="/e-to-the-ix.gif" />
</p>

## Multiplying Polar Forms

Polar forms $re^{i\theta}$ are very useful, and are often more so than the
standard form $a+bi$. Why?

Let's multiply complex numbers in both forms: standard and polar.

$$
\begin{align*}
(a+bi) \cdot (c+di) &= ac - bd + i(bc + ad) \\ \\
r_1e^{i\theta_1} \cdot r_2e^{i\theta_2} &= r_1r_2e^{i(\theta_1 + \theta_2)}
\end{align*}
$$

The standard one gives us no intuition about the output.

By contrast, the polar form is very simple to read. Multiplying
$r_1e^{i\theta_1} \cdot r_2e^{i\theta_2}$ gives a new polar number. It has a
radius of $r_1r_2$ and an angle $\theta_1 + \theta_2$.

In this case, the polar form gives us a much clearer intuition for what the
result will be.

## Logarithms of Polar Forms

Computing logarithms of polar forms is very simple, since a polar form involves
a power of $e$.

There's one slight disclaimer: since we can increase or decrease $\theta$ by
$2\pi i$ and end up with the same number, we have to note that in the
logarithm's output.

$$
\begin{align*}
\ln re^{i\theta} &= \ln r + \ln e^{i\theta} \\
\tag*{where \(n \in ℤ\)}
&= \ln r + i(\theta + 2\pi n)
\end{align*}
$$

The $\text{where } n \in ℤ$ at the end means that $n$ must be an integer.

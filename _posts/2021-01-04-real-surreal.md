---
layout: post
title: Real numbers and surreal numbers
---

<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.css" integrity="sha384-yFRtMMDnQtDRO8rLpMIKrtPCD5jdktao2TV19YiZYWMDkUR5GQZR/NOVTdquEx1j" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.js" integrity="sha384-9Nhn55MVVN0/4OFx7EE5kpFBPsEMZxKTCnA+4fqDmg12eCTqGi6+BB2LjY8brQxJ" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
</head>

In my [last post](https://pranavchinmay.github.io/adding-fractions/), I described the first "expansion" of numbers most of us encounter: going from the set of integers, $$\mathbb{Z}$$ $$(...,-1,0,1,...)$$, to the set of fractions, or **rational numbers**, $$\mathbb{Q}$$. The introduction of rational numbers was motivated by the following question. What do you multiply $$5$$ by to get $$1$$? In the set $$\mathbb{Q}$$, this question has an answer: $$\frac{1}{5}$$. One might imagine, now, that this set $$\mathbb{Q}$$ contains sufficiently many numbers to handle whatever questions we may throw at it.

But it doesn't. What number, when multiplied by itself, gives $$2$$? Let us give it a symbol: $$\sqrt{2}$$. Now, is $$\sqrt{2}$$ a rational number? Does it live in $$\mathbb{Q}$$?

This is an old question, with an old [proof](https://www.math.utah.edu/~pa/math/q1.html). No. The number we have labelled $$\sqrt{2}$$ is not a rational number. We need a larger set of numbers to deal with such questions. This is the set of **real numbers**, denoted $$\mathbb{R}$$. Okay, good, but what does this look like: what properties does it have? Our reference point is $$\mathbb{Q}$$, so let's go from there. The two primary properties of the rational numbers, $$\mathbb{Q}$$, are the following: 
(i) they are **totally ordered**---given any two rationals, $$a$$ and $$b$$, at least one of the following happens: $$a \leq b$$, or $$b \leq a$$, 
(ii) they form a **field**---you can add, subtract, and multiply rational numbers, and divide by nonzero rational numbers. 

The questions, now, are the following: do these two properties extend to $$\mathbb{R}$$? Does $$\mathbb{R}$$ have any other properties?

Let's tackle (i) first. If the reals are to be totally ordered, we will need to know how big this "$$\sqrt{2}$$" is. Our intuition tells us to note that $$1.4^2 = 1.96$$, and $$1.5^2 = 2.25$$, so this thing we have called "$$\sqrt{2}$$", whose square is $$2$$, should be larger than $$1.4$$ and smaller than $$1.5$$. Next, $$1.41^2 = 1.9881$$, and $$1.42^2 = 2.0164$$, so $$\sqrt{2}$$ should be larger than $$1.41$$, and smaller than $$1.42$$. We continue this process indefinitely, and it leads us to the following familiar picture. 

<p align="center">
  <img src="https://raw.githubusercontent.com/pranavchinmay/pranavchinmay.github.io/master/images/real-line.PNG" alt=""/>
</p>

The real line. This picture is an excellent one, because it affirms clearly that the real numbers possess property (i), i.e., they are totally ordered. We will never be able to precisely locate $$\sqrt{2}$$, but we can always "zoom in" to get arbitrarily close to it. 

As for property (ii), the real numbers do form a field. Our initial, motivating question illustrates this: we can multiply $$\sqrt{2}$$ by $$\sqrt{2}$$ to get $$2$$. We can also add any two real numbers: the sum of $$2$$ and $$\sqrt{2}$$ can just be called "$$2 + \sqrt{2}$$", and placed appropriately on the number line, as you learned to do in school. 

There are lots of other real numbers that are not rational numbers: you may be familiar with $$\pi$$, or $$e$$, or (potentially), the [Euler-Mascheroni constant](https://en.wikipedia.org/wiki/Euler%E2%80%93Mascheroni_constant) $$\gamma$$. (Interestingly enough, it is yet unknown whether $$\gamma$$ is rational. It is also unknown if $$\pi + e$$ is rational, or $$\pi e$$ is rational). In fact, [most real numbers are irrational](https://en.wikipedia.org/wiki/Cantor%27s_diagonal_argument#Real_numbers), whatever that means. 

So the real numbers successfully inherit the two fundamental properties of the rational numbers. But surely they must have extra propertes that the rational numbers do not have. They do. 

(iii) the Least Upper Bound property---every nonempty set of reals that is bounded above has a Least Upper Bound.

This property is related to our initial, motivating question: what number, when multiplied by itself, gives $$2$$? Consider the set $$S$$ of all **rational numbers** whose square does not exceed $$2$$. The set $$S$$ is nonempty: it contains $$0$$, for instance. The set $$S$$ is bounded above: $$5$$ is larger than every number in $$S$$, for instance. However, the set $$S$$ has **no Least Upper Bound** in the set of rational numbers $$\mathbb{Q}$$. Any rational upper bound for $$S$$ necessarily admits a slightly smaller rational upper bound for $$S$$. So among all possible rational upper bounds for $$S$$, there is **no** smallest one. 

On the other hand, if we consider the set $$T$$ of all **real numbers** whose square does not exceed $$2$$, notice what happens. The set $$T$$ is nonempty: it contains $$0$$, for instance. The set $$T$$ is bounded above: $$5$$ is larger than every number in $$T$$, for instance. And the set $$T$$ **does** have a Least Upper Bound in the set of real numbers $$\mathbb{R}$$: the number $$\sqrt{2}$$. Surely $$\sqrt{2}$$ is an upper bound for this set, and among all possible upper bounds, it is the **smallest one**. No real number smaller than $$\sqrt{2}$$ is an upper bound for $$T$$, almost by definition. 

This third property of the real numbers $$\mathbb{R}$$ distinguishes them from the rational numbers $$\mathbb{Q}$$. Which leads us to the following canonical definition. The real numbers $$\mathbb{R}$$ are the unique totally ordered field with the least upper bound property. I say "unique" here because any other totally ordered field with the least upper bound property looks exactly like $$\mathbb{R}$$. 



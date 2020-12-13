---
layout: post
title: How do you add fractions?
---

<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.css" integrity="sha384-yFRtMMDnQtDRO8rLpMIKrtPCD5jdktao2TV19YiZYWMDkUR5GQZR/NOVTdquEx1j" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.js" integrity="sha384-9Nhn55MVVN0/4OFx7EE5kpFBPsEMZxKTCnA+4fqDmg12eCTqGi6+BB2LjY8brQxJ" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
</head>

Probably in school you learned that

$$ \frac{a}{b} + \frac{c}{d} = \frac{ad+bc}{bd}. $$

When I was an undergraduate, a professor asked me why fraction addition had this rather funny looking definition. Why not just define it this way?

$$ \frac{a}{b} + \frac{c}{d} = \frac{a+c}{b+d}. $$

Well, obviously, because it doesn't work. If I buy a pizza, give my mother half of it, and my father a quarter, well, I've given away three-fourths of the pizza, not one-sixth. What a silly question!

But an answer like this isn't something most math professors will accept. Not because it is wrong (clearly it is right), but because there's more to the story than meets the eye. Such questions are little tidbits: well-known, accessible instances of deeper phenomenon. Indeed, there are many lovely ideas related to this innocent question. Let's dive in. 

To begin, we need a good definiton of what "fraction" means. After all, if we are to be adding these objects, we should know what they are in the first place. Well, hey, of course you know what fractions are, you learned about them in middle school. Think about what motivated the introduction of fractions into your studies. You were perfectly happy with your numbers, $$1$$, $$2$$, $$3$$,... maybe even $$0$$ and $$-1$$, $$-2$$, $$-3$$,... why did they make your life difficult by introducing fractions?

The concept of fractions is motivated by a simple problem. Imagine you are seven years old again, and all the numbers you know look like the ones above (**integers**). Then someone (probably a teacher you were scared of) comes along and asks you: what number do you multiply $$5$$ by to get $$1$$? Umm... there's no such number, as far as you know. Indeed, there's no such integer. That's not very satisfying. We would like to have such a number, for any one of your favourite reasons: "it would have practical application", or "it bothers me that there's no such number", or "more numbers? Yay!" 

So we introduce such a number: $$\frac{1}{5}$$. And we say that $$\frac{5}{1} \times \frac{1}{5} = 1$$. Okay, reasonable. In the teacher's question, $$5$$ and $$1$$ were arbitrary integers, so in this manner we get a whole new family of numbers, that look like $$\frac{a}{b}$$, where both $$a$$ and $$b$$ are integers, and $$b$$ is not zero. We call these fractions. 

At the beginning, we had with us the set of all integers (denoted $$\mathbb{Z}$$), and in trying to answer the question above, we have thrown in a whole new family of numbers. Now we have with us the set of all fractions (denoted $$\mathbb{Q}$$). Observe two things. First, every integer is a fraction (in notation, we write $$\mathbb{Z} \subseteq \mathbb{Q}$$), since any integer $$n$$ can be written as $$\frac{n}{1}$$. Second, in going from $$\mathbb{Z}$$ to $$\mathbb{Q}$$, we have thrown in **multiplicative inverses** for all the non-zero integers. That is, for every non-zero integer $n$, we have a **fraction**, namely $$\frac{1}{n}$$, that has the property $$\frac{n}{1} \times \frac{1}{n} = 1$$. This is what we have done.

But is this the only way to do such a thing? Ideally, yes! It would be quite disastrous if there were hundreds of different ways to endow integers with multiplicative inverses. Then we would have to make a choice each time we wanted to use fractions, and make sure our choice doesn't mess stuff up, and keep track of all these things, ugh...

Here is the key point. We would like the following procedure to be unique: endowing integers with multiplicative inverses and performing arithmetic with these inverses. To achieve this, we have to add fractions the way you were taught in school. 

In the language of algebra, we have a **ring homomorphism** $$i: \mathbb{Z} \rightarrow \mathbb{Q}$$ that takes every non-zero integer to a fraction that possesses a multiplicative inverse. Here, $$i$$ take the **integer** $$5$$ (which has no multiplicative inverse) to the **fraction** $$5/1$$, which has a multiplicative inverse, namely $$1/5$$. 

Now, if there was another way to make fractions, we would have a ring homomorphism $$f: \mathbb{Z} \rightarrow S$$, where $$S$$ is some set, that would take every non-zero integer to an element of $$S$$ that had a multiplicative inverse in $$S$$. 

Translating this notion of "uniqueness" I have been talking about, we would like to have a ring homomorphism $$g: \mathbb{Q} \rightarrow S$$ that made the following diagram **commute**:




This post was motivated by Problem 1.3D in Ravi Vakil's The Rising Sea. 

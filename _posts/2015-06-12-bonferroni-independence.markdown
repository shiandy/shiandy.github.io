---
layout: post
title: Bonferroni Correction and Independence
categories: stats
---

*My attempt to explain why the Bonferroni correction is most appropriate when
the tests are independent, and is overly conservative when they are not.*

<!--more-->
I was talking to some people in my lab the other day about the Bonferroni
correction and why it's best to use when there is independence. It wasn't
immediately obvious why this is true. This is something that was often mentioned
in stats classes but never fully explained. 

## Bonferroni Correction Intro

The Bonferroni correction is a solution to the [*multiple hypothesis
testing*](https://xkcd.com/882/) problem. In the XKCD comic, the characters are
trying to find if jelly beans are linked to acne, but they test each color of
jelly bean separately at the 0.05 level. The problem is, if jelly beans (of any
color) truly aren't linked to acne, the probability that the characters will see
at least one significant association among n different colors is 

<div>
\[1 - (1 - 0.05)^n\]
</div>

which is much higher than 0.05. One way to correct for this is to adjust the
cutoff for the hypothesis test. The Bonferroni correction says to adjust the
original cutoff <span>\\(\alpha\\)</span> by dividing it by the number of tests
k. 


## Bonferroni Correction Proof
Let's say we have n hypotheses we want to test, and in k of them, the null
hypothesis is true. Let K denote the set of these hypotheses where the null is
true. Let's set the significance cutoff for each test at
<span>\\(\alpha/n\\)</span>. Let the p-values from test i be
<span>\\(p_i\\)</span>. Then, the probability we will make at least 1
incorrect rejection is

<div>
\[P \left(\bigcup_{i \in K} (p_i \leq \frac{\alpha}{n}) \right) \leq
\sum_{K} P(p_i \leq \frac{\alpha}{n}) \leq k \frac{\alpha}{n} \leq n
\frac{\alpha}{n} = \alpha\]
</div>

The proof relies on the union bound in the first inequality. The equality only
holds if the hypothesis tests are disjoint. 



## Independent Tests

However, the tests being disjoint does not imply that they're independent. If
the outcome of the tests were disjoint, then its possible we could turn all the
inequalities above to equalities. How does independence relate?

Recall from before that, for a cutoff of <span>\\(\alpha/n\\)</span>, the
probability of at least one incorrect rejection is bounded by
<div>
\[1 - (1 - \alpha/n)^n\]
</div>

If we take the limit as n gets large, <span>\\((1 - \alpha/n)^n\\)</span>
approaches <span>\\(e^{-\alpha}\\)</span> (recall the compound interest formula).
Using Taylor series approximation, 

<div>
\[e^{-\alpha} \approx 1 - \alpha\]
</div>

so when tests are independent, the probability of at least one rejection is
close to <span>\\(\alpha\\)</span>.


## Dependent Tests


The problem is, most sets of hypotheses are positively dependent: you're more
likely to reject one hypothesis if you have previous ones that are already
rejected.

For positively dependent hypotheses, the probability of incorrectly rejecting at
least 1 null hypothesis is actually less than 

<div>
\[1 - (1 - \alpha/n)^n\]
</div>

from before. Consider the case with two hypotheses, and let A be the event that
the first is not rejected, and B the event that the second is not rejected. The
probability that at least one is rejected is

<div>
\[1 - P(A \cap B) = 1 - P(A | B) P(B) \]
</div>

Given that B happened, event A is less likely to happen (e.g. if we don't reject
once, we are less likely to reject again because of positive correlation). If A
and B were independent, then <span>\\(P(A|B) = P(A)\\)</span>, but we have here
that <span>\\(P(A|B) < P(A)\\)</span>. Since the probability of incorrectly
rejecting at least 1 null hypothesis is decreased, we don't need to correct as
much as we thought we would, meaning the Bonferroni correction is too
conservative. 

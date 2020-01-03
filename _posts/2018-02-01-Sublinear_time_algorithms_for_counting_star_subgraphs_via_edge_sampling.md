---
categories: [research]
layout: post
title: Sublinear-time algorithms for counting star subgraphs via edge sampling
subtitle: Maryam Aliakbarpour, Amartya Shankha Biswas, Themis Gouleakis, John Peebles, Ronitt Rubinfeld, Anak Yodpinyanee
year: 2018
journal: Algorithmica
pdf: /pdf/counting_stars.pdf
tags: []
comments: true
---

We study the problem of estimating the value of sums of the form $$S_p = \sum \binom{x_i}{p}$$
when one has the ability to sample $$x_i\ge 0$$ with probability proportional to its magnitude.
When $$p=2$$, this problem is equivalent to estimating the selectivity of a self-join query in database systems when one can sample rows randomly.
We also study the special case when $$\{x_i\}$$ is the degree sequence of a graph,
which corresponds to counting the number of $$p$$-stars in a graph when one has the ability to sample edges randomly.
Our algorithm for a $$(1\pm \epsilon)$$-multiplicative approximation of
$$S_p$$ has query and time complexities $$O\left(\frac{m\log\log n}{\epsilon^2 S_p^{1/p}}\right)$$.
Here, $$m=\frac{\sum x_i}{2}$$ is the number of edges in the graph, or equivalently, half the number of records in the database table.
Similarly, $$n$$ is the number of vertices in the graph and the number of unique values in the database table.
We also provide tight lower bounds (up to polylogarithmic factors) in almost all cases, even when $$\{xi\}$$ is a degree sequence and one is allowed to use the structure of the graph to try to get a better estimate.
We are not aware of any prior lower bounds on the problem of join selectivity estimation.
For the graph problem, prior work which assumed the ability to sample only vertices uniformly gave algorithms with matching lower bounds (Gonen et al.
in SIAM J Comput 25:1365–1411, 2011).
With the ability to sample edges randomly, we show that one can achieve faster algorithms for approximating the number of star subgraphs, bypassing the lower bounds in this prior work.
For example, in the regime where $$S_p\le n$$, and $$p=2$$, our upper bound is $$\mathcal{\tilde{O}}(n/S_p^{1/2})$$, in contrast to their $$\Omega(n/S_p^{1/3})$$ lower bound when no random edge queries are available.
In addition, we consider the problem of counting the number of directed paths of length two when the graph is directed.
This problem is equivalent to estimating the selectivity of a join query between two distinct tables.
We prove that the general version of this problem cannot be solved in sublinear time.
However, when the ratio between in-degree and out-degree is bounded—or equivalently, when the ratio between the number of occurrences of values in the two columns being joined is bounded—we give a sublinear time algorithm via a reduction to the undirected case.

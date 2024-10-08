---
layout: post
title: Massively Parallel Algorithms for Small Subgraph Counting
collaborators: Amartya Shankha Biswas, Talya Eden, Quanquan C. Liu, Slobodan Mitrović, Ronitt Rubinfeld
tags: []
journal: APPROX-RANDOM
year: 2022
pdf: /research/pdf/MPC_subgraphs.pdf
comments: true
---
With the prevalence of large graphs, it is becoming increasingly important to design scalable algorithms. Over the last two decades, frameworks for parallel computation, such as MapReduce, Hadoop, Spark and Dryad, gained significant popularity.
The Massively Parallel Computation (MPC) model is a de-facto standard for studying these frameworks theoretically.
Subgraph counting is a fundamental problem in analyzing massive graphs, often studied in the context of social and complex networks. There is a rich literature on designing scalable algorithms for this problem, with the main challenge to design methods which are both efficient and accurate.
In this work, we tackle this challenge and design several new algorithms for subgraph counting in MPC.

Given a graph $$G$$ over $$n$$ vertices, $$m$$ edges and $$T$$ triangles,
our first main result is an algorithm that, with high probability,
outputs a $$(1+\epsilon)$$-approximation to $$T$$, with asymptotically **optimal round and total space complexity**
provided any $$S \geq \max{(\sqrt m, n^2/m)}$$ space per machine and assuming $$T=\Omega(\sqrt{m/n})$$.


Our second main result is an $$O(\log \log n)$$-rounds algorithm for exactly counting the number of triangles, parametrized by the **arboricity** $$\alpha$$ of the input graph. 	The space per machine is $$O(n^{\delta})$$ for any constant $$\delta$$, and the total space is $$O(m\alpha)$$, which matches the **time** complexity of (combinatorial) triangle counting in the sequential model.
	We also prove that this result can be extended to exactly counting $$k$$-cliques for any constant $$k$$, with the same round complexity and total space $$O(m\alpha^{k-2})$$. Alternatively,  allowing $$O(\alpha^2)$$ space per machine, the total space requirement reduces to $$O(n\alpha^2)$$.

Finally, we prove that a recent result of  Bera, Pashanasangi and Seshadhri (ITCS 2020) for exactly counting all subgraphs of size at most $$5$$, can be implemented in the MPC model in
$$\tilde{O}_{\delta}(\sqrt{\log n})$$ rounds, $$O(n^{\delta})$$ space per machine and $$O(m\alpha^3)$$
 total space. Therefore, this result also exhibits the phenomenon that a time bound
 in the sequential model translates to a space bound in the MPC model.

---
layout: post
title: Local Access to Random Walks
collaborators: Amartya Shankha Biswas, Edward Pyne, Ronitt Rubinfeld
tags: []
journal: Innovations in Theoretical Computer Science Conference (ITCS)
year: 2022
pdf: /research/pdf/random_walks.pdf
comments: true
---
For a graph $$G$$ on $$n$$ vertices, naively sampling the position of a random walk of at time $$t$$ requires work $$\Omega(t)$$.
We desire **local access** algorithms supporting $$position(t)$$ queries, which return the position of a random walk from some fixed start vertex $$s$$ at time $$t$$,
where the joint distribution of returned positions is $$1/\poly(n)$$ close to those of a uniformly random walk in $$\ell_1$$ distance.

We first give an algorithm for local access to random walks on a given undirected $$d$$-regular graph with $$\widetilde{O}(\frac{1}{1-\lambda}\sqrt{n})$$ runtime per query,
where $$\lambda$$ is the second-largest eigenvalue of the random walk matrix of the graph in absolute value. Since random $$d$$-regular graphs $$G(n,d)$$ are expanders with high probability,
this gives an $$\widetilde{O}(\sqrt{n})$$ algorithm for a graph drawn from $$G(n,d)$$ whp, which improves on the naive method for small numbers of queries.

We then prove that no algorithm with subconstant error given probe access to an input $$d$$-regular graph can have runtime better than $$\Omega(\sqrt{n}/\log(n))$$ per query in expectation when the input graph is drawn from $$G(n,d)$$, obtaining a nearly matching lower bound. We further show an $$\Omega(n^{1/4})$$ runtime per query lower bound even with an oblivious adversary (i.e. when the query sequence is fixed in advance).

We then show that for families of graphs with additional group theoretic structure, dramatically better results can be achieved.
We give local access to walks on small-degree abelian Cayley graphs, including cycles and hypercubes, with runtime $$\text{polylog}(n)$$ per query. This also allows for efficient local access to walks on $$polylog$$ degree expanders. We show that our techniques apply to graphs with high degree by
extending or results to graphs constructed using the tensor product (giving fast local access to walks on degree $$n^\epsilon$$ graphs for any $$\epsilon \in (0,1]$$) and Cartesian product.

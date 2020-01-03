---
categories: [research]
layout: post
title: Local Access to Huge Random Objects Through Partial Sampling
authors: Amartya Shankha Biswas, Ronitt Rubinfeld, Anak Yodpinyanee
tags: []
journal: Innovations in Theoretical Computer Science Conference (ITCS)
year: 2020
comments: true
---
Consider an algorithm performing a computation on a *huge random object* (for example a random graph or a "long" random walk).  Is it necessary to generate the entire object prior to the computation, or is it possible to provide query access to the object and sample it incrementally "on-the-fly" (as requested by the algorithm)?  Such an *implementation* should emulate the random object by answering queries in a manner consistent with an instance of the random object sampled from the true distribution (or close to it).  This paradigm is useful when the algorithm is sub-linear and thus, sampling the entire object up front would ruin its efficiency.

Our first set of results focus on undirected graphs with independent edge probabilities, i.e. each edge is chosen as an independent Bernoulli random variable.
We provide a general implementation for this model under certain assumptions.
Then, we use this to obtain the first efficient local implementations for the Erdos-Renyi $$G(n,p)$$ model for *all* values of $$p$$,
and the Stochastic Block model.
As in previous local-access implementations for random graphs, we support **Vertex-Pair** and **Next-Neighbor** queries.
In addition, we introduce a new **Random-Neighbor** query.
Next, we give the first local-access implementation for **All-Neighbors** queries in the (sparse and directed) Kleinberg's Small-World model.
Our implementations require no pre-processing time, and answer each query using $$\mathcal{O}(poly(\log n))$$ time, random bits, and additional space.

Next, we show how to implement random Catalan objects, specifically focusing on Dyck paths
(balanced random walks on the integer line that are always non-negative).
Here, we support **Height** queries to find the location of the walk,
and **First-Return** queries to find the time when the walk returns to a specified location.
This in turn can be used to implement **Next-Neighbor** queries on random rooted ordered trees,
and **Matching-Bracket** queries on random well bracketed expressions (the Dyck language).

Finally, we introduce two features to define a new model that:
(1) allows multiple independent (and even simultaneous) instantiations of the same implementation,
to be consistent with each other without the need for communication,
(2) allows us to generate a richer class of random objects that do not have a succinct description.
Specifically, we study uniformly random *valid* $$q$$-colorings of an input graph $$G$$ with maximum degree $$\Delta$$.
This is in contrast to prior work in the area, where the relevant random objects are defined as a distribution with $$\mathcal O(1)$$ parameters
(for example, $$n$$ and $$p$$ in the $$G(n,p)$$ model).
The distribution over valid colorings is instead specified via a "huge" input (the underlying graph $$G$$),
that is far too large to be read by a sub-linear time algorithm.
Instead, our implementation accesses $$G$$ through local neighborhood probes,
and is able to answer queries to the color of any given vertex in sub-linear time for $$q\ge 9\Delta$$,
in a manner that is consistent with a specific random valid coloring of $$G$$.
Furthermore, the implementation is memory-less, and can maintain consistency with non-communicating copies of itself.

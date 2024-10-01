---
layout: post
title: Massively Parallel Algorithms for Distance Approximation and Spanners
collaborators: Amartya Shankha Biswas, Michal Dory, Mohsen Ghaffari, Slobodan Mitrović, Yasamin Nazari
tags: []
journal: Symposium on Parallelism in Algorithms and Architectures (SPAA)
year: 2021
pdf: /research/pdf/MPC}_spanners.pdf
comments: true
---
Over the past decade, there has been increasing interest in distributed/parallel algorithms for processing large-scale graphs.
By now, we have quite fast algorithms---usually sublogarithmic-time and often $$\poly(\log\log n)$$-time,
or even faster---for a number of fundamental graph problems in the massively parallel computation ($$\texttt{MPC}$$) model.
This model is a widely-adopted theoretical abstraction of MapReduce style settings,
where a number of machines communicate in an all-to-all manner to process large-scale data.
Contributing to this line of work on $$\texttt{MPC}$$ graph algorithms,
we present $$poly(\log k) \in poly(\log\log n)$$ round $$\texttt{MPC}$$ algorithms for computing $$O(k^{1+{o(1)}})$$-spanners
in the strongly sublinear regime of local memory. To the best of our knowledge, these are the first sublogarithmic-time $$\texttt{MPC}$$ algorithms for spanner construction.

As primary applications of our spanners, we get  two important implications, as follows:

    * For the $$\texttt{MPC}$$ setting, we get an $$O(\log^2\log n)$$-round algorithm for $$O(\log^{1+o(1)} n)$$ approximation of all pairs shortest paths (APSP) in the near-linear regime of local memory. To the best of our knowledge, this is the first sublogarithmic-time $$\texttt{MPC}$$ algorithm for distance approximations.

    * Our result above also extends to the \clique model of distributed computing, with the same round complexity and approximation guarantee. This gives the first \emph{sub-logarithmic} algorithm for approximating APSP in \emph{weighted} graphs in the \clique model.

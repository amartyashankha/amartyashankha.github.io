---
layout: post
title: Towards a decomposition-optimal algorithm for counting and sampling arbitrary motifs in sublinear time
collaborators: Amartya Shankha Biswas, Talya Eden, Ronitt Rubinfeld
tags: []
journal: APPROX-RANDOM
year: 2021
pdf: /research/pdf/arbitrary_motifs.pdf
comments: true
---
We consider the problem of sampling and approximately counting an arbitrary given motif $$H$$ in a graph $$G$$, where access to $$G$$ is given via queries:
degree, neighbor, and pair, as well as uniform edge sample queries.
Previous algorithms for these tasks were based on a decomposition of $$H$$ into a collection of odd cycles and stars,
denoted $$D^*(H) = {O_{k_1},...,O_{k_q}, S_{p_1},...,S_{p_l}}$$.
These algorithms were shown to be optimal for the case where $$H$$ is a clique or an odd-length cycle,
but no other lower bounds were known. We present a new algorithm for sampling arbitrary motifs which,
up to $$poly(log n)$$ factors, is always at least as good, and for most graphs $$G$$ is strictly better.
The main ingredient leading to this improvement is an improved uniform algorithm for sampling stars,
which might be of independent interest, as it allows to sample vertices according to the $$p$$-th moment of the degree distribution.
Finally, we prove that this algorithm is decomposition-optimal for decompositions that contain at least one odd cycle.
These are the first lower bounds for motifs $$H$$ with a nontrivial decomposition, i.e.,
motifs that have more than a single component in their decomposition.

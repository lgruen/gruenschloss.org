---
layout: default
title: Leonhard Gruenschloss
---

# Quasi-Monte Carlo (QMC) Samplers

## [Halton](https://github.com/lgruen/halton)

A very fast C++ implementation of the Halton sequence that supports both
Faure-permutations and random digit permutations.  Together with the component (i / N)
this will yield a Hammersley point set.  Comes with a Python script to generate
optimized code for arbitrary dimensions. It also includes code to enumerate samples in a
2D domain, for example pixels.

## [MCQMC LFSR](https://github.com/lgruen/mcqmclfsr)

A C++ implementation of the small linear feedback shift registers (LFSR) for use in a
Markov chain quasi-Monte Carlo context, as described in *S. Chen, M. Matsumoto, T.
Nishimura, and A. Owen:* [New inputs and methods for Markov chain quasi-Monte
Carlo](http://www-stat.stanford.edu/~owen/reports/).

## [Sobol'](https://github.com/lgruen/sobol)

A C++ implementation of a simple and fast random-access Sobol'-sequence generator,
based on the direction numbers published in *S. Joe and F. Y. Kuo:* [Constructing Sobol sequences with better
two-dimensional projections](http://web.maths.unsw.edu.au/~fkuo/sobol/).

# Publications

## [Low-Discrepancy Quasi-Uniform Digital Sequences in Every Dimension](https://github.com/lgruen/quasi-uniform-sequences-lean)

Preprint, version 1, 2026. Companion to the paper on nets below.

Lean 4 formalization of the headline results: [Palomar entry
PALOMAR-2026-10-29-000041](https://palomar-registry.org/entry?id=PALOMAR-2026-10-29-000041&version=1).
[Code, Lean library and verification archive](https://github.com/lgruen/quasi-uniform-sequences-lean), archived at
[Zenodo](https://doi.org/10.5281/zenodo.23769767). Also see the [interactive
explainers](https://lgruen.github.io/quasi-uniform-sequences-lean/explainers/).

*Abstract:* A sequence of points in the unit cube is quasi-uniform if its first $$N$$ points are
spread like a grid for every $$N$$: minimum distance $$\delta$$ and covering radius both of the
optimal order $$N^{-1/s}$$. Dick, Goda and Suzuki asked for such sequences among the digital
sequences of quasi-Monte Carlo integration, and Goda, Hofer and Suzuki asked whether any
Halton-type sequence is quasi-uniform. In dimension two and higher no Halton-type sequence, no
Sobol' sequence, no classical Niederreiter sequence and no Faure sequence is quasi-uniform: a
carry in the last digits of one coordinate leaves the leading digits of all coordinates
unchanged, giving explicit pairs of points that are far too close. One fixed linear scramble of
a generalized Faure sequence, the same for all numbers of points, repairs this: the residue
theorem ties the coordinates together, so that a carry in one coordinate is seen by the others.
For every dimension $$s$$ and every prime base $$p>2^s$$ this gives explicit quasi-uniform
digital $$(0,s)$$-sequences, hence of low discrepancy, whose first $$N=p^{sK-1}$$ points are at
least $$(1-2p^{-1/s})N^{-1/s}$$ apart for every $$K$$; in dimensions two and three, for every prime
$$p\ge5$$, a variant keeps its first $$N$$ points at least $$(1-2/p)N^{-1/s}$$ apart whenever $$N$$
is a power of $$p^{s^2}$$. The results are formalized in Lean 4, apart from some finite
computations, which are checked by scripts. The constructions, proofs and formalization were
produced by an AI system (Anthropic Claude Opus 5.5) under my direction; see the AI-use
statement in the paper.

## [Low-Discrepancy Quasi-Uniform Digital Nets in Every Dimension](https://hexagonmath.org/abs/2610.00217v1)

Preprint, version 1, 2026: [hexagon:2610.00217v1](https://hexagonmath.org/abs/2610.00217v1).
The companion paper above treats sequences.

Lean 4 formalization of the main theorem: [Palomar entry
PALOMAR-2026-10-13-000011](https://palomar-registry.org/entry?id=PALOMAR-2026-10-13-000011&version=1).
[Code and Lean library](https://github.com/lgruen/separated-nets-lean), archived at
[Zenodo](https://doi.org/10.5281/zenodo.23327748). Also see the [Lean
blueprint](https://lgruen.github.io/separated-nets-lean/blueprint/) and the [interactive
explainers](https://lgruen.github.io/separated-nets-lean/explainers/).

*Abstract:* Dick, Goda and Suzuki asked for low-discrepancy digital nets that are
quasi-uniform, with minimum distance $$\delta$$ and covering radius both of the optimal order
$$N^{-1/s}$$, and stated the problem as open in dimension $$s\ge3$$. We construct such nets
in every dimension. For every $$s\ge3$$, every base $$q$$ whose prime factors are at least
$$s-1$$, and every $$k\ge1$$, we give explicit digital $$(0,sk,s)$$-nets over
$$\mathbb{Z}/q\mathbb{Z}$$ with $$N=q^{sk}$$ points, covering radius at most
$$\sqrt{s}\,N^{-1/s}$$, and $$\delta N^{1/s}\ge1-a^*_s/q$$ once $$q\ge5a^*_s+4$$. In prime bases these
families are well separated in the sense of Dick, Goda and Suzuki, and they stay so under
every digital shift. The results are formalized in Lean 4, apart from some finite
computations, which are checked by scripts. The constructions, proofs and formalization
were produced by AI systems (Anthropic Claude) under my direction; see the AI-use
statement in the paper.

## [SIGGRAPH 2012 course: Advanced (Quasi-) Monte Carlo Methods for Image Synthesis](https://sites.google.com/site/qmcrendering/)

with S. Premoze, A. Keller, and M. Raab.

## [Enumerating Quasi-Monte Carlo Point Sequences in Elementary Intervals](https://github.com/lgruen/sample-enum)

with M. Raab and A. Keller.

In H. Wozniakowski and L. Plaskota (eds.), Monte Carlo and Quasi-Monte Carlo Methods
2010, Springer-Verlag, Berlin, 2012.

*Abstract:* Low discrepancy sequences, which are based on
radical inversion, expose an intrinsic stratification.  New algorithms are presented to
efficiently enumerate the points of the Halton and (t,s)-sequences per stratum.  This
allows for consistent and adaptive integro-approximation as for example in image
synthesis.

## [Parallel Quasi-Monte Carlo Integration by Partitioning Low Discrepancy Sequences](https://github.com/lgruen/parqmc)

with A. Keller.

In H. Wozniakowski and L. Plaskota (eds.), Monte Carlo and Quasi-Monte Carlo Methods
2010, Springer-Verlag, Berlin, 2012.

*Abstract:* A general concept for parallelizing quasi-Monte Carlo methods
is introduced. By considering the distribution of computing jobs across a multiprocessor
as an additional problem dimension, the straightforward application of quasi-Monte Carlo
methods implies parallelization.  The approach in fact partitions a single
low-discrepancy sequence into multiple low-discrepancy sequences. This allows for
adaptive parallel processing without synchronization, i.e. communication is required
only once for the final reduction of the partial results.  Independent of the number of
processors, the resulting algorithms are deterministic,  and generalize and improve upon
previous approaches.

## [Quasi-Monte Carlo Point Progressive Photon Mapping](https://github.com/lgruen/qppm)

with A. Keller and M. Droske.

In H. Wozniakowski and L. Plaskota (eds.), Monte Carlo and Quasi-Monte Carlo Methods
2010, Springer-Verlag, Berlin, 2012.

*Abstract:* The simulation of light transport
often involves specular and transmissive surfaces, which are modeled by functions that
are not square integrable. However, in many practical cases unbiased Monte Carlo methods
are not able to handle such functions efficiently and consistent Monte Carlo methods are
applied. Based on quasi-Monte Carlo integration, a deterministic alternative to the
stochastic approaches is introduced. The new method for deterministic consistent
functional approximation uses deterministic consistent density estimation.

## [MSBVH: An Efficient Acceleration Data Structure for Ray Traced Motion Blur](https://github.com/lgruen/msbvh)

with M. Stich, S. Nawaz, and A. Keller.

In Proceedings of the Conference on High Performance Graphics (HPG '11).

*Abstract:* When a bounding volume hierarchy is used for accelerating the intersection
*of
rays and scene geometry, one common way to incorporate motion blur is to interpolate
node bounding volumes according to the time of the ray. However, such hierarchies
typically exhibit large overlap between bounding volumes, which results in an
inefficient traversal. This work builds upon the concept of spatially partitioning nodes
during tree construction in order to reduce overlap in the presence of moving objects.
The resulting hierarchies are often significantly cheaper to traverse than those
generated by classic approaches.

## [(t, m, s)-Nets and Maximized Minimum Distance, Part II](https://github.com/lgruen/diag0m2)

with A. Keller.

In P. L'Ecuyer and A. Owen (eds.), Monte Carlo and Quasi-Monte Carlo Methods 2008, Springer-Verlag,
Berlin, 2009.

*Abstract:* The quality parameter t of (t,m,s)-nets controls extensive stratification
properties of the generated sample points. However, the definition allows for points
that are arbitrarily close across strata boundaries.  We continue the investigation of
(t,m,s)-nets under the constraint of maximizing the mutual distance of the points on the
unit torus and present two new constructions along with algorithms. The first approach
is based on the fact that reordering (t,s)-sequences can result in (t,m,s+1)-nets with
varying toroidal distance, while the second algorithm generates points by permutations
instead of matrices.

## [Motion Blur](https://github.com/lgruen/motion-blur)

Diploma thesis at Ulm University, Germany, 2008.

Supervisors: A. Keller and M. Weber.

## [(t, m, s)-Nets and Maximized Minimum Distance](https://github.com/lgruen/netsearch)

with J. Hanika , R. Schwede, and A. Keller.

In A. Keller, S. Heinrich, and H. Niederreiter (eds.), Monte Carlo and Quasi-Monte Carlo
Methods 2006, Springer-Verlag, Berlin, 2008.

*Abstract:* Many experiments in computer graphics imply that the average quality of
quasi-Monte Carlo integro-approximation is improved as the minimal distance of the point
set grows. While the definition of (t,m,s)-nets in base b guarantees extensive
stratification properties, which are best for t=0, sampling points can still lie
arbitrarily close together. We remove this degree of freedom, report results of two
computer searches for (0,m,2)-nets in base 2 with maximized minimum distance, and
present an inferred construction for general m.  The findings are especially useful in
computer graphics and, unexpectedly, some (0,m,2)-nets with the best minimum distance
properties cannot be generated in the classical way using generator matrices.

## [Benchmarking Ray Tracing for Realistic Light Transport Algorithms](https://github.com/lgruen/bwfirt)

with M. Raab, J. Hanika, M. Finckh, and A. Keller.


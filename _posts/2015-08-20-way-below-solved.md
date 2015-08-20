---
layout: post
categories: math
title: Problem with way-below relation solved
description: The hard problem mentioned in last thread was solved. An elaborate counterexample is given to show the in-equivalence of two definitions.
---
 
In the previous thread (dated 17 Aug 2015) we mentioned a problem of the different definitions
of "way-below relation" which is hard to solve. This problem was solved on 19 Aug 2015 by author by explicitly 
giving a counterexample where Definition 2 does not imply Definition 1.
 
The construction of counterexample is as following: let M be the set of natural numbers (including element 0) with 
an extra member: inf, which means infinity.

Let us consider the Cartesian product set M x M = {(m, n) | m, n are in M} with the only orders generated from
(with transitivity):
 
  (a, i) <= (a, j)      , if i <= j or j = inf, and a is any natural number other than inf
  
  (i, inf) <= (j, inf)  , if i <= j or j = inf
  
  (i, 0) <= (j, 0)      , if i <= j or j = inf

The last line above being to ensure that there is a least element (bottom). It is obvious now that the set M x M forms a cpo.
 
We let x be the element (0, inf), y be the element (inf, inf).
 
Then we first show that for every directed set D, y <= sup(D) implies that there exists element d in D, x <= d:

Suppose y <= sup(D). Because y = (inf, inf), with the only orders as shown above and their transitive closures,
sup(D) must be (inf, inf), i.e. y = sup(D). Then D must either contain y or some element (i, inf). Let d = (i, inf).
Therefore x <= (i, inf) = d.
 
However, there is no open Set U with y is in U and x <= U. Therefore, y is not in the interior of {z | x <= z}.

To show this, we first realize U must take the form of {(j, inf) | j >= a}, where a is a fixed natural number; or just
U = {y}, due to the requirement of its upwards closure. In the former case, we construct D = {(a, i) | i is any natural 
number}, obviously sup(D) = (a, inf) is in U, but there is no element in both D and U. In the latter case, we construct 
D = {(i, inf) | i is any natural number}, obviously sup(D) = y is in U, but again D does not intersect U. Therefore, it 
contradicts the openness of U.

Concluding the above, this constitutes a counterexample where Definition 2 holds but Definition 1 does not hold. Hence 
the two definitions do not agree in this case. It can be shown that the two definitions are not even equivalent for Scott 
domains.

 
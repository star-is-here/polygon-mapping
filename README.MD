# Optimal polygonal mapping of disparate non-hierarchical mapped datasets

## Problem

There is an increasing number of geospatially oriented datasets being generated for academia, commercial, or federal purposes. Many of these datasets however are often aggregated up to lower polygonal mapping (i.e. zipcodes or school districts). This is often done to avoid privacy disclosure, facilitate the ease of analysis, or increase interpretability of results. Often, researchers will have disparate datasets generated from different sources and aggregated to different polygonal mappings.

Common approaches to unify multiple datasets of different polygonal mappings is to either assign or apportion the disparate polygonal mappings to a final desired polygonal mapping. These methods rely on an additional variable outside our feature set that can be calculated for every intersection of our original mappings and desired mappings. Often times this is land area or total area.

### Assignment method

Consider an original set of polygons S and desired set of polygons T that both span our mapping space. A surjective mapping f from original set of polygons S to desired set of polygons T is created by determining for each polygon in S the corresponding polygon in T that maximizes some intersection function g(s, t) for s \in S and t \n T.

### Apportion method

In apportioning, instead of creating a surjective mapping f, instead a normalized g'(s, t) intersection function is used to apportion out the independent and dependent variables in our analysis. 

Both methods assume a known intersection function that closely approximates the distribution of our variables across the mapping space. This is easily observed false in many cases or non-trivial to determine the intersection function.

## Proposal

We instead propose an agglomerative method of determining the optimal desired polygonal mapping from a disparate set of polygonal mappings. 

### Claim

Given the set U of all possible union of polygons that wholly contain elements from our set of disparate polygonal mappings {S, T, ...}, there exist an optimal polygonal mapping U_i from U wrt to a final estimate/statistic.

### Conjecture

A penalized search across set U with a regularized loss function converges on the optimal mapping asymptotically?

### Conjecture

The agglomerative search can be approximated to less than O(n^2)
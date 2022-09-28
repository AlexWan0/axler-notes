Joint notes from Berkeley Math 110 fa'22 and Axler

## Overview
- affine subset is a single shift of U given the offset (v, how much we shift)
- quotient space is the space of all shifts of U in V
- quotient map gets the affine subset (single shift) given the offset (v, how much we shift)

## Affine Subsets
- v in V
- U subspace of V
- v + U = {v + u for every u in U}
- is affine subset and "parallel" to U
	+ intuition: shifting U by offset v
	+ imagine: you're in R^2 and U is a line
- is a subspace iff v is in U
	+ imagine: you're in R^2 and U is a line
	+ if v is in U, then you're moving parallel to the line
		* i.e. not really doing anything
	+ if v is not in U, then you're actually moving the line, breaking its subspace properties
		* e.g. the line no longer goes through the origin -> 0 is not in the set

## Quotient Space
- V/U = {v + U for every v in V}
- **notice** V/U is a *set of sets*
- intuition: why is this a "quotient" space?
	+ imagine: you're in R^2 and U is a line
	+ number of unique elements in V/U would be the different ways in which you could shift the line

## Quotient Map
- pi: V -> V/U
- where pi(v) = v + U
- essentially gets a shift on U given the offset v
- is a linear map
	+ can use to show that dim(V/U) = dim(V) - dim(U) w/ funadmental theorem of linear maps

## T with tilde on top
- gonna just say T~ cuz it's easier to type :/
- T~ is from V/(null T) -> W
	+ i.e. the domain is all sets of offsets of the null space
	+ i.e. T~ maps a null space + offset to some vector in W
- defined as T~(v + null T) = Tv
	+ i.e. given offset + null space, you get just the regular mapping
- pi (quotient map) gets you from v to v + null T
- T~ gets you to W
	+ T also takes you to w in W
- whyyyyyyyyyyyyy?
	+ isomorphic to range T
	+ ehh

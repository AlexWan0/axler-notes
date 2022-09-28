Joint notes from Berkeley Math 110 fa'22 and Axler

## Terminology
- linear functionals on V == V' == dual of V
- dual of T == T'

## Linear Functionals
- e.g. output of arbitrary polynomial with input 0
- can express all linear functionals as phi(v) = a_1 v_1 + ... + a_n v_n

## Dual Space
vector space of linear functionals

## Dual Basis
- for basis v_1 ... v_m
- dual basis: phi_1 ... phi_m
	+ where phi_j(v_i) = 1 iff i == j else 0

- input/output
	+ for basis vectors intuitive
		* just zero/one

	+ for all other vectors
		* first split into linear combination of basis

		* -> phi_j just ends up equaling the coefficients of the jth basis vector
			- b/c everything else is zero!

	+ for annihilators
		* if you have an "out of range" set of dual basis where all of your basis vectors v_j for their corresponding phi_j isn't used by the subset U

		* then that phi is an annihilator

		* think: what happens if you split some u in U up into basis vectors and apply phi

## Dual Map
- T: V -> W
- phi: linear functional on W

- dual of T (T')
	+ space of linear functionals of W to space of linear functionals of V
		* W' -> V'
	+ definition:
		* input phi: phi in W'
		* output T'(phi): composite of phi and T
	+ i.e. for some arbitrary linear funcitonal of W (phi) ->
	+ we can make a linear functional of V by returning a function where you:
		* map V to W w/ T
		* W to F w/ phi
	+ i.e. given some map phi, outputs a map where you first do T then do phi

- is a linear map

## Annihilator
- U: subset of vector space V
- U^0: annihilator - sub*set* of linear functionals that map everything to zero
- U^0 is subspace of linear functionals on V

- IF U is a subspace of V then
	+ dim U + dim U^0 = dim V

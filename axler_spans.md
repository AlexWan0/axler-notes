## Basis
**Basis** properties
- only way to make zero is the trivial one
- linearly independent and spans V
- every vector in V can be written uniquely in terms of basis vectors
- every spanning list of length dim V is a basis
	- doesn't need to be independent
- can reduce spanning list to basis
- can expand linearly independent list to basis

expand subspace to full space with direct sum
- if V is subspace of U then there's a subspace W st direct_sum(V, W) = U
	- proof: expand bases

## Dimension
Dimension of subspace is smaller
- if U is a subpsace of V then dim U <= dim V

dim (U_1 + U_2) = dim U_1 + dim U_2 - dim(U_1 and U_2)
- proof: extend basis of U_1 and U_2 to basis of U_1 and basis of U_2
	- show that the combined basis vectors is that of U_1 + U_2
	- just need to show linear independence
		- do by rearranging basis vectors

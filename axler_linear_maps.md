# Linear Maps
Linear maps are subspaces T(V, W)
	Represents operations that are linear e.g. differentiation, integration

	V and W are just the subspaces that the input/output are - the input/output doesn't necessarily cover the entirety

1) You can always make a unique linear map between two subspaces
	Using their basis
	
	Proof: vector <-> basis conversion is linear

Null Spaces are subspaces
	null T(V, W): subset of V that T maps to 0

Injectivity	
	Tu = Tv implies u = v
	<=> null T = {0}

	Think: invertable, if output is the same, then input can't map to different things

Surjectivity
	range T = W

Ranges are subspaces
	All Tv for all v

Fundamental Theorem of Linear Maps
	dim V = dim null T + dim range T
	
	Proof: extend bases

Map from larger dim to smaller dim is not injective
Map from smaller dim to larger dim is not surjective
	Proof: use fundamental theorem

# Linear Maps -> Matrices
	T(v_1) . . . T(v_n)
	v_1			 v_n
w_1
.
.
.
w_m

Each k column represents T(v_k) as a linear comb of w_k

T(V, W) where V and W are represented with the bases w_i and v_i

How does a matrix dertermine a linear map?
	It contains the bases T(v_i) as columns
	Expressed in terms of w_i b/c that's the output space

# Matrix multiplication
If M(T) is to be representative of T then
	M(ST) should be = M(S)M(T)

	T: U -> V
	S: V -> W

	V is "hidden", part of the inner sum

	The output domain is represented with a linear combination over the bases vectors (each row in a column)

	let M(S) = A and M(T) = C

	Nested linear transformation of basis u_k
	(ST)u_k = S(sum_{r in rows of C} C_r,k v_r) # sum of V basis vectors for T transform

	sum_{r in rows of C} C_r,k S(v_r) # move S inside

	sum_{r in rows of C} C_r,k (sum_{j in rows of A} A_j,r w_j) # sum of W basis vectors for S transform

	We're looking for a W subspace output, so we want to write in the form of w basis vector sum

	sum_{j in rows of A} (sum_{r in rows of C} A_j,r C_r,k) w_j

	i.e. output transformation ST(u_k) is linear combination of sum_{r in rows of C} A_j,r C_r,k) and bases vectors w_j for each j

	The matrix is just the coefficients so

	M(ST) = sum_{r in rows of C} A_j,r C_r,k

Alternatively, thinking about matrix multiplication as multipling rows and columns
	column k of AC  = A (column k of C)
		The resulting column k of AC is only determined by the initial column k of C

	row j of AC = (row j of A) C
		The resulting row j of AC is only determined by the initial row j of A

Linear combinations
	Ac is linear combination of column vectors of A
	aC is a linear combination of row vectors of C

# Invertability
inverse of S is T s.t. ST = I and TS = I
	I linear map are different (V to V and W to W)

I is invertable

inverse of linear map is unique

isomorphism is an invertable linear map
	two vector spaces are isomorphic if there's an isomorphism between the two vector spaces

	is just a relabling

	isomorphism iff same dimensions bw vector spaces
		proof: apply linear map to bases

		fundamental theorem of linear maps and isomoprhisms
			dim V = dim null T + dim range T
			dim null T = 0 if injective b/c null T = {0}
			dim range T = dim W if surjective b/c range T = W

			isomorphism -> injective + surjective

M is an isomorphism between L(V, W) and F^m,n
	M is the operator that converts linear maps to matrices btw

dim L(V, W) = (dim V) (dim W)
	Proof: we know this to be true for matrices, we can convert the linear map to a matrix

# Linear maps act like matrix multiplication
We had M(ST) = M(S) M(T) earlier

We can also have M(u) of some vector u (wrt the output vector space)
	Just like normal. Column vector where each entry is the coefficient for a linear combination of bases of the ouput vector space

From this, we can say: M(Tu) = M(T) M(u)

# Operator
Linear map from vector space to itself
	L(V)

Suppose T is in L(V) then the following are equivalent for V that is finite dimensional
	T is invertible
	T is injective
	T is surjective

	i.e. T is injective <=> T is surjective
		USUALLY we need both injectivity and surjectivity for invertability but here we only need one

	Proof:
		fundamental theorem of linear maps
		dim null T = 0 <=> dim range T = dim V
		T is injective <=> T is surjective

		for dim range T = dim V means surjectivity
			dim range T is a subspace of V so they're equal iff dimensions are equal
				can think of this in terms of bases

				dim V linearly independent vectors that are in V

			can also think about this in terms of isomorphisms

# Product of Vector Spaces
Product of vector spaces is just every combination of vectors
	Is a subspace

	Dimension of product of vector spaces is sum of dimensions of individual spaces

Map from product to sum (gamma)
	that sum is a direct sum iff the map is injective
	proof: direct sum requires that only way to get zero is trivial zeros solution. injective iff null space is zeros.

-> Sum is direct iff dimensions add up
	proof: if direct sum then injective ^
		(gamma) is surjective cuz input is just the combination of the operands of the output sum, so is bijective/isomorphism
		so range space and domain space (of gamma) have same dim
		dimension of product of vector spaces is sum of dimensions of individual spaces

		i.e. thinking about sums in terms of combinations
			direct sum <-> injective mapping to sum (only one way to make a sum)
			direct sum dimensions sum <-> product dimensions sum

# Quotient of Vector Spaces
V/U where V is a subspace of U: *all* subspaces of V parallel to U
	think: parallel lines

	parallel subspaces: {v + U: v in V}

Is described by offset
	addition, scalar multiplication, zeros are on offset

	If offset is in U then it does nothing
		think: parallel lines

Parallel subspaces to U are equal or disjoint
	(a) v - w in U <=> (b)
		slope is in U (?)
		net effect is the same

	(b) v + U = w + U <=> v + U, w + U have non empty intersection
	v + U != w + U <=> v + U, w + U have empty intersection

	if they aren't completely equal then they have empty intersection
		adding v always keeps it parallel, there's no point intersections
			BUT it can miss it altogether bc dimensions

Quotient map
	pi: maps offset v to vector space v + U

	dim V/U = dim V - dim U
		proof: ft of linear maps
			dim V = dim null pi + dim range pi

			dim null pi: adding any u in U doesn't do anything bc u_1 + u_2 is already in U
			so dim null pi = dim U

			dim range pi = dim V/U

			rearrange to get formula

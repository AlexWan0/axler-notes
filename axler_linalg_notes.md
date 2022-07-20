# Random Thoughts/Intuitions
field denotes the "range" of scalar values
	has to be closed under operations

vector denotes the "range" of vectors of scalar values
	scalar values are defined by a field

	has to be closed under operations
		scalar multiplication and vector addition

F^n is vector space of n-length vectors
F^inf is vector space of infinite length vectors

vector space
	citeria
		has one element (e.g. zero)
		closed under vector addition
		closed under scalar multiplication

		other criteria?
		how to test for vector space vs actual criteria?

vector space of functions F^S
	set of all functions from S to F

	functions are defined by their input/output pairs
		so if you sum two functions
			you get a new function such that for input x, output is f(x) + g(x)

		and same for scalar multiplication

	equivelance to F^n or F^inf as
		for some list in F^n or F^inf
		input is index of list
		output is the value

		domain of input is n or inf
		range is F

subspaces
	subspaces can be over arbitrary elements
		as long as they have some operations defined
			see: functions

	criteria
		subset
		is vector space

continuous real valued functions on [0, 1] is a subspace of R^[0, 1]
	for some arbitrary input, sum of those outputs needs to be continous (around that input)

sum of subspaces
	is set of all possible sums between elements of two subspaces

	as union of two sets
		but the "non extended" version
		{a} U {b} = {a, b} needs to contain 4a + 2b

		so summing subspaces should have 4a + 2b included

	need to contain all elements from both subspaces, but also need to maintain vector space rules
		e.g. a from A and b from B

		what if we want 4a + 2b from summed vector set? need to add a value to the space that adds 4a from A and 2b from B

vector spaces as "extentions" of sets
	think mod/bijection stuff from cs70
		"set" of 5 mod 6 is actually "subspace" of 5, 11, 16 etc.

	if we have a set = {5}

	the vector space "version" of this would want 5, 10, 15, ... and 5, 0, -5, ...

	but *more*, has to satisfy all the subspace rules

direct sum
	direct sum is sum where there's only one way to make every element in sum subspace

	sum is direct sum between two sets iff intersection is only zero
		can't have two sets with only one dimension
			rel prime doesn't satisfy (2, 4, 6, 8, 10, ... vs 5, 10, 15, ...)

		(x, 0) (0, y) scenario
			covers separate dimensions

	sum is direct sum iff only way to write zero as a sum is where each element is zero
		(x, 0) (0, y) scenario

	as disjoint union of two sets
		union of two sets where the two sets are disjoint

		{a} U {b} = {a, b} normal union
			subspace contains every sum of a and b

		{a} U {a} = {a} normal union

		disjoint union retains the elements but with a different index to their respective sets
			{a_0, a_1}

			in retaining, we're adding a unique mapping to an originating set for each element in the resulting set

			i.e. each element in result set can be uniquely described by original sets
				with normal union, the resulting {a} could have "come from" either the first or second set

		{(a, 0)} U {(0, b)} = {(a, 0), (0, b)} disjoint
			a and b are just a_0 and a_1! 0 and 1 describe the index of the originating set!

			in the set, each element can be uniqely described by original sets (it's the same as before)

			subspaces
				subspace contains every comb (a, b)

				the "extention" of the set (a, b) can be still uniquely described by elements in its originating subspaces
					intuitively, for this example (they're on different dimensions)

					and by the definition of a direct sum

	-> direct sum says that elements can be uniquely described by their originating subspace elements

linear independence
	span but unique
		represent every vector in span but only way to do so 

	prove unique tech -> pretend it's not and subtract -> unique way to represent zero iff lin ind

	list of vectors contains a subset that's dependent
		start from a linearly independent list of vectors: v_1, v_2, v_3

		add a new one v_4 based on a linear combination of the other ones

		v_4 = av_1 + bv_2 + cv_3

		can now express ANY of the vectors with a combination of the other ones

		so can remove ANY of the vectors to make it linearly independent

	if we were to combine it with other vectors
		av_1 + bv_2 + cv_3 + dv_4 + ev_5 = 0 has nontrivial solution

		so we can choose any arbitrary vector to move to the isolate
			we can express it in terms of the other vectors, so we can remove it without changing the span!

		we can't remove the important vectors because their coefficient is zero
			i.e. the only way to zero out that term is to do the trivial solution

		-> if we have list of linearly dependent vectors we can remove one of them and keep the span
		
		-> that removed vector is in the span

	if you have a list of vectors that span V, then adding another vector in V will make list linearly dependent

	recursive proof
		setting: an overall linearly dependent list of vectors, with a subset of them being independent

linear dependence lemma
	there's some vector such that it's in the span of the previous elements
		(proof: the largest nonzero coeff)

		there's a vector such that it's in the span of the other nonzero coefficient vectors (plus an arbitrary number of zero coefficient ones)
			2.23 -> in some cases it includes u_i, in other cases it doesn't, ordering forces us to choose the latest ones
				can just as easily do the first nonzero term

				ordering forces a property about a consistent subset -> b/c we often know properties (like the span) of some subset that we want to compare

	removing it keeps the span

# Scope
- ## [Proof (from Introduction to Math Proof)](#proof)
- ## [Algorithms (from Mastering Algorithms with C)](#algorithms)




## Proof

- ### Proof of biconditional statements
	Proving biconditional statements is similar to proving by exhaustion.

	In Section 1.3, we showed that the biconditional statement P ⇔ Q is logically equivalent to (P ⇒ Q) ∧ (Q ⇒ P). Hence, the proof of a biconditional statement has the following form:
	
	Prove P ⇒ Q by any technique. Prove Q ⇒ P by any technique. Therefore, P ⇔ Q, since P ⇔ Q ≡ (P ⇒ Q ) ∧ (Q ⇒ P).
	
	Example:
	![proof-1](./proof-1.png)

- ### Proof by Contradiction of P aka _reductio ad absurdum_
	In Section 2.2.1 we showed how to prove the statement P ⇒ Q by contradiction. A proof by contradiction of the statement P (which may or may not be a conditional statement) is based on the logical equivalence P ≡ ((¬ P) ⇒ C) where C is a contradiction. To prove this equivalence, we recall the conditional statement (A ⇒ B) ≡ ((¬ A) ∨ B), so ((¬ P) ⇒ C) ≡ (¬ (¬ P) ∨ C) ≡ (P ∨ C) by double negation. Since C is a contradiction, C is a false statement and therefore (P∨ C) ≡ P. Hence, P ≡ ((¬ P) ⇒ C) where C is a contradiction, and the proof of the statement P by contradiction has the form:

	Assume ¬ P. . . . Therefore, C a contradiction. Hence, P. Often the contradiction C will be of the form R ∨ (¬ R) where R is any statement. A proof by contradiction of the statement P is also called an indirect proof or a _reductio ad absurdum_ proof.
	
	Example:
	![proof-2](./proof-2.png)

- ### Fundamental Theorem of Arithmetic
	Every natural number greater than one is a prime or can be written uniquely as a product of primes except for the order in which the prime factors are written.

	Example:

	Observe that 11 is a prime and the composite 12 = 2 · 2 · 3 = 2 · 3 · 2. Thus, the prime 2 is a factor of 12 exactly twice and the prime 3 is a factor of 12 exactly once and 12 can be written uniquely as 12 = 2 · 2 · 3 except for the fact that the order of the prime factors on the right-hand side of the last equation may be changed.

- ### Side Notes
	The number 1 is neither a composite number nor a prime number.

	It follows from the definition of composite number that the natural number n is composite if and only if there exist natural numbers a and b such that n = ab where 1 < a < n and 1 < b < n.

	If a divides b, then we also say a is a factor of b and b is divisible by a.


## Algorithms

- ### Side Notes
	At this point i read just about the importancy of algorithms and data structures in programmin, and how it improves efficiency, abstraction, and reusability. I read about types of algorithms, like randomized algorithms (quick sort), divide-and-conquer algorithms and dynamic programming solutions.

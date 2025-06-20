# Strong Induction

## Introduction

This lecture introduces strong induction, an alternative form of mathematical induction, along with the well-ordering property and demonstrates how these principles are equivalent.

## Strong Induction

Strong induction can be formalized as the following rule of inference:
1. P(1) is true
2. For all k ∈ N, if P(1), P(2), ..., P(k) are all true, then P(k+1) is true
3. Therefore, for all n ∈ N, P(n) is true

The key difference from regular induction is that the inductive step assumes all previous cases (not just the kth case) when proving the (k+1)th case.

## Example Proof Using Strong Induction

The lecture demonstrates strong induction by proving: "For all n ≥ 2, n is divisible by a prime number."

### Process:
1. **Base Case**: P(2) is true since 2 is divisible by itself, and 2 is prime
2. **Inductive Step**: Assume P(2), P(3), ..., P(k) are all true for some k ≥ 2
3. Consider P(k+1):
   - If k+1 is prime, then it is divisible by itself, so P(k+1) is true
   - If k+1 is not prime, then it has a divisor m where 2 ≤ m ≤ k
   - By the inductive hypothesis, m has a prime divisor p
   - Since p divides m and m divides k+1, p divides k+1
   - Therefore P(k+1) is true

## The Well-Ordering Property

The well-ordering property is an axiom stating that every non-empty subset of positive integers has a least element.

### Axioms about Natural Numbers:
1. 1 is a positive integer
2. If n is a positive integer, then n+1 is also a positive integer
3. Every positive integer except 1 is the successor of another positive integer
4. Every non-empty subset of positive integers has a least element (well-ordering)

## Proof Using Well-Ordering Property

The lecture reshows the same theorem ("For all n ≥ 2, n is divisible by a prime number") using the well-ordering property:

1. Let S be the set of integers greater than 1 with no prime divisor
2. Assume S is non-empty
3. By the well-ordering property, S must have a smallest element n
4. n cannot be prime (as it would then have itself as a prime divisor)
5. Since n is composite, it has a divisor d where 1 < d < n
6. By the minimality of n, d must have a prime divisor p
7. Since p divides d and d divides n, p divides n
8. This contradicts n being in S
9. Therefore, S must be empty, proving the theorem

## Equivalence of Induction Principles

The lecture concludes by stating that the following three principles are logically equivalent:
1. Mathematical induction
2. Strong induction
3. Well-ordering property

This means that proving a statement with any of these techniques is valid, and we can choose the approach that works best for a particular problem.

## Conclusion

Strong induction provides a powerful alternative to regular induction for proving statements where the step from k to k+1 depends on more than just the kth case. It is especially useful for problems involving divisibility, sequences with recurrence relations, and other problems where previous cases contribute to later ones.
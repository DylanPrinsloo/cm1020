# Introduction to Proofs

## Key Proof Types and Terminology

This lecture introduces three fundamental types of mathematical proofs and the terminology associated with them.

### Important Terminology

- **Proof**: A valid argument used to establish the truth of a statement
- **Theorem**: A formal statement that can be shown to be true
- **Axiom**: A statement assumed to be true that serves as a premise for further arguments
- **Lemma**: A proven statement used as a stepping stone toward a larger result
- **Corollary**: A theorem that can be established with a short proof from an existing theorem

## Three Types of Proofs

### 1. Direct Proof

- **Approach**: Prove that a conditional statement p → q is true by assuming p is true and showing q must be true
- **Process**: Start with the hypothesis and use axioms, definitions, and rules of inference to reach the conclusion
- **Example**: Proving "there exists a real number between any two unequal real numbers"
  - Let x and y be arbitrary real numbers with x < y
  - Define z = (x+y)/2
  - Show z is between x and y, proving the theorem

### 2. Proof by Contrapositive

- **Approach**: Based on the fact that p → q is equivalent to its contrapositive ¬q → ¬p
- **Process**: Assume ¬q is true and show that ¬p must also be true
- **Example**: Proving "if n² is even, then n is even"
  - Instead of proving directly, prove the contrapositive: "if n is odd, then n² is odd"
  - Assume n is odd, so n = 2k+1 for some integer k
  - Show n² = (2k+1)² = 4k²+4k+1 = 2(2k²+2k)+1, which is odd
  - Thus, proved the contrapositive, establishing the original theorem

### 3. Proof by Contradiction

- **Approach**: Assume the statement to be proven is false and show this leads to a logical contradiction
- **Process**: Assume ¬p is true, then derive a contradiction, showing ¬p must be false (and therefore p is true)
- **Example**: Proving "there are infinitely many prime numbers"
  - Assume there are only finitely many primes: p₁, p₂, ..., pₙ
  - Consider number c = (p₁×p₂×...×pₙ) + 1
  - This number must have at least one prime divisor
  - Show that no existing prime p₁ through pₙ can divide c (leads to contradiction)
  - Therefore, the assumption is false, and there must be infinitely many primes

## Conclusion

These three proof techniques form the foundation of mathematical reasoning. Each approach has its strengths and is applicable in different scenarios:
- Direct proofs are straightforward when a clear path exists from hypothesis to conclusion
- Contrapositive proofs are useful when proving the original implication directly is difficult
- Contradiction proofs are powerful for existence or impossibility proofs

Understanding these methods allows mathematicians to tackle a wide range of problems and establish the truth of mathematical statements with rigorous logical arguments.
# Proof by Induction

## Introduction

This lecture explores how mathematical induction can be used to prove various types of statements, including formulas, inequalities, and divisibility properties. It also demonstrates how induction can go wrong if not properly applied.

## Proving a Formula by Induction

The lecture begins with proving the sum formula: 
$$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

### Process:
1. **Base Case**: Verify P(1) is true
   - Left side: 1
   - Right side: (1)(1+1)/2 = 1
   - Therefore P(1) is true

2. **Inductive Step**: Assume P(k) is true and prove P(k+1) is true
   - Assume sum from 1 to k equals k(k+1)/2
   - Then the sum from 1 to k+1 = k(k+1)/2 + (k+1)
   - After algebraic manipulation: (k+1)(k+2)/2
   - Which is the formula for P(k+1)

## Proving an Inequality by Induction

The lecture then shows how to prove: 3^n < n! for all n ≥ 7

### Process:
1. **Base Case**: Verify P(7) is true
   - Left side: 3^7 = 2,187
   - Right side: 7! = 5,040
   - Since 2,187 < 5,040, P(7) is true

2. **Inductive Step**: Assume P(k) is true and prove P(k+1) is true
   - Assume 3^k < k!
   - Then 3^(k+1) = 3 × 3^k < 3 × k!
   - Since k ≥ 7, we know 3 < k+1
   - Therefore 3^(k+1) < (k+1) × k! = (k+1)!
   - Thus P(k+1) is true

## Proving Divisibility by Induction

The lecture demonstrates proving that 6^n + 4 is divisible by 5 for all n ≥ 0

### Process:
1. **Base Case**: Verify P(0) is true
   - 6^0 + 4 = 1 + 4 = 5, which is divisible by 5

2. **Inductive Step**: Assume P(k) is true and prove P(k+1) is true
   - Assume 6^k + 4 = 5p for some p ∈ ℕ
   - Then 6^(k+1) + 4 = 6 × 6^k + 4 = 6 × (5p - 4) + 4 = 30p - 24 + 4 = 30p - 20 = 5(6p - 4)
   - Therefore 6^(k+1) + 4 is divisible by 5
   - Thus P(k+1) is true

## Example of Incorrect Induction

The lecture provides a critical example of how induction can go wrong:

- Attempting to prove: sum of 2^i from i=0 to n-1 equals 2^n for all n ∈ ℕ

### Error Analysis:
1. **Inductive Step**: The proof correctly shows that if P(k) is true, then P(k+1) is true
2. **Critical Mistake**: The base case was not verified
3. **Counterexample**: For n=2, the left side is 2^0 + 2^1 = 1 + 2 = 3, but the right side is 2^2 = 4

This example highlights that both the base case and inductive step must be verified for a proof by induction to be valid. False assumptions can lead to seemingly valid but actually incorrect conclusions.

## Conclusion

The lecture emphasizes that mathematical induction is a powerful technique for proving various types of statements, but proper application requires careful verification of both the base case and the inductive step to avoid fallacious reasoning.
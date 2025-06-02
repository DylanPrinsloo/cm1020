# Postulates of Boolean Algebra

## [Introduction](images/33_outlines.png)

Boolean algebra is governed by a set of fundamental rules that allow us to analyze and design digital circuits. This lesson covers:

1. Huntington's postulates (six axioms)
2. Derived theorems and rules
3. De Morgan's theorems
4. Principle of duality
5. Methods for proving Boolean equivalence

## [Huntington's Postulates](images/huntingtons_postulates.png)

Huntington defined six fundamental axioms that must be satisfied by any Boolean algebra:

1. **Closure**: The result of any Boolean operation is either 0 or 1
2. **Identity**: 
   - x + 0 = x (0 is identity for OR)
   - x · 1 = x (1 is identity for AND)
3. **Commutativity**:
   - x + y = y + x
   - x · y = y · x
4. **Complements**:
   - x + x' = 1
   - x · x' = 0
5. **Distributivity**:
   - x + (y · z) = (x + y) · (x + z)
   - x · (y + z) = (x · y) + (x · z)
6. **Distinct Elements**: Any Boolean algebra has exactly two distinct values (0 and 1)

## [Derived Theorems](images/33_basic_theorems.png)

From these six axioms, we can derive additional rules:

### Idempotent Laws
- x + x = x
- x · x = x

### Tautology and Contradiction
- x + 1 = 1 (tautology)
- x · 0 = 0 (contradiction)

### Involution
- (x')' = x

### Associative Laws
- (x + y) + z = x + (y + z)
- (x · y) · z = x · (y · z)

### Absorption Laws
- x + (x · y) = x
- x · (x + y) = x

### Uniqueness of Complements
- If y + x = 1 and y · x = 0, then x = y'

### Inversion Law
- 0' = 1
- 1' = 0

## De Morgan's Theorems

1. [**First Theorem**:](images/33_de_morgans_theorem_1_2.png)
   - (x · y)' = x' + y'
   - "The complement of a product equals the sum of the complements"

```
Truth Table:
x | y | x·y | (x·y)' | x' | y' | x'+y'
--|---|-----|--------|----|----|------
0 | 0 |  0  |    1   |  1 |  1 |   1
0 | 1 |  0  |    1   |  1 |  0 |   1
1 | 0 |  0  |    1   |  0 |  1 |   1
1 | 1 |  1  |    0   |  0 |  0 |   0
```

1. [**Second Theorem**:](images/33_de_morgans_theorem_1_2.png)
   - (x + y)' = x' · y'
   - "The complement of a sum equals the product of the complements"

```
Truth Table:
x | y | x+y | (x+y)' | x' | y' | x'·y'
--|---|-----|--------|----|----|------
0 | 0 |  0  |    1   |  1 |  1 |   1
0 | 1 |  1  |    0   |  1 |  0 |   0
1 | 0 |  1  |    0   |  0 |  1 |   0
1 | 1 |  1  |    0   |  0 |  0 |   0
```

## [Principle of Duality](images/principle_of_duality.png)

The principle of duality states that from any Boolean relation, we can derive another valid relation by:
1. Changing every OR (+) to AND (·)
2. Changing every AND (·) to OR (+)
3. Changing all 0s to 1s and all 1s to 0s

### Example of Duality
Original: A + (B · C) = (A + B) · (A + C)
Dual: A · (B + C) = (A · B) + (A · C)

## Proving Boolean Equivalence

[There are four primary methods for proving equivalence between Boolean expressions:](images/ways_of_proving_theorems.png)

1. **Perfect Induction**: Show that the expressions have identical truth tables
2. **Axiomatic Proof**: Apply Huntington's postulates or derived theorems
3. **Duality Principle**: Apply the principle of duality to a known theorem
4. **Proof by Contradiction**: Assume the hypothesis is false and show this leads to a false conclusion

### Example: [Proving the Absorption Rule](images/example_absorption_theorem.png)

Using a truth table:
```
x | y | x·y | x+(x·y)
--|---|-----|--------
0 | 0 |  0  |    0
0 | 1 |  0  |    0
1 | 0 |  0  |    1
1 | 1 |  1  |    1
```

The truth table confirms that x + (x·y) = x for all possible values of x and y.

Using axioms:
1. x + (x·y) = (x·1) + (x·y)   [Identity law]
2. = x·(1 + y)                [Distributivity]
3. = x·1                      [1 + y = 1]
4. = x                        [Identity law]

By duality, we can also conclude that x·(x + y) = x.
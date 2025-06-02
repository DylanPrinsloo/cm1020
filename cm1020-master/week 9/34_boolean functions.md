# Boolean Functions

## Introduction to Boolean Functions

A Boolean function defines a mapping from one or multiple Boolean input values to a Boolean output value. For n Boolean input values, there are 2^n possible input combinations.

## Representation of Boolean Functions

Boolean functions can be represented in different ways:

### 1. Truth Table Representation
- Shows the output for every possible combination of inputs
- For a function with n inputs, the truth table has 2^n rows
- There is only one way to represent a Boolean function in a truth table

```
Example with 3 inputs (x, y, z):
x | y | z | f(x,y,z)
--|---|---|--------
0 | 0 | 0 |    0
0 | 0 | 1 |    1
0 | 1 | 0 |    0
0 | 1 | 1 |    1
1 | 0 | 0 |    0
1 | 0 | 1 |    1
1 | 1 | 0 |    1
1 | 1 | 1 |    1
```

### 2. Algebraic Representation
- A function can be expressed in multiple algebraic forms
- Example: f(x) = x + x'y and f(x) = x + y are equivalent

## [Standardized Forms](images/34_standardised_forms_of_a_function.png)

### 1. Sum of Products (SOP) Form
- Variables combined using the AND operator are summed together using the OR operator
- Example: f(x,y,z) = xy + xz + yz
- Also called disjunctive normal form

### 2. Product of Sums (POS) Form
- Variables combined using the OR operator are multiplied together using the AND operator
- Example: f(x,y,z) = (x+y)(x+z)(y+z)
- Also called conjunctive normal form

## Creating Sum of Products Form from Truth Table

To create an SOP expression from a truth table:

1. Focus on the rows where the output equals 1
2. For each such row:
   - If an input is 1, use the uncomplemented variable
   - If an input is 0, use the complemented variable (x')
3. Create a product term for each row where output is 1
4. Combine all product terms with OR operations

```
Example:
Truth Table for f(x,y):
x | y | f(x,y)
--|---|------
0 | 0 |   0
0 | 1 |   1
1 | 0 |   1
1 | 1 |   1

SOP Form: f(x,y) = x'y + xy' + xy
```

## [Useful Boolean Functions](images/34_useful_functions.png)

### 1. Exclusive OR (XOR) Function
- Notation: x ⊕ y
- True if either x or y is true, but not both
- Also called inequality function

```
Truth Table for XOR:
x | y | x⊕y
--|---|----
0 | 0 |  0
0 | 1 |  1
1 | 0 |  1
1 | 1 |  0

Algebraic form: x⊕y = x'y + xy'
```

### 2. Implication Function
- Notation: x → y
- Represents "if x then y"
- False only when x is true and y is false

```
Truth Table for Implication:
x | y | x→y
--|---|----
0 | 0 |  1
0 | 1 |  1
1 | 0 |  0
1 | 1 |  1

Algebraic form: x→y = x' + y
```

## Summary

Boolean functions are fundamental in digital design and can be represented in various forms:
- Truth tables provide a complete enumeration of all input-output combinations
- Algebraic expressions can take different forms but represent the same function
- Standard forms (SOP and POS) provide systematic ways to express functions
- Special functions like XOR and implication have important applications in logic and circuit design
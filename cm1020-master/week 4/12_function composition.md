# Function Composition: A Complete Guide

## What is Function Composition?

Function composition is like creating a **chain of operations** where the output of one function becomes the input of another. Think of it as an assembly line where each station performs a specific task on the product passing through.

## 1. Formal Definition

Given two functions:
- **G**: A → B (takes inputs from set A, produces outputs in set B)
- **F**: B → C (takes inputs from set B, produces outputs in set C)

Their **composition** F ∘ G (read as "F composed with G" or "F after G") is defined as:

```
(F ∘ G)(x) = F(G(x))
```

This creates a new function that goes directly from A to C.

## 2. The Two-Stage Process

To evaluate (F ∘ G)(x), follow these steps:

**Stage 1**: Apply G to the input x
- Result: G(x)

**Stage 2**: Apply F to the result from Stage 1
- Result: F(G(x))

### Visual Representation
```
Input x → [Function G] → G(x) → [Function F] → F(G(x)) = (F ∘ G)(x)
```

## 3. Concrete Example with Step-by-Step Solution

Let's define:
- G(x) = x² (squaring function)
- F(u) = 2u (doubling function)

**Finding (F ∘ G)(x):**

**Step 1**: Apply G first
- G(x) = x²

**Step 2**: Apply F to the result
- F(G(x)) = F(x²) = 2(x²) = 2x²

**Therefore**: (F ∘ G)(x) = 2x²

**Testing with x = 3:**
- G(3) = 3² = 9
- F(9) = 2(9) = 18
- So (F ∘ G)(3) = 18 ✓

## 4. Domain and Codomain Visualization

```
Set A (Domain)     Set B (Intermediate)     Set C (Codomain)
    x      ──G──>      G(x)      ──F──>      F(G(x))
    │                    │                      │
    └──────── F ∘ G ─────────────────────────────┘
```

The composition F ∘ G creates a direct path from A to C, bypassing the need to explicitly work with set B.

## 5. Extended Numerical Example

Define:
- G(x) = 3x + 2
- F(x) = 2x + 3

**Finding the general form of (F ∘ G)(x):**

**Step 1**: G(x) = 3x + 2

**Step 2**: F(G(x)) = F(3x + 2) = 2(3x + 2) + 3 = 6x + 4 + 3 = 6x + 7

**Therefore**: (F ∘ G)(x) = 6x + 7

**Verification with x = 1:**
- G(1) = 3(1) + 2 = 5
- F(5) = 2(5) + 3 = 13
- Using our formula: (F ∘ G)(1) = 6(1) + 7 = 13 ✓

## 6. Why Order Matters: Non-Commutativity

**Key Insight**: F ∘ G ≠ G ∘ F (in general)

The order of composition matters because functions process information in sequence. Changing the order changes the entire process.

### Detailed Example

Using G(x) = x² and F(x) = 2x:

**Computing F ∘ G:**
- (F ∘ G)(x) = F(G(x)) = F(x²) = 2(x²) = 2x²

**Computing G ∘ F:**
- (G ∘ F)(x) = G(F(x)) = G(2x) = (2x)² = 4x²

**Comparison:**
- (F ∘ G)(x) = 2x²
- (G ∘ F)(x) = 4x²

These are clearly different functions! For x = 2:
- (F ∘ G)(2) = 2(2²) = 8
- (G ∘ F)(2) = 4(2²) = 16

### Real-World Analogy

Think of getting dressed:
- **Operation A**: Put on socks
- **Operation B**: Put on shoes

**A then B**: Put on socks, then shoes → Normal result
**B then A**: Put on shoes, then socks → Awkward result!

The order of operations fundamentally changes the outcome.

## 7. Important Notes

1. **Domain Compatibility**: For F ∘ G to exist, the codomain of G must be compatible with the domain of F.

2. **Notation**: F ∘ G means "F after G" or "apply G first, then F."

3. **Associativity**: While not commutative, composition is associative: (H ∘ F) ∘ G = H ∘ (F ∘ G).

4. **Function Machines**: Think of functions as machines that transform inputs into outputs. Composition is like connecting these machines in series.

## 8. Practice Problems

Try these to test your understanding:

**Problem 1**: If G(x) = x + 1 and F(x) = x³, find (F ∘ G)(2).

**Problem 2**: Show that if G(x) = √x and F(x) = x², then (F ∘ G)(x) ≠ (G ∘ F)(x) for x > 0.

**Solutions:**
1. G(2) = 3, F(3) = 27, so (F ∘ G)(2) = 27
2. (F ∘ G)(x) = (√x)² = x, but (G ∘ F)(x) = √(x²) = |x| = x for x > 0, so they're equal in this case! (This shows that while order usually matters, there are special cases where it doesn't.)
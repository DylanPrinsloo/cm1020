# Logic Networks and Boolean Simplification

## Combinational Circuits (Logic Networks)

Combinational circuits are arrangements of logic gates that implement Boolean functions where:
- Outputs depend solely on current input values
- No memory or feedback is involved
- Output is determined by the current configuration of inputs

## Building Logic Networks
1. **Boolean Function → Circuit**: Translate expressions directly to gates
2. **Circuit → Boolean Function**: Label gate outputs and work backward

## Example Applications: Adders
- **Half Adder**: Adds two binary bits
  * Sum output = XOR gate
  * Carry output = AND gate
  * Limitation: Only two inputs

- **Full Adder**: Adds three binary bits (includes carry-in)
  * Three inputs: x, y, carry-in
  * Two outputs: sum, carry-out
  * Used for multi-bit addition

## Boolean Function Simplification

**Benefits of Simplification:**
- Reduces circuit cost (fewer gates)
- Improves performance (less computation time)
- Enables more circuits on same chip

**Two Simplification Methods:**

1. **Algebraic Simplification**
   - Uses Boolean algebra laws:
     * De Morgan's Laws
     * Distributive Laws
     * Commutative/Idempotent Laws 
     * Complement Laws
     * Absorption Law

2. **Karnaugh Maps (K-maps)**
   - Graphical method representing Boolean functions
   - Cells differ by one variable are adjacent
   - Process: Group adjacent 1's into rectangles (powers of 2)
   - Works well for 2-5 variables

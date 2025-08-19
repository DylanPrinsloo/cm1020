## The Binomial Theorem and Pascal's Triangle

### Introduction

The binomial theorem provides a powerful method for expanding expressions involving two terms raised to a power. As the power increases, manual expansion becomes increasingly complex, making the binomial theorem an essential tool in algebra, combinatorics, and probability theory.

### Binomial Expressions

#### Definition
A **binomial expression** is an algebraic expression consisting of exactly two terms connected by addition or subtraction.

**Examples of Binomial Expressions:**
- $x + a$
- $2x - y$ 
- $x^2 - y^2$
- $2x - 3y$

#### The Challenge of Higher Powers
As we raise binomials to higher powers, expansion becomes increasingly complex:

- $(x + y)^1 = x + y$
- $(x + y)^2 = x^2 + 2xy + y^2$
- $(x + y)^3 = x^3 + 3x^2y + 3xy^2 + y^3$

Expanding $(x + y)^{30}$ manually would be extremely tedious and error-prone!

### [The Binomial Theorem](images/binomial_theorem.png)

#### Statement
For any two variables $x$ and $y$, and any non-negative integer $n$:

$$(x + y)^n = \sum_{k=0}^{n} \binom{n}{k} x^k y^{n-k}$$

#### Expanded Form
$$(x + y)^n = \binom{n}{0}x^0y^n + \binom{n}{1}x^1y^{n-1} + \binom{n}{2}x^2y^{n-2} + \cdots + \binom{n}{n}x^ny^0$$

#### [Example Application: Finding Specific Coefficients](images/binomial_theorem_example.png)

**Problem**: Find the coefficient of $x^8y^7$ in the expansion of $(3x - y)^{15}$.

**Solution**:
1. Rewrite as $(3x + (-y))^{15}$
2. (a = 3x), (b = -y), (n = 15)
3. Apply binomial theorem: 
   $$\sum_{k=0}^{15} \binom{15}{k} (3x)^k (-y)^{15-k}$$
4. For the term $x^8y^7$, we need $k = 8$ and $15-k = 7$  
   $$\sum_{k=0}^{15} \binom{15}{k} (3x)^8 (-y)^{7}$$
5. The coefficient is: 
   $$\binom{15}{8} \cdot 3^8 \cdot (-1)^7 = -3^8 \cdot \frac{15!}{8! \cdot 7!}$$

### Applications of the Binomial Theorem

#### Proving Combinatorial Identities

**Identity**: $2^n = \sum_{k=0}^{n} \binom{n}{k}$

**Proof**: Apply the binomial theorem with $x = 1$ and $y = 1$:
$$(1 + 1)^n = \sum_{k=0}^{n} \binom{n}{k} \cdot 1^k \cdot 1^{n-k} = \sum_{k=0}^{n} \binom{n}{k}$$

Therefore: $2^n = \sum_{k=0}^{n} \binom{n}{k}$

#### Counting Subsets

**Theorem**: The number of subsets of a set with $n$ elements is $2^n$.

**Proof**: 
A set with $n$ elements has:
- $\binom{n}{0}$ subsets with 0 elements
- $\binom{n}{1}$ subsets with 1 element  
- $\binom{n}{2}$ subsets with 2 elements
- $\vdots$
- $\binom{n}{n}$ subsets with $n$ elements

Total number of subsets = $\sum_{k=0}^{n} \binom{n}{k} = 2^n$

### [Pascal's Identity](images/pascals_identity.png)

#### Statement
For integers $n \geq k \geq 1$:
$$\binom{n}{k} + \binom{n}{k-1} = \binom{n+1}{k}$$

#### Combinatorial Proof
**Setup**: Let $T$ be a set with $n+1$ elements, and let $S$ be a subset of $T$ containing all elements except one specific element $a$.

**Analysis**: The number of $k$-element subsets of $T$ is $\binom{n+1}{k}$.

Each $k$-element subset of $T$ either:
1. **Contains element $a$**: Must choose $k-1$ additional elements from $S$ → $\binom{n}{k-1}$ ways
2. **Doesn't contain element $a$**: Must choose all $k$ elements from $S$ → $\binom{n}{k}$ ways

**Conclusion**: $\binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}$ ∎

### [Pascal's Triangle](images/pascals_triangle.png)

#### Construction
Pascal's triangle is a geometric arrangement of binomial coefficients where:
- Element at position $(n,r)$ equals $\binom{n}{r}$
- Each row $n$ contains the coefficients for $(x+y)^n$

#### Visual Representation
```
Row 0:           1
Row 1:         1   1  
Row 2:       1   2   1
Row 3:     1   3   3   1
Row 4:   1   4   6   4   1
Row 5: 1   5  10  10   5   1
```

#### Pascal's Identity in the Triangle
Pascal's identity shows that each element equals the sum of the two elements above it:

$$\binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}$$

**Visual Example**: 
- $\binom{4}{2} = 6$
- $\binom{3}{1} + \binom{3}{2} = 3 + 3 = 6$ ✓

#### Properties of Pascal's Triangle

**Symmetry**: $\binom{n}{k} = \binom{n}{n-k}$
- Triangle is symmetric about its center
- Choosing $k$ elements is equivalent to excluding $n-k$ elements

**Row Sums**: $\sum_{k=0}^{n} \binom{n}{k} = 2^n$
- Sum of any row equals a power of 2
- Confirms our subset counting theorem

**Alternating Sum**: $\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0$ for $n > 0$
- Obtained by setting $x = 1, y = -1$ in binomial theorem

### Computational Applications

#### Efficient Coefficient Calculation
Instead of computing $\binom{n}{k} = \frac{n!}{k!(n-k)!}$ directly:

```javascript
// Using Pascal's triangle for efficient computation
function buildPascalTriangle(rows) {
    const triangle = [];
    
    for (let n = 0; n <= rows; n++) {
        triangle[n] = [];
        triangle[n][0] = 1; // First element of each row
        triangle[n][n] = 1; // Last element of each row
        
        // Use Pascal's identity for interior elements
        for (let k = 1; k < n; k++) {
            triangle[n][k] = triangle[n-1][k-1] + triangle[n-1][k];
        }
    }
    
    return triangle;
}

// Get binomial coefficient C(n,k)
function binomialCoefficient(n, k, triangle) {
    return triangle[n][k];
}
```

#### Probability Applications
The binomial theorem appears frequently in probability:

**Binomial Distribution**: Probability of exactly $k$ successes in $n$ trials:
$$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$

Where the binomial coefficients come directly from the binomial theorem expansion.

### Key Relationships and Identities

#### Fundamental Identities
1. **Pascal's Identity**: $\binom{n}{k} + \binom{n}{k-1} = \binom{n+1}{k}$
2. **Symmetry**: $\binom{n}{k} = \binom{n}{n-k}$
3. **Sum Identity**: $\sum_{k=0}^{n} \binom{n}{k} = 2^n$
4. **Alternating Sum**: $\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0$ (for $n > 0$)

#### Connection to Combinatorics
The binomial theorem bridges algebra and combinatorics:
- **Algebraic view**: Method for expanding polynomial expressions
- **Combinatorial view**: Counting arrangements and selections
- **Unified perspective**: Binomial coefficients appear in both contexts naturally

### Summary

This lecture introduced fundamental concepts linking algebra, combinatorics, and computation:

1. **Binomial Theorem**: Systematic method for expanding $(x+y)^n$ using binomial coefficients
2. **Pascal's Identity**: Recursive relationship enabling efficient computation of binomial coefficients  
3. **Pascal's Triangle**: Geometric representation providing intuitive understanding and computational efficiency
4. **Applications**: From algebraic manipulation to subset counting and probability theory

The elegance of these concepts lies in their interconnectedness—the same mathematical structures appear across different areas of mathematics, demonstrating the deep unity underlying mathematical thinking.

**Key Insight**: Pascal's triangle and the binomial theorem provide both theoretical understanding and practical computational tools, making complex algebraic operations manageable while revealing beautiful mathematical patterns.
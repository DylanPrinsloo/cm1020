## Generalized Permutations and Combinations

### Introduction

Building on our foundation of basic permutations and combinations, we now explore more sophisticated counting scenarios. The key distinction is whether **repetition is allowed** in our selections, which dramatically changes both the counting formulas and their applications.

### Permutations with Repetition

#### Definition and Formula
When selecting $r$ objects from $n$ types of objects **with repetition allowed**, the number of possible arrangements is:

$$P(n,r)_{\text{with repetition}} = n^r$$

#### Proof Using Product Rule
Since repetition is permitted:
- **First selection**: $n$ possibilities
- **Second selection**: $n$ possibilities (can repeat)
- **Third selection**: $n$ possibilities
- $\vdots$
- **$r$-th selection**: $n$ possibilities

By the product rule: $n \times n \times n \times \cdots \times n = n^r$

#### Example: String Formation
**Problem**: How many strings of length $r$ can be formed using only uppercase letters from the English alphabet?

**Solution**: 
- We have 26 uppercase letters available
- Each position in the string can use any of the 26 letters (repetition allowed)
- Total strings = $26^r$

**Specific Cases**:
- 3-letter strings: $26^3 = 17,576$
- 4-letter strings: $26^4 = 456,976$

### Permutations without Repetition (Review)

#### Formula
When selecting $r$ objects from $n$ distinct objects **without repetition**:

$$P(n,r) = \frac{n!}{(n-r)!} = n \times (n-1) \times (n-2) \times \cdots \times (n-r+1)$$

#### Example: Running Competition
**Problem**: 10 runners are taking part in a competition. How many different ways can first and second place be awarded?

**Solution**:
- First place: 10 choices
- Second place: 9 remaining choices (no repetition)
- Total arrangements = $P(10,2) = \frac{10!}{8!} = 10 \times 9 = 90$

### Combinations with Repetition (Multisets)

#### Definition and Formula
When selecting $k$ objects from $n$ categories **with repetition allowed** (order doesn't matter):

$$C(n,k)_{\text{with repetition}} = \binom{n+k-1}{k} = \frac{(n+k-1)!}{k!(n-1)!}$$

#### Alternative Interpretations
This formula counts:
1. **Multisets**: Collections where elements can be repeated
2. **Identical balls in distinct boxes**: Ways to put $k$ identical balls into $n$ distinct boxes
3. **Functions**: Number of functions from a set of $k$ identical elements to a set of $n$ distinct elements

#### Stars and Bars Method
**Visual Approach**: Use "stars" (★) to represent objects and "bars" (|) to separate categories.

**Example**: Find all multisets of size 3 from the set $\{1, 2, 3, 4\}$.

The multiset $\{1, 1, 3\}$ is represented as: ★★|★||

**Counting Process**:
- Total positions needed: $k + (n-1) = 3 + 3 = 6$
- Choose $k$ positions for stars: $\binom{6}{3}$
- Answer: $\binom{3+4-1}{3} = \binom{6}{3} = 20$

**JavaScript Implementation**:
```javascript
function combinations WithRepetition(n, k) {
    return binomialCoefficient(n + k - 1, k);
}

function binomialCoefficient(n, k) {
    if (k > n) return 0;
    if (k === 0 || k === n) return 1;
    
    // Use the more efficient of C(n,k) or C(n,n-k)
    k = Math.min(k, n - k);
    
    let result = 1;
    for (let i = 0; i < k; i++) {
        result = result * (n - i) / (i + 1);
    }
    
    return Math.round(result);
}

// Example: multisets of size 3 from 4 categories
console.log(combinationsWithRepetition(4, 3)); // Output: 20
```

### Combinations without Repetition (Review)

#### Formula
When selecting $k$ objects from $n$ distinct objects **without repetition** (order doesn't matter):

$$C(n,k) = \binom{n}{k} = \frac{n!}{k!(n-k)!}$$

#### Alternative Interpretations
1. **Subsets**: Number of $k$-element subsets of an $n$-element set
2. **Distinct balls in distinct boxes**: Ways to put $k$ distinct balls into $n$ distinct boxes (each box holds at most one ball)
3. **Injective functions**: Number of one-to-one functions from a $k$-element set to an $n$-element set

### Complete Formula Summary

| Scenario | Order Matters? | Repetition Allowed? | Formula | Notation |
|----------|----------------|-------------------|---------|----------|
| **Permutations with repetition** | Yes | Yes | $n^r$ | - |
| **Permutations without repetition** | Yes | No | $\frac{n!}{(n-r)!}$ | $P(n,r)$ |
| **Combinations with repetition** | No | Yes | $\binom{n+k-1}{k}$ | $\left(\binom{n}{k}\right)$ |
| **Combinations without repetition** | No | No | $\binom{n}{k}$ | $C(n,k)$ |

### Decision Framework

To choose the correct formula, ask these questions:

1. **Does order matter?**
   - Yes → Use permutation formulas
   - No → Use combination formulas

2. **Can elements be repeated?**
   - Yes → Use repetition formulas
   - No → Use standard formulas

### Application Example: Committee Selection

**Problem**: John is chair of a committee. In how many ways can a committee of 3 be chosen from 10 people, given that John must be selected?

**Solution Analysis**:
- John is already chosen (fixed)
- Need to choose 2 more people from remaining 9
- Order doesn't matter (it's a committee)
- No repetition (each person appears once)

**Formula Application**:
$$\binom{9}{2} = \frac{9!}{2!(9-2)!} = \frac{9!}{2! \cdot 7!} = \frac{9 \times 8}{2 \times 1} = 36$$

### Real-World Applications

#### Computer Science Applications
1. **Password Generation**: Permutations with repetition ($26^r$ for letter passwords)
2. **Hash Table Design**: Combinations without repetition for key selection
3. **Algorithm Analysis**: Counting possible states or configurations
4. **Cryptography**: Key space calculations and randomness requirements

#### Probability and Statistics
1. **Sample Spaces**: Counting possible outcomes
2. **Probability Distributions**: Binomial and multinomial distributions
3. **Experimental Design**: Counting treatment combinations
4. **Quality Control**: Sampling without replacement scenarios

#### Practical Implementation
```javascript
// Complete toolkit for generalized counting
class CombinatoricsCalculator {
    // Permutations with repetition
    static permutationsWithRep(n, r) {
        return Math.pow(n, r);
    }
    
    // Permutations without repetition  
    static permutationsWithoutRep(n, r) {
        if (r > n) return 0;
        let result = 1;
        for (let i = 0; i < r; i++) {
            result *= (n - i);
        }
        return result;
    }
    
    // Combinations with repetition (stars and bars)
    static combinationsWithRep(n, k) {
        return this.binomial(n + k - 1, k);
    }
    
    // Combinations without repetition
    static combinationsWithoutRep(n, k) {
        return this.binomial(n, k);
    }
    
    // Helper: binomial coefficient
    static binomial(n, k) {
        if (k > n || k < 0) return 0;
        if (k === 0 || k === n) return 1;
        
        k = Math.min(k, n - k); // Use symmetry for efficiency
        
        let result = 1;
        for (let i = 0; i < k; i++) {
            result = result * (n - i) / (i + 1);
        }
        
        return Math.round(result);
    }
}

// Usage examples
console.log("Password possibilities (4 letters):", 
           CombinatoricsCalculator.permutationsWithRep(26, 4));

console.log("Race winners (1st, 2nd from 10):", 
           CombinatoricsCalculator.permutationsWithoutRep(10, 2));

console.log("Multisets of size 3 from 4 items:", 
           CombinatoricsCalculator.combinationsWithRep(4, 3));

console.log("Committee of 3 from 10 people:", 
           CombinatoricsCalculator.combinationsWithoutRep(10, 3));
```

### Key Insights and Patterns

#### Mathematical Relationships
1. **Repetition increases possibilities**: $n^r \geq \frac{n!}{(n-r)!}$ when repetition is allowed
2. **Order increases possibilities**: $\frac{n!}{(n-r)!} \geq \binom{n}{r}$ when order matters
3. **Symmetry in combinations**: $\binom{n}{k} = \binom{n}{n-k}$

#### Problem-Solving Strategy
1. **Identify the scenario**: What type of selection process is described?
2. **Ask key questions**: Does order matter? Is repetition allowed?
3. **Apply appropriate formula**: Use the decision framework
4. **Verify reasonableness**: Check if the answer makes intuitive sense

### Summary

This lecture expanded our combinatorial toolkit to handle four fundamental counting scenarios:

1. **Permutations with repetition** ($n^r$): Order matters, repetition allowed
2. **Permutations without repetition** ($\frac{n!}{(n-r)!}$): Order matters, no repetition  
3. **Combinations with repetition** ($\binom{n+k-1}{k}$): Order doesn't matter, repetition allowed
4. **Combinations without repetition** ($\binom{n}{k}$): Order doesn't matter, no repetition

**Key Takeaway**: Understanding when to apply each formula is crucial for solving real-world counting problems. The systematic approach of identifying whether order matters and whether repetition is allowed provides a reliable framework for tackling complex combinatorial challenges.

These tools are fundamental for:
- **Algorithm analysis**: Counting possible states and configurations
- **Probability theory**: Determining sample spaces and event probabilities  
- **Cryptography**: Calculating key spaces and security parameters
- **Computer science applications**: From database design to machine learning
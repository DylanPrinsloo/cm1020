## Fundamental Counting Principles

### 1. The Product Rule (Multiplication Principle)

When a process consists of multiple sequential tasks, and each task can be executed independently:

**Rule**: If task 1 can be done in $n$ ways and task 2 can be done in $m$ ways, then the entire process can be completed in $n \times m$ ways.

**General Form**: For $k$ sequential tasks with $n_1, n_2, \ldots, n_k$ ways respectively:
$$\text{Total ways} = n_1 \times n_2 \times \cdots \times n_k$$

**Example: Restaurant Combination Meals**
A restaurant offers:
- 2 salads
- 3 main dishes  
- 4 side dishes
- 3 desserts

Total combination meals = $2 \times 3 \times 4 \times 3 = 72$

**Set Theory Interpretation**: If $A$ and $B$ are disjoint sets representing ways to do tasks 1 and 2:
$$|A \times B| = |A| \times |B|$$

### 2. The Addition Rule (Sum Rule)

When we have multiple independent alternative ways to complete a task:

**Rule**: If task 1 can be done in $n$ ways OR task 2 can be done in $m$ ways (but not both), then there are $n + m$ total ways.

**Example: Committee Representative Selection**
Choose either:
- 1 of 10 academic staff members, OR
- 1 of 77 students

Total choices = $10 + 77 = 87$

**Set Theory Interpretation**: For disjoint sets $A$ and $B$:
$$|A \cup B| = |A| + |B|$$

### 3. Combining Sum and Product Rules

Complex problems often require both rules working together.

**Example: Programming Language Labels**
Labels can be:
- A single letter (26 possibilities), OR  
- A letter followed by two digits ($26 \times 10 \times 10$ possibilities)

Total labels = $26 + (26 \times 10 \times 10) = 26 + 2600 = 2626$

### 4. The Subtraction Rule (Inclusion-Exclusion Principle)

When counting overlapping sets, we must avoid double-counting:

**Rule**: If a task can be done in $n_1$ ways OR $n_2$ ways, with some overlap:
$$\text{Total ways} = n_1 + n_2 - \text{(overlapping ways)}$$

**Example: Binary Strings**
Count 8-bit binary strings that either:
- Start with "1", OR
- End with "00"

- Strings starting with "1": $2^7 = 128$
- Strings ending with "00": $2^6 = 64$  
- Strings starting with "1" AND ending with "00": $2^5 = 32$

Total = $128 + 64 - 32 = 160$

### 5. The Division Rule

When multiple counting methods produce the same result, we divide to avoid overcounting:

**Rule**: If a procedure can be carried out in $n$ ways, and exactly $d$ of these ways correspond to each distinct outcome, then there are $\frac{n}{d}$ distinct outcomes.

**Set Theory**: If finite set $A$ is the union of $n$ pairwise disjoint subsets, each with $d$ elements:
$$|A| = \frac{n}{d}$$

**Function Theory**: If function $f: A \to B$ maps exactly $d$ elements of $A$ to each element of $B$:
$$|B| = \frac{|A|}{d}$$

**Example: Circular Seating Arrangements**
Seat 4 people around a table where rotations are considered identical:

- Linear arrangements: $4! = 24$
- Each circular arrangement corresponds to 4 rotations
- Distinct circular arrangements: $\frac{24}{4} = 6$

## Key Takeaways

These fundamental counting principles form the foundation of combinatorics:

1. **Product Rule**: For sequential independent tasks
2. **Addition Rule**: For mutually exclusive alternatives  
3. **Subtraction Rule**: For overlapping cases (inclusion-exclusion)
4. **Division Rule**: For eliminating symmetric overcounting

Understanding when and how to apply each rule is crucial for solving complex combinatorial problems in computer science, probability, and discrete mathematics.
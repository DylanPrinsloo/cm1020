# 1. Overview on laws of sets

The lecture introduces fundamental algebraic properties that also apply to sets. Specifically, it covers:

- **Commutativity**: Changing the order of elements (or operands) does not change the result.
- **Associativity**: Changing the grouping of elements does not affect the outcome.
- **Distributivity**: One operation can “distribute” over another in a way that preserves the result.

In addition to these properties, the lecture reviews several standard set identities such as De Morgan's laws, identities involving the universal set and the empty set, the complement laws, and the absorption law. These identities are useful for simplifying set expressions.


### 2. Commutativity

**Definition:**  
An operation is said to be commutative if the order of operands does not affect the result.

**Key Examples:**

- **Addition and Multiplication:**  
  - *Addition:* \(2 + 3 = 3 + 2\)  
  - *Multiplication:* \(2 \times 3 = 3 \times 2\)
  
- **Set Operations:**  
  - *Union:* \(A \cup B = B \cup A\)  
  - *Intersection:* \(A \cap B = B \cap A\)  
  - *Symmetric Difference:* The symmetric difference is also commutative.
  
- **Non-Commutative Operations:**  
  - *Subtraction:* \(2 - 3 \neq 3 - 2\)  
  - *Set Difference:* \(A - B \neq B - A\) (For example, if \(A=\{1,2\}\) and \(B=\{1,3\}\), then \(A-B=\{2\}\) while \(B-A=\{3\}\).)

The takeaway is that while many familiar operations are commutative, operations such as subtraction and set difference are not.


### 3. Associativity

**Definition:**  
An operation is associative if the way in which operands are grouped does not change the result.

**Key Examples:**

- **Addition:**  
  With three numbers \(A\), \(B\), and \(C\),  
  \[
  A + (B + C) = (A + B) + C
  \]

- **Set Operations:**  
  - *Union:* \((A \cup B) \cup C = A \cup (B \cup C)\)  
  - *Intersection:* \((A \cap B) \cap C = A \cap (B \cap C)\)  
  - *Symmetric Difference:* Also follows associativity.

- **Non-Associative Operation:**  
  - *Set Difference:* The grouping matters for set difference. For three sets \(A\), \(B\), and \(C\),  
    - \( (A - B) - C\) might yield a different result from \(A - (B - C)\).

Understanding associativity is crucial when simplifying expressions because it tells us that grouping parentheses can be re-arranged freely for operations like union and intersection.


### 4. Distributivity

**Definition:**  
An operation is distributive over another when applying it over a combination (such as a sum) is equivalent to applying it individually over each element, and then combining the results.

**Key Examples in Arithmetic:**

- **Multiplication over Addition:**  
  \[
  3 \times (2 + 5) = (3 \times 2) + (3 \times 5)
  \]

**Key Examples in Set Theory:**

- **Union Over Intersection:**  
  \[
  A \cup (B \cap C) = (A \cup B) \cap (A \cup C)
  \]
  
- **Intersection Over Union:**  
  \[
  A \cap (B \cup C) = (A \cap B) \cup (A \cap C)
  \]

Membership tables can be used to verify that both sides of these expressions yield the same result, confirming distributivity.

### 5. Additional Set Identities

Several other identities were mentioned in the lecture:

- **De Morgan's Laws:**
  - The complement of a union equals the intersection of the complements:
    \[
    (A \cup B)^c = A^c \cap B^c
    \]
  - The complement of an intersection equals the union of the complements:
    \[
    (A \cap B)^c = A^c \cup B^c
    \]

- **Identity Laws:**
  - \(A \cup \emptyset = A\)  
  - \(A \cup U = U\) (where \(U\) is the universal set)
  - \(A \cap \emptyset = \emptyset\)  
  - \(A \cap U = A\)

- **Complement Laws:**
  - \(A \cup A^c = U\)  
  - \(A \cap A^c = \emptyset\)  
  - \((A^c)^c = A\)

- **Absorption Law:**
  - \(A \cup (A \cap B) = A\)  
  - \(A \cap (A \cup B) = A\)

- **Set Difference:**
  - \(A - B\) can be written as \(A \cap B^c\).

These identities are tools to rewrite and simplify expressions involving sets.


### 6. Application: Simplifying a Set Expression

An example was given to show how these identities can simplify complex expressions:

- **Expression:**  
  \[
  (A \cap B)^c \cup A^c \quad \text{is shown to be equivalent to} \quad B \cap A^c
  \]

**Step-by-Step Explanation:**

1. **Apply De Morgan’s Law:**  
   Start by rewriting the complement of \(A \cap B\) as  
   \[
   (A \cap B)^c = A^c \cup B^c
   \]
   Now, the expression becomes:
   \[
   (A^c \cup B^c) \cup A^c
   \]
2. **Use Commutativity and Idempotence:**  
   Recognizing that \(A^c\) appears twice and using commutativity (order doesn’t matter), you combine them:
   \[
   A^c \cup B^c = A^c \cup B^c \quad (\text{since duplicate elements don’t change the union})
   \]
3. **Rewriting Using the Distributive Law:**  
   Rearranging terms (and possibly applying additional set laws) leads to the simplified result:
   \[
   B \cap A^c
   \]
   The lecture illustrated how membership tables and set laws support this equivalence.
   


### Conclusion

>The lecturer had outlined the importance of understanding the properties of commutativity, associativity, and distributivity, not just for numerical operations but also for set operations. Recognizing which set operations share these properties and which do not is key. Additional notes on identities such as De Morgan’s laws, complement and identity laws, and the absorption law further empower us to simplify and evaluate complex set expressions systematically.

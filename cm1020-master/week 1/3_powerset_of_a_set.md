# **Summary of Power Set Concepts**

1. **Definition of a Power Set:**
   
   - The *power set* of a set S, denoted as P(S), is the set of all possible subsets of S.
  
   - Every subset of S—including the empty set and S itself—is an element of P(S).

2. **Subsets Versus Elements in Context:**
   
   - When discussing power sets, it’s important to distinguish between a subset and an element.
  
   - For example, if A is a set and B is its power set, any subset of A is an element of B.

   - An element of A might be a number, object, or another set, while an element of the power set P(A) is one of A’s subsets.

3. **Examples Illustrating Power Sets:**
   
   - **Example with a set S = {1, 2, 3}:**
  
     - The subsets of S are:  
       • The empty set: {}  
       • Single-element subsets: {1}, {2}, {3}  
       • Two-element subsets: {1, 2}, {1, 3}, {2, 3}  
       • The subset equal to S: {1, 2, 3}

     - Thus, P(S) = {{}, {1}, {2}, {3}, {1, 2}, {1, 3}, {2, 3}, {1, 2, 3}}.
  
   - This example shows that if S contains 3 elements, its power set will contain 2³ = 8 subsets.

4. **Special Cases – Power Set of the Empty Set:**

   - The empty set (∅) has exactly one subset: itself.
  
   - Therefore, the power set of the empty set is P(∅) = {∅}.
  
   - Taking the power set of P(∅) yields: P(P(∅)) = {∅, {∅}}.
   - 
     - Here, the empty set is both an element and (trivially) a subset.

     - This demonstrates that the elements of a power set are always subsets of the original set.

5. **Cardinality of a Power Set:**

   - The *cardinality* (or number of elements) of the power set of a set S is given by 2 raised to the power of the cardinality of S.
  
   - In other words, if |S| = n, then |P(S)| = 2ⁿ.
- 
   - For example, a set with 3 elements has a power set with 2³ = 8 subsets.
  
   - This relation can be extended. For instance, if one takes the power set of a power set, the relation is applied again. 
   
     - If A is a set with |A| = n, then:
       • |P(A)| = 2ⁿ  
       • |P(P(A))| = 2^(2ⁿ)  
       • |P(P(P(A)))| = 2^(2^(2ⁿ))

6. **Clarifying Subset and Element Statements:**

   - When a set contains another set as an element (e.g., a subset of A being considered as an element in P(A)), correct notation is used:
  
     - If X is a subset of S, then X ∈ P(S).
- 
     - In exercises, questions may ask whether a particular set (like {a}) is an element or a subset of P(S). The answer is that since every subset of S is in P(S), {a} is both a subset of S and an element of the power set P(S).


**Key Takeaways:**

- A power set includes all subsets of a set, from the empty set to the set itself.
  
- The number of elements in a power set grows exponentially with the number of elements in the original set.
  
- It is essential to understand and correctly denote the difference between a subset and an element when discussing power sets.

[Subset recap, and understanding of sets](images/subset-recap-image.PNG)
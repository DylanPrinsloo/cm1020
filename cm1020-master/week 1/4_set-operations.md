# **Summary Overview of set operations**

The lesson introduces four primary operations that can be performed on sets:

1. **Union (A ∪ B)**
   
2. **Intersection (A ∩ B)**
   
3. **Set Difference (A – B)**
   
4. **Symmetric Difference (A Δ B)**

Each operation combines sets in different ways by either including or excluding elements based on their membership in the original sets. The lesson also discusses how these operations can be described using set-builder notation and illustrated with membership tables (which use 1 to indicate membership and 0 to indicate non-membership).


## **1. Union of Sets (A ∪ B)**

- **Definition:** 
   
  The union of two sets A and B is the set containing all elements that are in A, in B, or in both.  
  In set-builder notation:  
  `A ∪ B = { x | x ∈ A or x ∈ B }`

- **Example:** 
   
  If A = {2, 4, 6, 8} and B = {1, 3, 5, 7, 9}, then:  
  `A ∪ B = {1, 2, 3, 4, 5, 6, 7, 8, 9}`

- **Membership Table:** 
   
  The table shows all possible combinations of membership (0 for not in, 1 for in):
  - (0 in A, 0 in B): x is not in A ∪ B.
  
  - (0 in A, 1 in B): x is in A ∪ B.

  - (1 in A, 0 in B): x is in A ∪ B.
  
  - (1 in A, 1 in B): x is in A ∪ B.


## **2. Intersection of Sets (A ∩ B)**

- **Definition:**  
  
  The intersection of A and B is the set of all elements that are common to both A and B.  
  In set-builder notation:  
  `A ∩ B = { x | x ∈ A and x ∈ B }`

- **Example:**  
  
  If A and B are such that only the numbers 3 and 7 occur in both, then:  
  `A ∩ B = {3, 7}`

- **Membership Table:** 
 
  In the table for intersection:

  - (0, 0): x is not in the intersection.

  - (0, 1) and (1, 0): x is not in the intersection.
  
  - (1, 1): x is in the intersection.


## **3. Set Difference (A – B)**

- **Definition:** 
 
  The set difference A – B includes all elements that are in A but *not* in B.  
  In set-builder notation:  
  `A – B = { x | x ∈ A and x ∉ B }`

- **Example:** 
   
  If A = {2, 3, 4, 6, 7} and B = {3, 4, 7}, then:  
  `A – B = {2, 6}`  
  That is, remove from A every element that is also in B.

- **Membership Table:**  
  
  In a membership table for A – B:

  - An element with 1 in A and 0 in B will be included.
  
  - If an element is either not in A or is in B, it is not included in A – B.


## **4. Symmetric Difference (A Δ B)**

- **Definition:**  
  
  The symmetric difference between A and B includes all elements that are in A or in B but excludes the ones that are in both.  
  It can be defined in two equivalent ways:

  - As the union minus the intersection:  
    `A Δ B = (A ∪ B) – (A ∩ B)`

  - Or as the union of the two differences:  
    `A Δ B = (A – B) ∪ (B – A)`

- **Example:**  
  
  Suppose A = {2, 4, 6, 8} and B = {1, 3, 5, 7, 9} with a common part already accounted for elsewhere (or consider a case where some elements appear only in one set). If the common elements are removed, the symmetric difference might be, for example,  
  `A Δ B = {1, 2, 5, 6}`  

  (This result depends on which elements are shared; the idea is that only those elements that appear exclusively in one set remain.)

- **Membership Table:** 
   
  For symmetric difference:

  - (0, 0): x is not in A Δ B.
  
  - (1, 1): x is not in A Δ B (because x is in both sets).
  
  - (1, 0) or (0, 1): x is in A Δ B.


## **Summary of How the Operations Differ**

- **Union** combines all elements with no repetition (even if an element is in both sets, it appears only once).
- **Intersection** narrows down the focus to those elements that occur in every set considered.
- **Set Difference** subtracts the elements of one set from another, effectively “removing” any common elements.
- **Symmetric Difference** gives a “non-overlapping” union by taking elements that are unique to each set (i.e., in one set and not the other).

Membership tables provide a systematic way to display these rules by encoding each element’s membership (1 if present, 0 if absent) and then applying the logical conditions (or, and, not) corresponding to each set operation.

### [images/De Morgan's Laws](images/de-morgans-law.JPG) are fundamental principles in set theory and logic that describe the relationships between the union and intersection of sets through their complements (opposites). Formulated by the British mathematician Augustus De Morgan, these laws provide a way to express the complement of the union of two sets in terms of the intersection of their complements, and vice versa.

## The two laws are stated as follows:

1. **First Law**: The complement of the union of two sets A and B is equal to the intersection of their complements. In set notation:

   (A ∪ B)′ = A′ ∩ B′

2. **Second Law**: The complement of the intersection of two sets A and B is equal to the union of their complements. In set notation:

   (A ∩ B)′ = A′ ∪ B′

## These laws can be visualized and verified using **Venn diagrams**: 

- **First Law**: In a Venn diagram, the union of sets A and B includes all elements in either A or B. The complement of this union consists of 
  elements not in A or B. This area is the same as the intersection of the complements of A and B, 
  confirming that [(A ∪ B)′ = A′ ∩ B′.](images/de-morgans-law-1st--venn.png)

- **Second Law**: Similarly, the intersection of sets A and B includes only elements common to both. The complement of this intersection consists of elements not common to both A and B. This area corresponds to the union of the complements of A and B, confirming that [(A ∩ B)′ = A′ ∪ B′.](images/de-morgans-law-2nd-proof-venn.png)

**Truth tables** can also be used to prove these laws in the context of Boolean algebra by demonstrating that both sides of the equations yield the same truth values for all possible inputs.

- [(A ∪ B)′ = A′ ∩ B′]((images/de-morgans-law-proof-mem-tbls.JPG))
  
- [(A ∩ B)′ = A′ ∪ B′](images/de-morgans-law-membership-table-2.png)

[**Example**:](images/de-morgans-law-example.png)

Consider the universal set U = {1, 2, 3, 4, 5, 6, 7, 8, 9}, with subsets A = {1, 2, 3, 4} and B = {4, 5, 6, 7}.

- **Union**: A ∪ B = {1, 2, 3, 4, 5, 6, 7}

- **Intersection**: A ∩ B = {4}

- **Complement of Union**: (A ∪ B)′ = {8, 9}

- **Complement of Intersection**: (A ∩ B)′ = {1, 2, 3, 5, 6, 7, 8, 9}

- **Intersection of Complements**: A′ ∩ B′ = {8, 9}

- **Union of Complements**: A′ ∪ B′ = {1, 2, 3, 5, 6, 7, 8, 9}

Here, (A ∪ B)′ equals A′ ∩ B′, and (A ∩ B)′ equals A′ ∪ B′, illustrating De Morgan's Laws.


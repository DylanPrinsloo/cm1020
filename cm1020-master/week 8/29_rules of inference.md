# [Rules of Inference in Propositional Logic](images/rules_of_inference_outlined.png)

## Valid Arguments

An argument in propositional logic is a sequence of propositions, where:
- The final proposition is called the **conclusion**
- The other propositions are called **premises** or **hypotheses**

An argument is **valid** if the truth of all its premises implies the truth of the conclusion.

### Example of Valid Argument
- Premise 1: If you have access to the internet, you can order a book on machine learning
- Premise 2: You have access to the internet
- Conclusion: You can order a book on machine learning

This argument is valid because whenever all premises are true, the conclusion must also be true.

### Example of Invalid Argument
- Premise 1: If you have access to the internet, you can order a book on machine learning
- Premise 2: You can order a book on machine learning
- Conclusion: You have access to the internet

This argument is not valid because we can imagine situations where the premises are true and the conclusion is false.

## Rules of Inference

Rules of inference serve as building blocks for constructing complex valid arguments. While truth tables can determine argument validity, they become impractical with multiple variables (e.g., 8 variables require 256 rows). Rules of inference provide a simpler approach.

Each rule of inference can be proved using a tautology.

### Modus Ponens

**Tautology**: [(p → q) ∧ p] → q

**Argument form**:
- p → q
- p
- Therefore, q

**Example**:
- Let p: "It is snowing"
- Let q: "I will study discrete mathematics"
- If "If it is snowing, I will study discrete mathematics" is true
- And "It is snowing" is true
- Then "I will study discrete mathematics" is true

### Modus Tollens

**Tautology**: [(p → q) ∧ ¬q] → ¬p

**Argument form**:
- p → q
- ¬q
- Therefore, ¬p

**Example**:
- Let p: "It is snowing"
- Let q: "I will study discrete mathematics"
- If "If it is snowing, I will study discrete mathematics" is true
- And "I will not study discrete mathematics" is true
- Then "It is not snowing" is true

### Conjunction

**Tautology**: [p ∧ q] → (p ∧ q)

**Argument form**:
- p
- q
- Therefore, p ∧ q

**Example**:
- Let p: "I will study programming"
- Let q: "I will study discrete mathematics"
- If "I will study programming" is true
- And "I will study discrete mathematics" is true
- Then "I will study programming and discrete mathematics" is true

### Simplification

**Tautology**: (p ∧ q) → p

**Argument form**:
- p ∧ q
- Therefore, p

**Example**:
- Let p: "I will study discrete mathematics"
- Let q: "I will study programming"
- If "I will study discrete mathematics and programming" is true
- Then "I will study discrete mathematics" is true

### Addition

**Tautology**: p → (p ∨ q)

**Argument form**:
- p
- Therefore, p ∨ q

**Example**:
- Let p: "I will visit Paris"
- Let q: "I will study discrete mathematics"
- If "I will visit Paris" is true
- Then "I will visit Paris or I will study discrete mathematics" is true

### Hypothetical Syllogism

**Tautology**: [(p → q) ∧ (q → r)] → (p → r)

**Argument form**:
- p → q
- q → r
- Therefore, p → r

**Example**:
- Let p: "It is snowing"
- Let q: "I will study discrete mathematics"
- Let r: "I will pass the quizzes"
- If "If it is snowing, I will study discrete mathematics" is true
- And "If I study discrete mathematics, I will pass the quizzes" is true
- Then "If it is snowing, I will pass the quizzes" is true

### Disjunctive Syllogism

**Tautology**: [(p ∨ q) ∧ ¬p] → q

**Argument form**:
- p ∨ q
- ¬p
- Therefore, q

**Example**:
- Let p: "I will study discrete mathematics"
- Let q: "I will study art"
- If "I will study discrete mathematics or I will study art" is true
- And "I will not study discrete mathematics" is true
- Then "I will study art" is true

### Resolution

**Tautology**: [(p ∨ q) ∧ (¬p ∨ r)] → (q ∨ r)

**Argument form**:
- p ∨ q
- ¬p ∨ r
- Therefore, q ∨ r

**Example**:
- Let p: "It is raining"
- Let q: "It is snowing"
- Let r: "It is cold"
- If "It is raining or it is snowing" is true
- And "It is not raining or it is cold" is true
- Then "It is snowing or it is cold" is true

## Building Valid Arguments

To build a valid argument:
1. If the argument is in English, transform it into an argument form by choosing a variable for each simple proposition
2. Start with the hypotheses of the argument
3. Build a sequence of steps where each step follows from previous steps by applying rules of inference and laws of logic
4. The final step is the conclusion

### Example of Building a Valid Argument

**Premises**:
1. It is not cold tonight
2. We will go to the theater only if it is cold
3. If we do not go to the theater, we will watch a movie at home
4. If we watch a movie at home, we will need to make popcorn

**Define proposition variables**:
- p: It is cold tonight
- q: We will go to the theater
- r: We will watch a movie at home
- s: We will need to make popcorn

**Formalized premises**:
1. ¬p
2. q → p
3. ¬q → r
4. r → s

**Building the argument**:
1. ¬p (given)
2. q → p (given)
3. ¬q (from 1, 2 by modus tollens)
4. ¬q → r (given)
5. r (from 3, 4 by modus ponens)
6. r → s (given)
7. s (from 5, 6 by modus ponens)

Therefore, the conclusion is: "We will need to make popcorn"

## Formal Fallacies

Fallacies are incorrect arguments in reasoning. Formal fallacies can be expressed in propositional logic and proven incorrect. Common formal fallacies include:

- Affirming the consequence
- Conclusion that denies premises
- Contradictory premises
- Denying the antecedent
- Existential fallacy
- Exclusive premises

### Example: Affirming the Consequence

**Invalid Argument**:
- If you have internet access, you can order this book
- You can order this book
- Therefore, you have internet access

**Formalized**: (p → q) ∧ q, therefore p

This is not a valid argument because (p → q) ∧ q → p is not a tautology (it's false when p is false and q is true).

---

# Summary 🧠

### 1. **Modus Ponens**

If `P → Q` and `P` are both true, then `Q` is true.
**Form:**

```
P → Q  
P  
∴ Q
```

### 2. **Modus Tollens**

If `P → Q` and `¬Q` are true, then `¬P` is true.
**Form:**

```
P → Q  
¬Q  
∴ ¬P
```

### 3. **Hypothetical Syllogism**

If `P → Q` and `Q → R` are true, then `P → R` is true.
**Form:**

```
P → Q  
Q → R  
∴ P → R
```

### 4. **Disjunctive Syllogism**

If `P ∨ Q` and `¬P` are true, then `Q` is true.
**Form:**

```
P ∨ Q  
¬P  
∴ Q
```

### 5. **Conjunction**

If `P` and `Q` are both true, then `P ∧ Q` is true.
**Form:**

```
P  
Q  
∴ P ∧ Q
```

### 6. **Simplification**

If `P ∧ Q` is true, then `P` is true.
**Form:**

```
P ∧ Q  
∴ P
```

### 7. **Addition**

If `P` is true, then `P ∨ Q` is true.
**Form:**

```
P  
∴ P ∨ Q
```

### 8. **Existential Instantiation**

From `∃x P(x)`, infer `P(c)` for some specific `c`.
**Form:**

```
∃x P(x)  
∴ P(c)
```

### 9. **Universal Generalization**

From `P(c)` for arbitrary `c`, infer `∀x P(x)`.
**Form:**

```
P(c) (for arbitrary c)  
∴ ∀x P(x)
```

### 10. **Existential Generalization**

From `P(c)` for some `c`, infer `∃x P(x)`.
**Form:**

```
P(c) (for some c)  
∴ ∃x P(x)
```

---

# ✅ Examples

### **Example 1**

**Given:**

1. `P ∨ Q` (Premise)
2. `¬P` (Premise)

**To Prove:** `Q`

**Solution:**

```
1. P ∨ Q          (Premise)  
2. ¬P             (Premise)  
3. Q              (From 1 and 2 using Disjunctive Syllogism)  
∴ Q
```

---

### **Example 2**

**Given:**

1. `∀x(P(x) → R(x))`
2. `∀x(Q(x) → S(x))`
3. `P(a)`
4. `Q(a)`

**To Prove:** `R(a) ∧ S(a)`

**Solution:**

```
1. ∀x(P(x) → R(x))       (Premise)  
2. ∀x(Q(x) → S(x))       (Premise)  
3. P(a)                  (Premise)  
4. Q(a)                  (Premise)  
5. P(a) → R(a)           (From 1 using Universal Instantiation)  
6. Q(a) → S(a)           (From 2 using Universal Instantiation)  
7. R(a)                  (From 3 and 5 using Modus Ponens)  
8. S(a)                  (From 4 and 6 using Modus Ponens)  
9. R(a) ∧ S(a)           (From 7 and 8 using Conjunction)  
∴ R(a) ∧ S(a)
```
# Laws of Propositional Logic

In this lecture, we will explore a number of propositional logic laws. First, we'll introduce and discuss some important laws of propositional logic including DeMorgan's laws. Then, we will show how these laws are used in practice to build a reasoning and prove equivalence.

## Introduction to Propositional Logic Laws

We said at the beginning of the topic that propositional logic is an algebra involving multiple laws. Let's take a look at some of the most important of them:

### Idempotent Laws
- $p \lor p \equiv p$ 
- $p \land p \equiv p$

### Commutative Laws
- $p \lor q \equiv q \lor p$
- $p \land q \equiv q \land p$

### Associative Laws
- $(p \lor q) \lor r \equiv p \lor (q \lor r)$
- $(p \land q) \land r \equiv p \land (q \land r)$

### Distributive Laws
- $p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$
- $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$

### Identity Laws
- $p \lor \text{false} \equiv p$
- $p \land \text{true} \equiv p$

### Domination Laws
- $p \lor \text{true} \equiv \text{true}$
- $p \land \text{false} \equiv \text{false}$

## Proving Logical Equivalence

Now, let's prove a case of Distributive Law of disjunction over conjunction. Take the following two compound propositions:
- $(p \lor q) \land r$
- $(p \land r) \lor (q \land r)$

By constructing the truth table for these compound propositions, we can see that they are logically equivalent.

## DeMorgan's Laws

DeMorgan's laws are very useful. They formalize how we negate conjunction and disjunction. The basic idea behind this law is to ensure that we change the logical connective after we negate.

- $\neg(p \land q) \equiv \neg p \lor \neg q$
- $\neg(p \lor q) \equiv \neg p \land \neg q$

For instance, the negation of disjunction is formed by taking the conjunction of the negation of the component propositions.

## Additional Important Laws

Other laws can be useful for simplifying compound propositions such as:

### Absorption Laws
- $p \lor (p \land q) \equiv p$
- $p \land (p \lor q) \equiv p$

### Negation Laws
- $p \lor \neg p \equiv \text{true}$ (Tautology)
- $p \land \neg p \equiv \text{false}$ (Contradiction)

### Double Negation Law
- $\neg\neg p \equiv p$

## Building an Equivalence Proof

Now, let's see how we can use the laws that we have seen so far to build an equivalence proof. For instance, let's examine the equivalence between these two compound propositions:

The given proposition is $\neg p \land (\neg p \lor q)$.

1. Using DeMorgan's laws, we have $\neg p \lor \neg(\neg p \lor q)$
2. Using DeMorgan's laws again, we have $\neg p \lor (\neg\neg p \land \neg q)$
3. Using the double negation law, we have $\neg p \lor (p \land \neg q)$
4. Using the distributive laws, we have $(\neg p \lor p) \land (\neg p \lor \neg q)$
5. Using the complement laws (negation laws), we have $\text{true} \land (\neg p \lor \neg q)$
6. Finally, using the identity law, we arrive at $\neg p \lor \neg q$

This means that these two propositions are equivalent: $\neg p \land (\neg p \lor q) \equiv \neg p \lor \neg q$

## Summary

In this lecture, we looked at a number of propositional logic laws. First, we introduced and explored some important laws of propositional logic including DeMorgan's laws. Then we saw how these laws are used in practice to simplify complex expressions and prove that two propositions are equivalent.
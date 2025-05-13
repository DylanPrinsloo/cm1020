# Logical Equivalence

In this lecture, we will discuss logical equivalence. We will:
1. Define the equivalence logical operator and examine some of its properties
2. Show how to prove that two propositions are equivalent using a truth table
3. Update the table of precedence by including implication and equivalence

## Definition of Logical Equivalence

In the last lecture, we explained logical implication. Now, we will define and investigate logical equivalence.

Let $p$ and $q$ be propositions. The **biconditional** or **equivalent statement**, $p \iff q$ is the proposition "$p$ implies $q$ and $q$ implies $p$." 

Biconditional statements are also called **bi-implications** and can also be expressed as "$p$ if and only if $q$."

## Truth Table for Biconditional

As shown in the truth table of equivalence, the biconditional statement $p \iff q$ is true when $p$ and $q$ have the same truth values and is false if this isn't the case.

| $p$ | $q$ | $p \iff q$ |
|-----|-----|------------|
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | F          |
| F   | F   | T          |

## Equivalent Propositions

Now, let's examine the concept of equivalent propositions, which is slightly different from equivalent statements.

Let $p$ and $q$ be propositions. $p$ and $q$ are **logically equivalent** if they always have the same truth value. We'll write $p \equiv q$.

Let's note that the symbol $\equiv$ is not a logical operator. $p \equiv q$ is not a compound proposition, but rather is the statement that $p \iff q$ is always true.

## Proving Equivalence Using Truth Tables

One way to determine equivalence is to use truth tables and check whether the two propositions have the same truth values.

For instance, let's compare the two propositions, $p \implies q$ and $\neg p \lor q$.

Let's begin by building the truth table:

| $p$ | $q$ | $p \implies q$ | $\neg p$ | $\neg p \lor q$ |
|-----|-----|----------------|----------|----------------|
| T   | T   | T              | F        | T              |
| T   | F   | F              | F        | F              |
| F   | T   | T              | T        | T              |
| F   | F   | T              | T        | T              |

The truth table shows us that $\neg p \lor q$ is equivalent to $p \implies q$ as they have the same truth values.

## Determining Non-Equivalence

In order to determine non-equivalence, we can use truth tables and find at least one row where the values differ.

For instance, let's examine whether the converse or the inverse of an implication is equivalent to the original implication.

Let's build the truth table:

| $p$ | $q$ | $p \implies q$ | $\neg p \implies \neg q$ (inverse) | $q \implies p$ (converse) |
|-----|-----|----------------|-----------------------------------|--------------------------|
| T   | T   | T              | T                                 | T                        |
| T   | F   | F              | T                                 | T                        |
| F   | T   | T              | F                                 | F                        |
| F   | F   | T              | T                                 | T                        |

The truth table shows that the converse and inverse propositions are different from $p \implies q$ as they have different truth values in the second and third rows.

## Example with Symbolic Expressions

Let's look at an example to illustrate what you have learned so far in this lecture.

Let $p$, $q$, and $r$ be the following propositions concerning unknown integer $n$:
- $p$ is the proposition "$n$ is equal to 20"
- $q$ is proposition "$n$ is even" 
- $r$ is proposition "$n$ is positive"

Let's express each of the following conditional statements symbolically:
- "If $n$ equals 20, then $n$ is positive" can be expressed as $p \implies r$
- "$n$ equals 20, if $n$ is even" can be expressed as $q \implies p$
- "$n$ equals 20, only if $n$ is even" can be expressed as $p \implies q$

## Precedence of Logical Operators

We have already looked at the precedence order of compound propositions: conjunction, disjunction, and negation. We have seen how it is used to simplify complex compound propositions.

Now that we have explored logical implication and logical equivalence, let's update the table to show the precedence order of compound propositions, including implication and equivalence:

1. Negation ($\neg$)
2. Conjunction ($\land$)
3. Disjunction ($\lor$)
4. Implication ($\implies$)
5. Equivalence ($\iff$)

## Summary

In this lecture, we have discussed logical equivalence. First, we defined equivalence and explored some of its properties. Then we showed how we can use truth tables to prove that two propositions are equivalent. Finally, we discussed the precedence of implication and equivalence in relation to the other logical operators seen in the previous lecture: negation, conjunction, and disjunction.
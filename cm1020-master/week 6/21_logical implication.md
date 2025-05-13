# Logical Implication

In this lecture, we will talk about logical implication. We will begin by defining an implication or conditional statements, then we will build its truth table, and finally we will discuss the converse, inverse, and contrapositive of an implication.

## Defining Implication

Let $p$ and $q$ be propositions. The **conditional statement** or **implication** $p \implies q$ is the proposition "if $p$ then $q$", where $p$ is called the **hypothesis**, and $q$ is called the **conclusion** or **consequence**.

### Example of Implication

Let $p$ and $q$ be the following statements:
- $p$: "John did well in discrete mathematics" 
- $q$: "John will do well in the programming course"

The conditional statement $p \implies q$ can be written as follows:
"If John did well in discrete mathematics then John will do well in the programming course."

## Truth Table for Conditional Statements

The logical condition can be viewed as the reasoning from $p$ to $q$. For instance, if our reasoning is correct, which is represented by true implication, then if the hypothesis is true, the conclusion is also true. But if the reasoning is incorrect, which is represented by false implication, then if the hypothesis is true, then the conclusion is false.

| $p$ | $q$ | $p \implies q$ |
|-----|-----|---------------|
| T   | T   | T             |
| T   | F   | F             |
| F   | T   | T             |
| F   | F   | T             |

The truth table also shows us that it's true to think that if the hypothesis is false, then any conclusion can be implied whether it's false or true.

## Alternative Ways to Express Conditional Statements

We can express conditional statements in multiple ways. For example, let $p$ and $q$ be the following statements:
- $p$ is the proposition "It's sunny"
- $q$ is the proposition "John goes to the park"

The implication $p \implies q$ can be expressed in the following ways:
- If $p$ then $q$
- If $p$, $q$
- $p$ implies $q$
- $p$ only if $q$
- $q$ follows from $p$
- $p$ is sufficient for $q$
- $q$ unless not $p$
- $q$ is necessary for $p$

All of those expressions hold the same meaning which is, "If it's sunny, then John goes to the park."

Let's also note that the statement "$q$ is necessary for $p$" might be counter-intuitive in English, because it suggests that John's going into the park is the requirement for a sunny day. The best way to understand it is to implicitly read it as, "John's going to the park is a necessary consequence of a sunny day."

## Converse, Inverse, and Contrapositive

Now, let's move on to examine the meaning of converse, inverse, and contrapositive. Let $p$ and $q$ be propositions, and $A$ the conditional statement $p \implies q$.

Starting with the statement $p \implies q$, we can form some new conditional statements. We will examine three important statements:
- The proposition $q \implies p$ is the **converse** of $A$
- Proposition $\neg q \implies \neg p$ is the **contrapositive** of $A$
- The proposition $\neg p \implies \neg q$ is the **inverse** of $A$

### Example of Converse, Inverse, and Contrapositive

Let $p$ and $q$ be the following statements:
- $p$: "It's sunny"
- $q$: "John goes to the park"

And $A$ the statement $p \implies q$, which means, "If it's sunny, then John goes to the park."

- The **converse** of $A$ is: "If John goes to the park then it's sunny."
- The **contrapositive** of $A$ is: "If John doesn't go to the park, then it's not sunny."
- The **inverse** of $A$ is: "If it's not sunny, then John doesn't go to the park."

### Another Example

Let $p$ and $q$ be true propositions concerning a given integer $n$:
- $p$ is "$n$ has one digit"
- $q$ is "$n$ is less than 10"

Let's begin by writing the following statement using symbolic logic expression:
"If the integer $n$ has one digit, then it is less than 10."

The statement can be written simply as $p \implies q$.

Now, let's write its contrapositive using both symbolic logic and English:
- In symbolic logic expression: $\neg q \implies \neg p$
- In English: "If $n$ is greater than or equal to 10, then $n$ has more than one digit."

## Summary

In this lecture we have talked about another type of logical operation, logical implication. We began by defining an implication or conditional statements, then we built and examined its truth table, and finally, we looked at the converse, contrapositive, and inverse of an implication.
# Injective and Surjective Functions

In this lecture, we will explore two important properties of functions: **injectivity** and **surjectivity**.

### [Injective (One-to-One) Functions](images/injective_functions.JPG)

A function is called **injective** (or one-to-one) if **different inputs produce different outputs**. That is, for a function $f: A \rightarrow B$, if $f(a) = f(b)$ implies that $a = b$, then $f$ is injective.

Alternatively, to prove a function is *not* injective, we only need to find **two different inputs that have the same output**.

#### Example: Injective vs. Non-Injective Function
- **Function f:** Each element in the domain has a unique image. Thus, $f$ is injective.
- **Function g:** The inputs 2 and 4 map to the same output, and so do 1 and 3. Thus, $g$ is **not injective**.

---

## Proving a Function is Injective (Linear Function Example)

Let $f(x) = 2x + 3$, a linear function from $\mathbb{R} \rightarrow \mathbb{R}$. Let's prove that this function is injective using two approaches:

### **Approach 1: Assume Equal Outputs**
Let $a, b \in \mathbb{R}$, and assume $f(a) = f(b)$:

$$2a + 3 = 2b + 3 \Rightarrow 2a = 2b \Rightarrow a = b$$

Hence, the function is injective.

### **Approach 2: Assume Different Inputs**
Let $a, b \in \mathbb{R}$, and assume $a \neq b$. Then:

$$2a \neq 2b \Rightarrow 2a + 3 \neq 2b + 3 \Rightarrow f(a) \neq f(b)$$

Again, this confirms that $f$ is injective.

---

## Non-Injective Function Example: Quadratic Function

Let $f(x) = x^2$, defined from $\mathbb{R} \rightarrow \mathbb{R}$.

- $f(5) = 25$, and $f(-5) = 25$
- Different inputs produce the **same output**, so this function is **not injective**.

### Making It Injective:
If we **restrict the domain** of $f(x) = x^2$ to $\mathbb{R}^+$ (non-negative real numbers), the function becomes injective.

Let $a, b \in \mathbb{R}^+$, and assume $f(a) = f(b)$:

$$a^2 = b^2 \Rightarrow a = b \quad \text{(since both are positive)}$$

Thus, the function is injective on $\mathbb{R}^+$.

---

### [Surjective (Onto) Functions](images/surjective_functions.JPG)

A function $f: A \rightarrow B$ is called **surjective** (or onto) if **every element in the codomain $B$** has **at least one pre-image** in the domain $A$.

This means that the **range of the function is equal to the codomain**.

#### Example: Surjective vs. Non-Surjective Function
- **Function f:** Every element in the codomain has at least one pre-image in the domain. Hence, it's **surjective**.
- **Function g:** Elements 2 and 3 in the codomain have no pre-images. So, $g$ is **not surjective**.

---

## Proving a Function is Surjective (Linear Function Example)

Let $f(x) = 2x + 3$, defined from $\mathbb{R} \rightarrow \mathbb{R}$. Let's show it is surjective.

We want to prove: For any $y \in \mathbb{R}$, there exists $x \in \mathbb{R}$ such that:

$$f(x) = y \Rightarrow 2x + 3 = y \Rightarrow x = \frac{y - 3}{2}$$

Since $\frac{y - 3}{2} \in \mathbb{R}$, the function is **surjective**.

---

### [Non-Surjective Example: Quadratic Function]()

Let $f(x) = x^2$, defined from $\mathbb{R} \rightarrow \mathbb{R}$.

- Codomain: $\mathbb{R}$
- Range: $\mathbb{R}^+ \cup \{0\}$

Since **no negative number** in the codomain has a pre-image (e.g., $f(x) = -1$ has no solution in $\mathbb{R}$), this function is **not surjective**.

## [Summary](images/recap_or_summary.png)
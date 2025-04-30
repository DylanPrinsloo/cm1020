# **Summary and Academic Explanation of Bijections and Inverse Functions**

---

### 1. Definitions  

- **Injective (One‐to‐One):**  
  A function \(f\colon A\to B\) is *injective* if  
  \[
    \forall\,a_1,a_2\in A,\;f(a_1)=f(a_2)\;\Longrightarrow\;a_1=a_2.
  \]  
  Equivalently, distinct inputs produce distinct outputs.  

- **Surjective (Onto):**  
  A function \(f\colon A\to B\) is *surjective* if  
  \[
    \forall\,b\in B,\;\exists\,a\in A\text{ such that }f(a)=b.
  \]  
  Every element of the codomain has at least one pre‐image.  

- **Bijective (Invertible):**  
  A function is *bijective* precisely when it is both injective and surjective.  Equivalently, it establishes a one‐to‐one correspondence between \(A\) and \(B\).  Only bijections admit well‐defined inverses.  

---

### 2. Verifying Bijectivity by Proving Injectivity and Surjectivity  

Consider 
\[
  f(x) = 2x + 3,\quad f\colon \mathbb{R}\to\mathbb{R}.
\]

1. **Injectivity:**  
   - Suppose \(f(a) = f(b)\).  
   - Then \(2a + 3 = 2b + 3\).  
   - Subtracting 3 and dividing by 2 yields \(a = b\).  
   - Hence \(f\) is injective.

2. **Surjectivity:**  
   - Let \(y\in\mathbb{R}\).  Seek \(x\) such that \(f(x)=y\).  
   - Solve \(2x+3=y\) to obtain \(x = \tfrac{y-3}{2}\).  
   - Since \(\tfrac{y-3}{2}\in\mathbb{R}\), every \(y\) has a pre‐image.  
   - Hence \(f\) is surjective.

Because \(f\) is both injective and surjective, it is bijective.

---

### 3. Constructing the Inverse Function  

If \(f\colon A\to B\) is bijective, its *inverse* \(f^{-1}\colon B\to A\) is defined by
\[
  f^{-1}(y) = x
  \quad\Longleftrightarrow\quad
  f(x) = y.
\]
For \(f(x)=2x+3\), set \(y=f(x)\) and solve:
\[
  y = 2x + 3
  \quad\Longrightarrow\quad
  x = \frac{y-3}{2}.
\]
Thus
\[
  f^{-1}(y) \;=\;\frac{y-3}{2}, 
  \quad f^{-1}\colon \mathbb{R}\to\mathbb{R}.
\]

Verification of invertibility properties:
\[
  \bigl(f\circ f^{-1}\bigr)(y)
  = f\bigl(f^{-1}(y)\bigr)
  = f\!\Bigl(\tfrac{y-3}{2}\Bigr)
  = 2\cdot\tfrac{y-3}{2} + 3
  = y,
\]
\[
  \bigl(f^{-1}\circ f\bigr)(x)
  = f^{-1}\bigl(f(x)\bigr)
  = f^{-1}(2x+3)
  = \tfrac{(2x+3)-3}{2}
  = x.
\]
In each case, composition with the inverse yields the identity function.

---

### 4. Graphical Relationship  

- The graph of \(f\) and that of its inverse \(f^{-1}\) are **reflections** of one another across the line \(y = x\).  
- Concretely, if \((a,b)\) lies on the graph of \(f\), then \((b,a)\) lies on the graph of \(f^{-1}\).  

---

### 5. Illustrative Examples of Non‐Bijectivity  

- A function that omits some codomain values (fails surjectivity) cannot be inverted.  
- A function that maps two distinct domain elements to the same codomain point (fails injectivity) cannot be inverted.  

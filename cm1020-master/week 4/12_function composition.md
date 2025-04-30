# **Summary and Explanation of Function Composition and Its Non-Commutativity**

---  

### 1. Definition of Function Composition  
Given two functions  
\[
G: A \to B, 
\qquad
F: B \to C,
\]  
their **composition**, denoted \(F\circ G\), is the function  
\[
F\circ G : A \;\longrightarrow\; C
\]
defined by
\[
(F\circ G)(x) \;=\; F\bigl(G(x)\bigr)\quad \text{for all }x\in A.
\]

---

### 2. Two-Stage Evaluation Process  
To compute \((F\circ G)(x)\):  
1. **First stage**: apply \(G\) to the input \(x\), yielding \(G(x)\).  
2. **Second stage**: apply \(F\) to that intermediate result, i.e.\ compute \(F\bigl(G(x)\bigr)\).  

---

### 3. Concrete Example  
Let  
\[
G(x) = x^2, 
\quad 
F(u) = 2u.
\]  
Then for any real \(x\):
1. \(G(x) = x^2\).  
2. \(F\bigl(G(x)\bigr) = F(x^2) = 2\,(x^2) = 2x^2.\)  
Hence \((F\circ G)(x) = 2x^2\).

---

### 4. Visualization via Sets and Mappings  
- **Domain** \(A\): starting set of inputs.  
- **Intermediate codomain** \(B\): outputs of \(G\).  
- **Final codomain** \(C\): outputs of \(F\).  

An element \(a\in A\) is sent by \(G\) to \(b = G(a)\in B\), then by \(F\) to \(c = F(b)\in C\).  Thus \(F\circ G\) carries \(a\) directly to \(c\).  

---

### 5. Additional Numerical Example  
Define  
\[
G(x) = 3x + 2,
\quad
F(x) = 2x + 3,
\]
with both \(F,G : \mathbb{R}\to\mathbb{R}\).  For \(x=1\):
1. \(G(1) = 3\cdot1 + 2 = 5.\)  
2. \(F\bigl(G(1)\bigr) = F(5) = 2\cdot5 + 3 = 13.\)  
Therefore \((F\circ G)(1) = 13.\)

---

### 6. Non-Commutativity of Composition  
In general,  
\[
F\circ G \;\neq\; G\circ F.
\]  
For example, with \(G(x)=x^2\) and \(F(x)=2x\):  
- \((F\circ G)(x) = 2x^2\),  
- \((G\circ F)(x) = (2x)^2 = 4x^2\).  

Since \(2x^2 \neq 4x^2\) for nonzero \(x\), the order of application matters.  

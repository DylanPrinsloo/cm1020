# **Summary and Academic Explanation of the Floor and Ceiling Functions**

---

### 1. Definitions  

1. **Floor Function**  
   $$
     \lfloor x\rfloor = \max\{n\in\mathbb{Z}:n\le x\},
     \quad \lfloor\cdot\rfloor:\mathbb{R}\to\mathbb{Z}.
   $$  
   It returns the greatest integer not exceeding $x$.

2. **Ceiling Function**  
   $$
     \lceil x\rceil = \min\{n\in\mathbb{Z}:n\ge x\},
     \quad \lceil\cdot\rceil:\mathbb{R}\to\mathbb{Z}.
   $$  
   It returns the least integer not less than $x$.

---

### 2. Behavior on Examples  

- **Positive inputs**  
  - $\lfloor2.9\rfloor = 2,\;\lceil2.9\rceil = 3.$  
  - $\lfloor3\rfloor = 3,\;\lceil3\rceil = 3.$

- **Negative inputs**  
  - $\lfloor-2.5\rfloor = -3$ (since $-3\le -2.5< -2$),  
    $\lceil-2.5\rceil = -2$.  
  - $\lfloor-3\rfloor = -3,\;\lceil-3\rceil = -3.$

---

### 3. Graphical "Step" Structure  

Both functions exhibit a piecewise-constant ("step") graph:  
- On each interval $[n,n+1)$, $\lfloor x\rfloor = n$.  
- On each interval $(n-1,n]$, $\lceil x\rceil = n$.  

---

### 4. Key Properties  

1. **Integer Inputs:**  
   $\lfloor n\rfloor = n = \lceil n\rceil$ for all $n\in\mathbb{Z}$.

2. **Translation by an Integer:**  
   For any $n\in\mathbb{Z}$ and real $x$,
   $$
     \lfloor x + n\rfloor = \lfloor x\rfloor + n,
     \quad
     \lceil x + n\rceil = \lceil x\rceil + n.
   $$
   *Proof Sketch for the Floor:*  
   - Let $\lfloor x\rfloor = m$.  Then by definition  
     $m \le x < m+1$.  
   - Adding $n$ yields  
     $m+n \le x+n < m+n+1$.  
   - Hence $\lfloor x+n\rfloor = m+n = \lfloor x\rfloor + n.$

3. **Inequalities Relating Floor and Ceiling:**  
   $$
     \lfloor x\rfloor \le x \le \lceil x\rceil,
     \quad
     \lceil x\rceil = -\,\lfloor -x\rfloor.
   $$

---

### 5. Applications and Interpretation  

- **Rounding Down/Up:**  $\lfloor x\rfloor$ rounds $x$ down to the nearest integer, while $\lceil x\rceil$ rounds $x$ up.
- **Indexing and Partitioning:**  Frequently used to map continuous values into discrete bins or to index arrays.
- **In Theoretical Proofs:**  The translation property ($\lfloor x+n\rfloor=\lfloor x\rfloor+n$) simplifies arguments involving periodicity or integer shifts.
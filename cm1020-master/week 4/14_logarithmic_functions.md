# **Summary and Academic Explanation of Exponential and Logarithmic Functions**

---

### 1. Exponential Functions  

- **Definition**  
  An *exponential function* with base $b$ is  
  $$
    f(x) = b^x,\quad b>0,\;b\neq 1.
  $$  
  - **Domain:** $\mathbb{R}$.  
  - **Range:** $(0,\infty)$.  
  - **Key point:** Always passes through $(0,1)$, since $b^0=1$.  

- **Monotonicity**  
  - If $b>1$, $b^x$ is strictly increasing (exponential growth).  
  - If $0<b<1$, $b^x$ is strictly decreasing (exponential decay).  

---

### 2. Logarithmic Functions as Inverses  

- **Definition**  
  The *logarithm* base $b$ is the inverse of the exponential:
  $$
    y = \log_b(x) 
    \quad\Longleftrightarrow\quad
    x = b^y,
    \quad b>0,\;b\neq1.
  $$  
  - **Domain:** $(0,\infty)$.  
  - **Range:** $\mathbb{R}$.  
  - **Intercept:** $\bigl(1,0\bigr)$, since $\log_b(1)=0$.  

- **Inverse Relationship**  
  $$
    b^{\,\log_b(x)} = x,
    \quad
    \log_b\bigl(b^x\bigr) = x,
  $$  
  and graphically the curves of $b^x$ and $\log_b(x)$ reflect across the line $y=x$.

---

### 3. Conversion Between Forms  

- **Exponential $\leftrightarrow$ Logarithmic**  
  $$
    b^y = x 
    \quad\Longleftrightarrow\quad
    \log_b(x) = y.
  $$  
  *Example:* $3^4=81$ is equivalent to $\log_3(81)=4$.

---

### 4. Fundamental Logarithm Laws  

For all admissible $m,n>0$ and real $k$:
1. **Product Rule:**  
   $\displaystyle \log_b(mn)=\log_b(m)+\log_b(n).$
2. **Quotient Rule:**  
   $\displaystyle \log_b\!\bigl(\tfrac mn\bigr)=\log_b(m)-\log_b(n).$
3. **Power Rule:**  
   $\displaystyle \log_b\bigl(m^k\bigr)=k\,\log_b(m).$
4. **Special Values:**  
   $\displaystyle \log_b(1)=0,\quad \log_b(b)=1.$

*Sample computations:*  
- $\log_3(81)=\log_3(3^4)=4\log_3(3)=4$.  
- $\log_{10}(100)=\log_{10}(10^2)=2$.  
- $\log_3\bigl(\tfrac1{81}\bigr)=\log_3(3^{-4})=-4$.  

---

### 5. Graphical Behavior  

- **Base $b>1$:**  
  - Exponential $b^x$ grows from $(0,1)$ upward;  
  - Logarithm $\log_b(x)$ grows slowly, crossing $(1,0)$.  
- **Base $0<b<1$:**  
  - Exponential $b^x$ decays toward 0;  
  - Logarithm $\log_b(x)$ decreases, crossing $(1,0)$.  
- In every case, the two curves are symmetric about $y=x$.

---

### 6. The Natural Logarithm  

- **Definition:**  
  $\displaystyle \ln(x)=\log_e(x)$, where $e\approx2.71828$ is Euler's constant.  
- **Key properties:**  
  $\ln(1)=0,\;\ln(e)=1$, and $\ln(x)$ is strictly increasing on $(0,\infty)$.

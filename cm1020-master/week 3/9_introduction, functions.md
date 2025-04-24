### **1. Introduction to Functions**

- In everyday situations, many quantities depend on changes in other variables.  
  - Example: A plant’s growth depends on sunlight and rainfall.  
  - Example: A runner’s speed depends on time and distance.

- In mathematics, a **function** is a rule that describes how one quantity (the output) depends on another quantity (the input).

- **Definition**:  
  A function is a relation from a set of inputs to a set of outputs such that *each input is associated with exactly one output*.

- In computer programming, functions are fundamental units of logic that perform specific tasks. Most code written by programmers involves defining and using functions.

---

### **2. Mathematical Notation and Terminology**

- A function **f** from set **A** to set **B** is denoted as:  
  `f: A → B`  
  Meaning: for every element **x** in **A**, there is one corresponding element **f(x)** in **B**.

- **f(x) = y**  
  - **x** is called the **input** or **pre-image**  
  - **y** is the **output** or **image** of **x**

---

### **3. Function Properties and Definitions**

- **Domain (D_f)**: The set of all possible inputs (x-values).  
- **Co-domain (coD_f)**: The set that contains all potential outputs (y-values).  
- **Range (R_f)**: The actual set of outputs that the function maps to (a subset of the co-domain).

#### Example:
Let A = {“sea”, “sky”, “land”}  
Let B = {1, 2, 3, 4, 5, 6}

- Define f: A → B such that f(string) = number of characters in the string.

  - f(“sea”) = 3  
  - f(“land”) = 4  
  - f(“sky”) = 3

Then:
- **Domain** = A = {“sea”, “sky”, “land”}  
- **Co-domain** = B = {1, 2, 3, 4, 5, 6}  
- **Range** = {3, 4} (actual outputs)

---

### **4. Image and Pre-image**

- The **image** of an element x is f(x).  
- The **pre-image** of y is any x such that f(x) = y.

#### Example:
f(“on”) = 2  
Then:  
- 2 is the **image** of “on”  
- “on” is the **pre-image** of 2

If multiple elements of the domain map to the same output, the pre-image of that output is a **set** of those elements.

---

### **5. Examples of Functions**

#### Example 1:
Function f: Z → Z (Z = set of integers)  
f(x) = |x| (absolute value of x)

- **Domain**: Z  
- **Co-domain**: Z  
- **Range**: {x ∈ Z | x ≥ 0}  
- Pre-image of 1: {-1, 1}

#### Example 2:
Function g: R → R (R = set of real numbers)  
g(x) = x² + 1

- **Domain**: R  
- **Co-domain**: R  
- **Range**: {x ∈ R | x ≥ 1}  
- Pre-image of 5: {-2, 2}

---

### **6. What is Not a Function**

A relation is **not a function** if:

- An input has **no image** (i.e., not mapped to any output)  
- An input has **more than one image** (mapped to multiple outputs)

#### Example:
If a relation maps marks to students:
- 65 has no image → violates function rule  
- 62 maps to multiple students → violates uniqueness of output

But a relation mapping student names to unique exam marks **is** a function.

---

### **7. Summary**

- A function assigns each input exactly one output.
- Key components:
  - **Domain**: Set of inputs
  - **Co-domain**: Set of all possible outputs
  - **Range**: Set of actual outputs
  - **Image**: Output for a specific input
  - **Pre-image**: Input(s) that map to a specific output
- Functions must be well-defined: no input has more than one output.

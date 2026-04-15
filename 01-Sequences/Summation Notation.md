## Summations

From the sequence $\{a_n\}$, we use the notation:

$$\sum_{j=m}^{n} a_j, \quad \sum_{j=m}^{n} a_j, \quad \text{or} \quad \sum_{m \leq j \leq n} a_j$$

**Read as:** "the sum from $j = m$ to $j = n$ of $a_j$"

**Represents:** $a_m, a_{m+1}, \ldots, a_n$

$$\sum_{j=m}^{n} a_j = a_m + a_{m+1} + \cdots + a_n$$

---

## Notation

- **$j$** is called the **index of summation**
- The index runs through all integers starting with **lower limit $m$** and ending with **upper limit $n$**

---

## Example: Linear Combination

When $a$ and $b$ are real numbers:

$$\sum_{j=1}^{n} (ax_j + by_j) = a\sum_{j=1}^{n} x_j + b\sum_{j=1}^{n} y_j$$

where $x_1, x_2, \ldots, x_n$ and $y_1, y_2, \ldots, y_n$ are real numbers.

---

## Example: Sum of First 100 Terms

Express the sum of the first 100 terms of sequence $\{a_j\}$ where $a_j = \frac{1}{j}$ for $j = 1, 2, 3, \ldots$

**Solution:** The lower limit is 1, upper limit is 100:

$$\sum_{j=1}^{100} \frac{1}{j}$$

---

## Example: Evaluate $\sum_{j=1}^{5} j^2$

$$\sum_{j=1}^{5} j^2 = 1^2 + 2^2 + 3^2 + 4^2 + 5^2$$

$$= 1 + 4 + 9 + 16 + 25 = 55$$

---

## Example: Evaluate $\sum_{k=4}^{8} (-1)^k$

$$\sum_{k=4}^{8} (-1)^k = (-1)^4 + (-1)^5 + (-1)^6 + (-1)^7 + (-1)^8$$

$$= 1 + (-1) + 1 + (-1) + 1 = 1$$

---

## Shifting the Index

**Example:** Rewrite $\sum_{j=1}^{5} j^2$ with index running from 0 to 4

Let $k = j - 1$. Then:
- When $j = 1$: $k = 1 - 1 = 0$
- When $j = 5$: $k = 5 - 1 = 4$
- Term $j^2$ becomes $(k+1)^2$

$$\sum_{j=1}^{5} j^2 = \sum_{k=0}^{4} (k+1)^2$$

**Check:** Both sums equal $1 + 4 + 9 + 16 + 25 = 55$ ✓

---

## Double Summation

To evaluate: **expand the inner summation, then the outer summation**

$$\sum_{i=1}^{4} \sum_{j=1}^{3} ij = \sum_{i=1}^{4} (i + 2i + 3i)$$

$$= \sum_{i=1}^{4} 6i = 6 + 12 + 18 + 24 = 60$$

---

## Summation Over a Set

$$\sum_{s \in S} f(s)$$

Represents the sum of values $f(s)$ for all members $s$ of set $S$.

---

## Product Notation

The Greek capital letter pi, $\prod$, denotes a **product**.

$$\prod_{k=1}^{5} a_k = a_1 a_2 a_3 a_4 a_5$$

---

## Recursive Definition

If $m$ is any integer, then:

$$\prod_{k=m}^{m} a_k = a_m$$

$$\prod_{k=m}^{n} a_k = \left(\prod_{k=m}^{n-1} a_k\right) \cdot a_n \quad \text{for all integers } n > m$$

---

## Properties of Summations and Products

### 1. Summation of Union
$$\sum_{k=m}^{n} a_k + \sum_{k=m}^{n} b_k = \sum_{k=m}^{n} (a_k + b_k)$$

### 2. Generalized Distributive Law
$$c \sum_{k=m}^{n} a_k = \sum_{k=m}^{n} c \cdot a_k$$

### 3. Product of Products
$$\left(\prod_{k=m}^{n} a_k\right) \cdot \left(\prod_{k=m}^{n} b_k\right) = \prod_{k=m}^{n} (a_k \cdot b_k)$$

---

[[Sequences|← Back to Sequences]]
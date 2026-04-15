## Product Rule

Suppose that a procedure can be broken down into a sequence of two tasks. If there are $n_1$ ways to do the first task and for each of these ways of doing the first task, there are $n_2$ ways to do the second task, then there are $n_1 n_2$ ways to do the procedure.

---

### Example 1: Office Assignment

A new company with just two employees, Sanchez and Patel, rents a floor of a building with 12 offices. How many ways are there to assign different offices to these two employees?

**Solution:**  
The procedure consists of:
1. Assigning an office to Sanchez → 12 ways
2. Assigning an office to Patel (different from Sanchez's) → 11 ways

**By the product rule:**
$$12 \times 11 = 132 \text{ ways}$$

---

## Extended Product Rule

If a procedure can be broken down into a sequence of $n$ tasks, and there are:
- $n_1$ ways to do the first task
- $n_2$ ways to do the second task  
- ...
- $n_k$ ways to do the $k$-th task

Then there are $n_1 \times n_2 \times \cdots \times n_k$ ways to do the procedure.

**General form:**
$$|A_1 \times A_2 \times \cdots \times A_m| = |A_1| \cdot |A_2| \cdots |A_m|$$

---

## Counting Subsets of a Finite Set

Use the product rule to show that the number of different subsets of a finite set $S$ is $2^{|S|}$:

**Solution:**  
Let $S$ be a finite set. By the product rule, there are $2^{|S|}$ bit strings of length $|S|$.

Hence:
$$|P(S)| = 2^{|S|}$$

Each element can either be in the subset (1) or not in the subset (0), giving 2 choices per element.

---

## The Sum Rule

If a task can be done in one of $n_1$ ways or in one of $n_2$ ways, where **none of the set of $n_1$ ways is the same as any of the set of $n_2$ ways**, then there are $n_1 + n_2$ ways to do the task.

> **Key:** The sets of ways must be **disjoint** (no overlap).

---

## The Division Rule

There are $\frac{n}{d}$ ways to do a task if it can be done using a procedure that can be carried out in $n$ ways, and for every way $w$, exactly $d$ of the $n$ ways correspond to way $w$.

**Function form:**  
If $f$ is a function from $A$ to $B$ where $A$ and $B$ are finite sets, and for every value $y \in B$ there are exactly $d$ values $x \in A$ such that $f(x) = y$, then:

$$|B| = \frac{|A|}{d}$$

---

## The Pigeonhole Principle

If $k$ is a positive integer and $k + 1$ or more objects are placed into $k$ boxes, then there is at least one box containing two or more of the objects.

> **Simple version:** If you have more pigeons than pigeonholes, at least one hole must contain multiple pigeons.

---

## Permutations and Combinations

### Permutation

A **permutation** of a set of distinct objects is an ordered arrangement of these objects.

### $r$-Permutation

An ordered arrangement of $r$ elements of a set is called an **$r$-permutation**.

---

### Theorem 1: Counting $r$-Permutations

If $n$ is a positive integer and $r$ is an integer with $1 \leq r \leq n$, then there are:

$$P(n, r) = n(n-1)(n-2) \cdots (n-r+1)$$

$r$-permutations of a set with $n$ distinct elements.

> **Note:** $P(n, 0) = 1$ when $n$ is a nonnegative integer (exactly one way to order zero elements).

---

### Corollary 1

If $n$ and $r$ are integers with $0 \leq r \leq n$, then:

$$P(n, r) = \frac{n!}{(n-r)!}$$

---

## Combinations

### Definition

The number of $r$-combinations of a set with $n$ elements, where $n$ is a nonnegative integer and $r$ is an integer with $0 \leq r \leq n$, is denoted by:

$$C(n, r) \quad \text{or} \quad \binom{n}{r}$$

$\binom{n}{r}$ is called a **binomial coefficient**.

---

### Theorem 2: Formula for Combinations

$$C(n, r) = \frac{n!}{r!(n-r)!}$$

**Computing:**

$$C(n, r) = \frac{n!}{r!(n-r)!} = \frac{n(n-1) \cdots (n-r+1)}{r!}$$

Cancel out all terms in the larger factorial in the denominator from the numerator and denominator, then multiply all terms.

---

### Corollary 2: Symmetry

Let $n$ and $r$ be nonnegative integers with $r \leq n$. Then:

$$\binom{n}{r} = \binom{n}{n-r}$$

---

## Combinatorial Proofs

A **combinatorial proof** of an identity is a proof that uses counting arguments to prove that both sides of the identity count the same objects but in different ways, OR a proof based on showing that there is a bijection between the sets of objects counted by the two sides of the identity.

---

[[04-Permutations-Combinations/binomial-theorem|Next: Binomial Theorem →]]
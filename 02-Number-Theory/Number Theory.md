## Division

### Definition 1: Divisibility

If $a$ and $b$ are integers with $a \neq 0$, we say that **$a$ divides $b$** if there is an integer $c$ such that $b = ac$, or equivalently, if $\frac{b}{a}$ is an integer.

When $a$ divides $b$:
- $a$ is a **factor** or **divisor** of $b$
- $b$ is a **multiple** of $a$

**Notation:**
- $a \mid b$ denotes that $a$ divides $b$
- $a \nmid b$ denotes that $a$ does not divide $b$

---

### Theorem 1: Properties of Divisibility

Let $a, b, c$ be integers where $a \neq 0$. Then:

1. If $a \mid b$ and $a \mid c$, then $a \mid (b + c)$
2. If $a \mid b$, then $a \mid bc$ for all integers $c$
3. If $a \mid b$ and $b \mid c$, then $a \mid c$

---

### Corollary 1: Divisibility of Integer Combinations

If $a, b, c$ are integers where $a \neq 0$, such that $a \mid b$ and $a \mid c$, then:

$$a \mid (mb + nc) \quad \text{whenever } m, n \text{ are integers}$$

---

## Division Algorithm

When an integer is divided by a positive integer, there is a **quotient** and a **remainder**.

**Division Algorithm:**  
Let $a$ be an integer and $d$ a positive integer. Then there are **unique** integers $q$ and $r$ with $0 \leq r < d$ such that:

$$a = dq + r$$

---

### Definition 2: Division Terminology

In the equality $a = dq + r$:
- $d$ is the **divisor**
- $a$ is the **dividend**
- $q$ is the **quotient**
- $r$ is the **remainder**

**Notation:**
- $q = a \text{ div } d$
- $r = a \text{ mod } d$

---

## Modular Arithmetic

### Definition 3: Congruence

If $a$ and $b$ are integers and $m$ is a positive integer, then **$a$ is congruent to $b$ modulo $m$** if $m$ divides $a - b$.

**Notation:** $a \equiv b \pmod{m}$

We say $a \equiv b \pmod{m}$ is a **congruence** and $m$ is its **modulus** (plural: moduli).

If $a$ and $b$ are not congruent modulo $m$: $a \not\equiv b \pmod{m}$

---

### Notation Note

- $a \equiv b \pmod{m}$ represents a **set of integers**
- $a \bmod m = b$ represents a **function**

---

### Theorem 3

Let $a$ and $b$ be integers, and $m$ a positive integer. Then:

$$a \equiv b \pmod{m} \iff a \bmod m = b \bmod m$$

**Meaning:** $a \equiv b \pmod{m}$ if and only if $a$ and $b$ have the **same remainder** when divided by $m$.

---

### Example: Congruence Check

**Determine whether $17 \equiv 5 \pmod{6}$ and whether $24 \equiv 14 \pmod{6}$**

- $6$ divides $17 - 5 = 12$ → $17 \equiv 5 \pmod{6}$ ✓
- $24 - 14 = 10$ is not divisible by $6$ → $24 \not\equiv 14 \pmod{6}$ ✗

---

### Theorem 4

Let $m$ be a positive integer. The integers $a$ and $b$ are congruent modulo $m$ if and only if there is an integer $k$ such that:

$$a = b + km$$

---

### Congruence Class

The set of all integers congruent to an integer $a$ modulo $m$ is called the **congruence class of $a$ modulo $m$**.

---

### Theorem 5: Arithmetic with Congruences

Let $m$ be a positive integer. If $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, then:

$$a + c \equiv b + d \pmod{m}$$
$$ac \equiv bd \pmod{m}$$

---

### Example

Because $7 \equiv 2 \pmod{5}$ and $11 \equiv 1 \pmod{5}$:

$$18 = 7 + 11 \equiv 2 + 1 = 3 \pmod{5}$$
$$77 = 7 \cdot 11 \equiv 2 \cdot 1 = 2 \pmod{5}$$

---

### Corollary 2: Modular Addition and Multiplication

Let $m$ be a positive integer and let $a, b$ be integers. Then:

$$(a + b) \bmod m = ((a \bmod m) + (b \bmod m)) \bmod m$$

$$ab \bmod m = ((a \bmod m)(b \bmod m)) \bmod m$$

---

## Arithmetic Modulo $m$

Operations on $\mathbb{Z}_m = \{0, 1, \ldots, m-1\}$:

**Addition modulo $m$:**
$$a +_m b = (a + b) \bmod m$$

**Multiplication modulo $m$:**
$$a \cdot_m b = (a \cdot b) \bmod m$$

---

### Example: Modulo 11

Find $7 +_{11} 9$ and $7 \cdot_{11} 9$

**Solution:**
$$7 +_{11} 9 = (7 + 9) \bmod 11 = 16 \bmod 11 = 5$$

$$7 \cdot_{11} 9 = (7 \cdot 9) \bmod 11 = 63 \bmod 11 = 8$$

Therefore: $7 +_{11} 9 = 5$ and $7 \cdot_{11} 9 = 8$

---

## Primes and Greatest Common Divisors

### Definition 1: Prime Numbers

An integer $p > 1$ is called **prime** if the only positive factors of $p$ are $1$ and $p$.

A positive integer $> 1$ that is not prime is called **composite**.

---

### Theorem 1: Fundamental Theorem of Arithmetic

Every integer greater than 1 can be written **uniquely** as a prime or as the product of two or more primes, where the prime factors are written in order of nondecreasing size.

---

### Trial Division

### Theorem 2

If $n$ is a composite integer, then $n$ has a prime divisor less than or equal to $\sqrt{n}$.

---

### Theorem 4: Prime Number Theorem

The ratio of the number of primes not exceeding $x$ and $\frac{x}{\ln x}$ approaches 1 as $x$ grows without bound.

(Here $\ln x$ is the natural logarithm of $x$)

---

## Greatest Common Divisors and Least Common Multiples

### Definition 2: GCD

Let $a$ and $b$ be integers, not both zero. The largest integer $d$ such that $d \mid a$ and $d \mid b$ is called the **greatest common divisor** of $a$ and $b$.

**Notation:** $\gcd(a, b)$

---

### Example

What is $\gcd(24, 36)$?

Positive common divisors of 24 and 36: $1, 2, 3, 4, 6, 12$

$$\gcd(24, 36) = 12$$

---

### Definition 3: Relatively Prime

The integers $a$ and $b$ are **relatively prime** if $\gcd(a, b) = 1$.

---

### Definition 4: Pairwise Relatively Prime

The integers $a_1, a_2, \ldots, a_n$ are **pairwise relatively prime** if:

$$\gcd(a_i, a_j) = 1 \quad \text{whenever } 1 \leq i < j \leq n$$

---

### Example

Are 10, 17, and 21 pairwise relatively prime? Are 10, 19, and 24?

$$\gcd(10, 17) = 1, \quad \gcd(10, 21) = 1, \quad \gcd(17, 21) = 1$$

Therefore, 10, 17, and 21 **are** pairwise relatively prime. ✓

---

### Definition 5: LCM

The **least common multiple** of positive integers $a$ and $b$ is the smallest positive integer that is divisible by both $a$ and $b$.

**Notation:** $\text{lcm}(a, b)$

---

### Theorem 5

Let $a$ and $b$ be positive integers. Then:

$$ab = \gcd(a, b) \cdot \text{lcm}(a, b)$$

---

## The Euclidean Algorithm

### Lemma 1

Let $a = bq + r$ where $a, b, q, r$ are integers. Then:

$$\gcd(a, b) = \gcd(b, r)$$

---

### Theorem 6: Bézout's Theorem

If $a$ and $b$ are positive integers, then there exist integers $s$ and $t$ such that:

$$\gcd(a, b) = sa + tb$$

---

### Definition 6: Bézout Coefficients

If $a$ and $b$ are positive integers, then integers $s$ and $t$ such that $\gcd(a, b) = sa + tb$ are called **Bézout coefficients** of $a$ and $b$.

The equation $\gcd(a, b) = sa + tb$ is called **Bézout's identity**.

---

### Lemma 2

If $a, b, c$ are positive integers such that $\gcd(a, b) = 1$ and $a \mid bc$, then $a \mid c$.

---

### Lemma 3

If $p$ is prime and $p \mid a_1 a_2 \cdots a_n$ where each $a_i$ is an integer, then $p \mid a_i$ for some $i$.

---

### Theorem 7: Linear Congruence Cancellation

Let $m$ be a positive integer and let $a, b, c$ be integers. If:

$$ac \equiv bc \pmod{m} \quad \text{and} \quad \gcd(c, m) = 1$$

then:

$$a \equiv b \pmod{m}$$

---

[[03-Counting/counting|Next: Counting →]]
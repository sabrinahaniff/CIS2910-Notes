## The Binomial Theorem

Let $x$ and $y$ be variables, and let $n$ be a nonnegative integer. Then:

$$(x + y)^n = \sum_{j=0}^{n} \binom{n}{j} x^{n-j} y^j$$

**Expanded form:**

$$(x + y)^n = \binom{n}{0}x^n + \binom{n}{1}x^{n-1}y + \cdots + \binom{n}{n-1}xy^{n-1} + \binom{n}{n}y^n$$

---

## Corollaries

### Corollary 1

Let $n$ be a nonnegative integer. Then:

$$\sum_{k=0}^{n} \binom{n}{k} = 2^n$$

**Proof:** Set $x = 1$ and $y = 1$ in the binomial theorem.

---

### Corollary 2

Let $n$ be a positive integer. Then:

$$\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0$$

**Proof:** Set $x = -1$ and $y = 1$ in the binomial theorem.

**This implies:**

$$\binom{n}{0} + \binom{n}{2} + \binom{n}{4} + \cdots = \binom{n}{1} + \binom{n}{3} + \binom{n}{5} + \cdots$$

(The sum of binomial coefficients at even positions equals the sum at odd positions)

---

### Corollary 3

Let $n$ be a nonnegative integer. Then:

$$\sum_{k=0}^{n} 2^k \binom{n}{k} = 3^n$$

**Proof:** Set $x = 1$ and $y = 2$ in the binomial theorem.

The LHS is the expansion of $(1 + 2)^n$.

---

## Pascal's Triangle & Identity

### Pascal's Identity

Let $n$ and $k$ be positive integers with $n \geq k$. Then:

$$\binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}$$

This identity is the basis for **Pascal's Triangle**.

---

## Vandermonde's Identity

Let $m$, $n$, and $r$ be nonnegative integers with $r$ not exceeding either $m$ or $n$. Then:

$$\binom{m+n}{r} = \sum_{k=0}^{r} \binom{m}{r-k} \binom{n}{k}$$

---

### Corollary 4

If $n$ is a nonnegative integer, then:

$$\binom{2n}{n} = \sum_{k=0}^{n} \binom{n}{k}^2$$

---

## Theorem 4: Bit String Identity

Let $n$ and $r$ be nonnegative numbers with $r \leq n$. Then:

$$\binom{n+1}{r+1} = \sum_{j=r}^{n} \binom{j}{r}$$

This counts the number of bit strings of length $n+1$ containing exactly $r+1$ ones.

---

## Example Problems

### Example 1: Card Hand

What is the probability of selecting a hand using a deck of cards of A, K, Q, J, 10?

- 52 cards in a deck
- 4 of each type / 4 suits
- 13 of each suit

**Method 1:**

$$52 \cdot \frac{4}{51} \cdot \frac{4}{50} \cdot \frac{4}{49} \cdot \frac{4}{48}$$

**Method 2:**

$$\frac{\binom{4}{1} \binom{4}{1} \binom{4}{1} \binom{4}{1} \binom{4}{1}}{\binom{52}{5}} = \frac{1024}{2598960} \approx 0.00394$$

---

### Example 2: Full House

What is the probability the hand contains a full house?  
(3 of one kind and 2 of another)

$$\frac{\binom{13}{2} \binom{4}{3} \binom{4}{2}}{\binom{52}{5}} = \frac{13 \cdot 12 \cdot 4 \cdot 6}{2598960} \approx 0.00144$$

Alternative:

$$\frac{\binom{13}{1} \binom{4}{3} \binom{12}{1} \binom{4}{2}}{\binom{52}{5}} \approx 0.00144$$

---

### Example 3: Bit String

A sequence of 10 bits is randomly generated. What is the probability at least one of these bits is zero?

$$P(\text{at least 1 zero}) = 1 - P(\text{no zeros})$$

$$= 1 - \frac{1}{2^{10}} = 1 - \frac{1}{1024} = \frac{1023}{1024}$$

Each bit is either 0 or 1 with equal probability $\frac{1}{2}$.

---

### Example 4: Divisibility

What is the probability that a positive integer not exceeding 100 is divisible by either 2 or 5?

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

$$P(2 \cup 5) = \frac{50}{100} + \frac{20}{100} - \frac{10}{100} = \frac{60}{100} = 0.6$$

- Divisible by 2: 50 numbers
- Divisible by 5: 20 numbers  
- Divisible by both (10): 10 numbers

---

[[05-Probability/discrete-probability|Next: Discrete Probability →]]
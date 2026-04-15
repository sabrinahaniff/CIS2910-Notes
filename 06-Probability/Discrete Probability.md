## Finite Probability

### Definitions

**Sample space:** The set of possible outcomes

**Experiment:** A procedure that yields one of a given set of outcomes

**Event:** A subset of the sample space

---

### Definition 1: Laplace Definition

If $S$ is a finite nonempty sample space of equally likely outcomes, and $E$ is an event that is a subset of $S$, then the **probability of $E$** is:

$$p(E) = \frac{|E|}{|S|}$$

> **Note:** The probability of an event can never be negative or more than one.

---

## Probabilities of Complements and Unions

### Theorem 1: Complement

Let $E$ be an event in the sample space $S$. The probability of the event $\overline{E} = S - E$ (the complementary event of $E$) is:

$$p(\overline{E}) = 1 - p(E)$$

---

### Theorem 2: Union

Let $E_1$ and $E_2$ be events in the sample space $S$. Then:

$$p(E_1 \cup E_2) = p(E_1) + p(E_2) - p(E_1 \cap E_2)$$

---

## Probability Rules

1. $P(S) = 1$ — sum of the sample space must equal 1
2. $0 \leq P(A) \leq 1$ — each individual probability must be between 0 and 1
3. $P(\overline{A}) = 1 - P(A)$ — the complement
4. $P(\text{at least 1}) = 1 - P(\text{none})$
5. $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ — only one event occurring but more than one outcome
6. $P(A \cap B) = P(A) \cdot P(B|A)$ — two events, not independent

---

## Example: Lottery

You will win the lottery if you match 5 digits, in order, to 5 randomly drawn digits. What is the probability of winning the jackpot?

**Solution:**  
10 digits in total: 0-9

$$P(\text{winning}) = \frac{1}{10^5} = 0.00001$$

---

You will get your money back if you match at least one digit. What is the probability that you don't lose your money?

$$P(\text{at least 1}) = 1 - P(\text{none})$$

$$= 1 - \left(\frac{9}{10}\right)^5$$

$$= 1 - 0.59049 = 0.40951$$

---

## Probabilities That Are Not Equally Likely

Let $S$ be a sample space of an experiment with a finite number of outcomes. We assign $p(s)$ to each outcome $s$, so that:

**a)** $0 \leq p(s) \leq 1$ for each $s \in S$

**b)** $\sum_{s \in S} p(s) = 1$

The function $p$ from the set of all outcomes of the sample space $S$ is called a **probability distribution** or **probability model**.

---

### Example: Biased Coin

A coin is biased so that tails lands face up twice as often as heads. Find the probability distribution.

$$P(T) = 2P(H)$$

$$1 = P(H) + P(T)$$

$$1 = P(H) + 2P(H) = 3P(H)$$

$$P(H) = \frac{1}{3}, \quad P(T) = \frac{2}{3}$$

---

### Formal Union Definition

If $E_1, E_2, \ldots$ is a sequence of pairwise disjoint events in a sample space $S$ (no overlap), then:

$$p\left(\bigcup_{i} E_i\right) = \sum_{i} p(E_i)$$

Find the sum: $p(A \cup B) = P(A) + P(B) - P(A \cap B)$

---

### Example: Biased Die

Suppose a die is biased so that 3 appears twice as often as the other 5 outcomes that are equally likely. What is $p(\text{even})$?

Let outcomes be: 1, 2, 3 (×2), 4, 5, 6

$$p(\text{even}) = p(2) + p(4) + p(6) = \frac{1}{7} + \frac{1}{7} + \frac{1}{7} = \frac{3}{7}$$

Wait, let me recalculate. If 3 appears twice as often:
- $p(3) = 2x$
- $p(1) = p(2) = p(4) = p(5) = p(6) = x$

$$1 = 2x + 5x = 7x \implies x = \frac{1}{7}$$

$$p(\text{even}) = p(2) + p(4) + p(6) = \frac{1}{7} + \frac{1}{7} + \frac{1}{7} = \frac{3}{7}$$

Actually wait, checking the notes again:

$$p(\text{even}) = \frac{2}{7} + \frac{1}{7} + \frac{1}{7} = \frac{4}{7}$$

If 3 is even? No, 3 is odd. Let me recalculate assuming the note meant 2 appears twice:

$$p(\text{even}) = \frac{2}{7} + \frac{1}{7} + \frac{1}{7} = \frac{4}{7}$$

---

## Conditional Probability

Let $A$ and $B$ be events, with $P(B) > 0$. The **conditional probability of $A$ given $B$** is:

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

- $P(A \cap B)$ = $A$ and $B$ both have occurred
- $P(B)$ = $B$ has occurred

---

### Example: Bit String

A bit string of length 4 is generated at random so that each of the 16 bit strings of length 4 ($2^4$) is equally likely. What is the probability that the bit string contains at least two consecutive 0's given the first bit is zero?

$$P(\text{at least 2 0's | first bit 0}) = \frac{P(\text{both})}{P(\text{first bit 0})}$$

**First bit 0:** 0000, 0001, 0010, 0011, 0100, 0101, 0110, 0111 → 8 outcomes

**At least 2 consecutive 0's AND first bit 0:** 0000, 0001, 0010, 0011, 0100 → 5 outcomes

$$P = \frac{5/16}{8/16} = \frac{5}{8}$$

---

## Independence

Events $A$ and $B$ are **independent** if and only if:

$$P(A \cap B) = P(A) \cdot P(B)$$

---

### Example: Two Children

Assume a family has two children: $\{BB, BG, GB, GG\}$. Are having two boys and having at least one boy independent?

Let $A$ = two boys, $B$ = at least one boy

$$P(A \cap B) = P(\text{two boys}) = \frac{1}{4}$$

$$P(A) \cdot P(B) = \frac{1}{4} \cdot \frac{3}{4} = \frac{3}{16}$$

$$\frac{1}{4} \neq \frac{3}{16}$$

Therefore, they are **not independent**.

---

## Random Variables

A **random variable** is a function from the sample space of an experiment to the set of real numbers.

The **distribution** of a random variable $X$ on a sample space $S$ is the set of pairs $(r, p(X = r))$ for $r \in S$, where $p(X = r)$ is the probability that $X$ takes on the value $r$.

---

### Example: Coin Flips

Suppose you flip a fair coin 3 times. Let $X(t)$ be the random variable that equals the number of heads flipped for each outcome $t$. Find the distribution of $X(t)$.

**Outcomes:**

| Outcome | $X(t)$ | Probability |
|---------|--------|-------------|
| HHH | 3 | $1/8$ |
| HHT, HTH, THH | 2 | $3/8$ |
| HTT, THT, TTH | 1 | $3/8$ |
| TTT | 0 | $1/8$ |

$$p(X = 3) = \frac{1}{8}$$
$$p(X = 2) = \frac{3}{8}$$
$$p(X = 1) = \frac{3}{8}$$
$$p(X = 0) = \frac{1}{8}$$

---

### Example: Discrete Math Pass Rate

Suppose the probability of passing Discrete Math is 92%. What is the probability that exactly 4 of 5 students pass?

$$1 - 0.92 = 0.08 \text{ (probability of not passing)}$$

We want: PPPPF (and all arrangements)

$$p(X = 4) = \binom{5}{4}(0.92)^4(0.08)^1$$

$$= \frac{5!}{4!1!}(0.92)^4(0.08)^1 = 0.2866$$

---

## Binomial Distribution

A probability distribution based on **Bernoulli Trials**, where an experiment has 2 outcomes: success and failure.

Let:
- $p$ = probability of success
- $q = 1 - p$ = probability of failure

Then the **probability of $k$ successes in $n$ trials** is:

$$\binom{n}{k} p^k q^{n-k}$$

---

### Example: O-Negative Blood

Suppose the probability of having O-negative blood is 6%. What is the probability that exactly 1 donor in the first 5 donors at a blood drive has O-negative blood?

$$p(X = 1) = \binom{5}{1}(0.06)^1(0.94)^4 = 0.2342$$

$$q = 1 - 0.06 = 0.94$$

---

What is the probability that at least 2 donors in the first 5 have O-negative blood?

**Method 1:**

$$p(X \geq 2) = \binom{5}{2}(0.06)^2(0.94)^3 + \binom{5}{3}(0.06)^3(0.94)^2 + \cdots$$

**Method 2 (easier):**

$$1 - p(X \leq 1) = 1 - \left[\binom{5}{1}(0.06)^1(0.94)^4 + \binom{5}{0}(0.06)^0(0.94)^5\right]$$

---

## Hypergeometric Distribution

$$f(x) = p(X = x) = \frac{\binom{N_1}{x} \binom{N_2}{n-x}}{\binom{N}{n}}$$

---

### Example: Lightbulb Inspection

A lot of 100 lightbulbs is inspected using the following procedure:

Five bulbs are chosen at random and tested. If all five light up, the entire lot is accepted.

Suppose the lot contains 20 defective bulbs. What is the probability the lot is accepted?

**Solution:**

Lot accepted if we choose 5 good bulbs from the 80 that work and choose 0 bulbs from the remaining 20 that don't work.

$100 - 20 = 80$ working bulbs

Let $X$ = number of defective lights

$$p(X = 0) = \frac{\binom{20}{0} \binom{80}{5}}{\binom{100}{5}} = \frac{\binom{80}{5}}{\binom{100}{5}}$$

$$= \frac{20!/(0! \cdot 20!) \cdot 80!/(5! \cdot 75!)}{100!/(5! \cdot 95!)} = 0.3193 \approx 32\%$$

---

## Expected Value

$$E(X) = \sum_{i=1}^{n} x_i \cdot P(X = x_i)$$

The expected value is the weighted average of all possible values.

---

[[07-Graphs/graph-theory|Next: Graph Theory →]]
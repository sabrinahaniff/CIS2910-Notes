# Practice Midterm (Sections 5.1 - 5.2)

## Mathematical Induction

We show that $P(n)$ is true for every positive integer $n$, where $P(n)$ is the statement that we can reach the $n$-th rung of the ladder.

---

## Principle of Mathematical Induction

To prove that $P(n)$ is true for all positive integers $n$, where $P(n)$ is a propositional function, we complete **two steps**:

### Basis Step
Verify that $P(1)$ is true.

### Inductive Step  
Show that the conditional statement $P(k) \to P(k+1)$ is true for all positive integers $k$.

---

## Completing the Inductive Step

1. **Assume** that $P(k)$ is true for an arbitrary positive integer $k$ and show that under this assumption, $P(k+1)$ must also be true.

2. The assumption that $P(k)$ is true is called the **inductive hypothesis**.

---

## Example Proof Structure

**For all** $n \geq b$, $P(n)$ for a fixed integer $b$.

### Basis Step:
$P(b)$ is true: $P(1)$ is true (train stops at the first station)

### Inductive Step:
Assume $P(k)$ is true for an arbitrary fixed integer $k \geq b$.

Since $P(1)$ is true, then $P(k)$ is true (the train stops at the $k$-th station), and if $P(k)$ is true, $P(k+1)$ is true (the train stops at the $(k+1)$-th station).

---

[[Sequences|← Back to Sequences]] | [[06-Probability/discrete-probability|Next: Probability →]]
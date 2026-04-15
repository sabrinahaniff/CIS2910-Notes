##Sequences

> A sequence is a **discrete structure** used to represent an ordered list.
> - "Discrete" = not continuous

## Definition

A **sequence** is a function from a subset of the set of integers (usually either $\{0, 1, 2, \ldots\}$ or $\{1, 2, 3, \ldots\}$) to a set $S$.

**Notation:**
- $a_n$ denotes the image of the integer $n$
- $a_n$ is called a **term** of the sequence
- $\{a_n\}$ describes the sequence (represents an individual term)

We describe sequences by listing the terms in order of increasing subscripts.

---

## Examples

**Finite sequence with 5 terms:**
$$1, 2, 3, 5, 8$$

**Infinite sequence:**
$$1, 3, 9, 27, 81, \ldots, 3^n, \ldots$$

---

### Example: $a_n = \frac{1}{n}$

The list of terms $a_1, a_2, a_3, a_4, \ldots$ starts with:
$$1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \ldots$$

---

## Geometric Progression

A **geometric progression** is a sequence of the form:
$$a, ar, ar^2, \ldots, ar^n, \ldots$$

where:
- $a$ = initial term (real number)
- $r$ = common ratio (real number)

> **Remark:** A geometric progression is a discrete analogue of the exponential function $f(x) = ar^x$

### Examples

| Sequence | Formula | Initial term $a$ | Common ratio $r$ | First 5 terms |
|----------|---------|------------------|------------------|---------------|
| $\{b_n\}$ | $b_n = (-1)^n$ | 1 | -1 | $1, -1, 1, -1, 1, \ldots$ |
| $\{c_n\}$ | $c_n = 2 \cdot 5^n$ | 2 | 5 | $2, 10, 50, 250, 1250, \ldots$ |
| $\{d_n\}$ | $d_n = 6 \cdot \left(\frac{1}{3}\right)^n$ | 6 | $\frac{1}{3}$ | $6, 2, \frac{2}{3}, \frac{2}{9}, \frac{2}{27}, \ldots$ |

---

## Arithmetic Progression

An **arithmetic progression** is a sequence of the form:
$$a, a+d, a+2d, \ldots, a+nd, \ldots$$

where:
- $a$ = initial term (real number)
- $d$ = common difference (real number)

> **Remark:** An arithmetic progression is a discrete analogue of the linear function $f(x) = dx + a$

### Examples

**Sequence** $\{s_n\}$ with $s_n = -1 + 4n$:
- Initial term: $-1$
- Common difference: $4$
- Starting at $n=0$: $-1, 3, 7, 11, \ldots$

**Sequence** $\{t_n\}$ with $t_n = 7 - 3n$:
- Initial term: $7$
- Common difference: $-3$
- Starting at $n=0$: $7, 4, 1, -2, \ldots$

---

## Strings (Finite Sequences)

A **string** is denoted by $a_1a_2\ldots a_n$

**Length of a string** = number of terms

**Empty string** $\lambda$ = string with no terms (length zero)

**Example:** The string "abcd" has length 4.

---

## Recurrence Relations

A **recurrence relation** for sequence $\{a_n\}$ is an equation that expresses $a_n$ in terms of one or more previous terms: $a_0, a_1, \ldots, a_{n-1}$

- Valid for all integers $n \geq n_0$ (where $n_0$ is a nonnegative integer)
- A recurrence relation **recursively defines** a sequence

**Solution:** A sequence is a solution if its terms satisfy the recurrence relation.

**Initial conditions:** Specify the terms that precede the first term where the recurrence relation takes effect.

### Example 1

Let $\{a_n\}$ satisfy:
- Recurrence relation: $a_n = a_{n-1} + 3$ for $n = 1, 2, 3, \ldots$
- Initial condition: $a_0 = 2$

Find $a_1, a_2, a_3$:

$$a_1 = a_0 + 3 = 2 + 3 = 5$$
$$a_2 = a_1 + 3 = 5 + 3 = 8$$
$$a_3 = a_2 + 3 = 8 + 3 = 11$$

### Example 2

Let $\{a_n\}$ satisfy:
- Recurrence relation: $a_n = a_{n-1} - a_{n-2}$ for $n = 2, 3, 4, \ldots$
- Initial conditions: $a_0 = 3, a_1 = 5$

Find $a_2, a_3$:

$$a_2 = a_1 - a_0 = 5 - 3 = 2$$
$$a_3 = a_2 - a_1 = 2 - 5 = -3$$

---

## The Fibonacci Sequence

The **Fibonacci sequence** $f_0, f_1, f_2, \ldots$ is defined by:
- Initial conditions: $f_0 = 0, f_1 = 1$
- Recurrence relation: $f_n = f_{n-1} + f_{n-2}$ for $n = 2, 3, 4, \ldots$

**First terms:**
$$f_2 = f_1 + f_0 = 1 + 0 = 1$$
$$f_3 = f_2 + f_1 = 1 + 1 = 2$$
$$f_4 = f_3 + f_2 = 2 + 1 = 3$$
$$f_5 = f_4 + f_3 = 3 + 2 = 5$$
$$f_6 = f_5 + f_4 = 5 + 3 = 8$$

---

## Solving Recurrence Relations

We solve a recurrence relation by finding an **explicit formula** (closed formula) for the terms.

### Example: Factorial Sequence

$$a_n = n! \quad \text{for } n = 1, 2, 3, \ldots$$

Since $n! = n \cdot (n-1)!$, we have:
- Recurrence relation: $a_n = n \cdot a_{n-1}$
- Initial condition: $a_1 = 1$

---

## Links

- [[summation-notation|Summation Notation →]]
- [[01-sequences/practice-problems|Practice Problems →]]

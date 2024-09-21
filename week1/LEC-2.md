# Measuring Time Efficiency of Algorithms

We measure the time efficiency of algorithms only up to an order of magnitude. Thus, we express the running time as a function \( t(n) \) of the input size \( n \), but we ignore constants. We only say that \( t(n) \) is proportional to \( n^2 \) or \( n \log n \) or \( 2^n \).

## Comparing Running Times

To compare the running times across algorithms, we use the concept of an upper bound denoted by **Big O**. A function \( g(n) \) is an upper bound for another function \( t(n) \) if, beyond some point, \( g(n) \) dominates \( t(n) \). We allow ourselves a constant \( c \) such that:

\[
t(n) \leq c \cdot g(n) \quad \text{for } n \geq n_0
\]

### Example 1

Suppose \( t(n) = 100n + 5 \). We claim that \( t(n) \) is **Big O** of \( n^2 \):

- For \( n \geq 5 \):
  \[
  100n + 5 \leq 101n
  \]
- Now, since \( n^2 \) is greater than \( n \) for \( n \geq 1 \):
  \[
  101n \leq 101n^2
  \]

Thus, with \( n_0 = 5 \) and \( c = 101 \), we have established that \( 100n + 5 \) is **Big O** of \( n^2 \).

### Example 2

For \( t(n) = 100n^2 + 20n + 5 \):

- For \( n \geq 1 \):
  \[
  100n^2 + 20n + 5 \leq 125n^2
  \]
  
Thus, we can say \( t(n) \) is **Big O** of \( n^2 \).

## Establishing Not Big O

To show that \( n^3 \) is not **Big O** of \( n^2 \):

Assume \( n^3 \leq c \cdot n^2 \) for some \( n_0 \). For \( n = c \):
\[
c^3 \leq c^3
\]
However, for \( n = c + 1 \):
\[
(c + 1)^3 > c(c + 1)^2
\]

Thus, \( n^3 \) is not **Big O** of \( n^2 \).

## Useful Facts about Big O

If \( f_1 \) is **Big O** of \( g_1 \) and \( f_2 \) is **Big O** of \( g_2 \), then:
\[
f_1 + f_2 \text{ is dominated by } \max(g_1, g_2)
\]

### Example of Algorithm Phases

For an algorithm with phases \( A \) and \( B \) taking time \( \text{Big O}(g_A) \) and \( \text{Big O}(g_B) \), the overall running time is:
\[
\text{Big O}(\max(g_A, g_B))
\]

## Lower Bound: Omega

A function \( t(n) \) is **Omega** of \( g(n) \) if:
\[
t(n) \geq c \cdot g(n) \quad \text{for } n \geq n_0
\]

### Example

For \( n^3 \) and \( n^2 \):
- Since \( n^3 \geq n^2 \) for \( n \geq 1 \), \( n^3 \) is **Omega** of \( n^2 \).

## Matching Upper and Lower Bounds: Theta

A function \( t(n) \) is **Theta** of \( g(n) \) if it is both:
- **Big O** of \( g(n) \)
- **Omega** of \( g(n) \)

### Example

For \( n(n-1)/2 \):
- Upper bound: 
  \[
  n(n-1)/2 < \frac{1}{2} n^2
  \]
- Lower bound:
  \[
  n(n-1)/2 > \frac{1}{4} n^2
  \]

Thus, \( n(n-1)/2 \) is **Theta** of \( n^2 \).

## Summary

- \( f(n) \) is **Big O** of \( g(n) \) if \( g(n) \) dominates \( f(n) \).
- Establishing upper and lower bounds helps in analyzing algorithms.
- **Theta** indicates that two functions are of the same order of magnitude.

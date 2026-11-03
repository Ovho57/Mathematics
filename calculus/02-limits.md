# 02 — Limits

A limit describes the value a function approaches as its input approaches a particular number.

\[
\lim_{x\to a}f(x)=L
\]

means that as (x) gets close to (a), (f(x)) gets close to (L).

## Direct substitution

For many functions:
\[
\lim_{x\to2}(x^2+3x)=4+6=10
\]

## Why (0/0) is not an answer

The expression (0/0) is indeterminate. Simplify or use another method.

Example:
\[
\lim_{x\to2}\frac{x^2-4}{x-2}
\]
Factor:
\[
\frac{(x-2)(x+2)}{x-2}=x+2\quad(x\ne2)
\]
So the limit is (4). The original expression is undefined at (2), but its limit exists.

## One-sided limits

- (x\to a^-): approach from smaller values.
- (x\to a^+): approach from larger values.

The two-sided limit exists only if both sides approach the same value.

## Limits at infinity

\[
\lim_{x\to\infty}\frac1x=0
\]

As (x) grows, (1/x) approaches zero.

## Mistakes to avoid

- Treating (0/0) as zero.
- Assuming the limit must equal the function value.
- Cancelling terms that are not factors.
- Ignoring one-sided behavior.

## Practice

1. (lim_{x\to4}(2x+1))
2. (lim_{x\to3}(x^2-9)/(x-3))
3. (lim_{x\to0}x^2)

**Answers:** (9), (6), (0).

# 08 — Integration Techniques

## Substitution

Use when an inner function and its derivative appear.

Example:
\[
\int2x(x^2+1)^3dx
\]
Let (u=x^2+1), (du=2x,dx):
\[
\int u^3du=\frac{u^4}4+C=\frac{(x^2+1)^4}4+C
\]

## Integration by parts

\[
\int u\,dv=uv-\int v\,du
\]

Useful when differentiating one factor makes it simpler.

Example:
\[
\int xe^x dx=xe^x-e^x+C
\]

## Other methods

- Trigonometric identities for trig powers/products.
- Partial fractions for suitable rational functions.
- Trigonometric substitution for expressions involving square roots such as (sqrt{a^2-x^2}).

## Choosing a method

Look for an inner function with its derivative (substitution), a product that simplifies when differentiated (parts), or a rational expression (partial fractions).

## Practice

Evaluate (int3x^2(x^3+4)^2dx).

**Answer:** ((x^3+4)^3/3+C).

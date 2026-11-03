# 11 — Differential Equations

A differential equation connects a function with its derivatives. It describes a rule for change.

## Exponential growth/decay

\[
\frac{dy}{dt}=ky
\]

The solution is:
\[
y=Ce^{kt}
\]

- (k>0): growth
- (k<0): decay

## Initial conditions

An initial condition helps find (C). If (y(0)=5), then (C=5).

## Example

\[
\frac{dy}{dt}=2y,\quad y(0)=3
\]

Solution:
\[
y=Ce^{2t}\Rightarrow C=3\Rightarrow y=3e^{2t}
\]

## Separation of variables

For equations of form (dy/dt=g(t)h(y)), rearrange to put y-terms with (dy) and t-terms with (dt), then integrate both sides. Check that the rearrangement is valid.

## Applications

Population, cooling, motion, charging systems, and biological processes. Real systems may need more complicated assumptions.

## Practice

Solve (dy/dt=4y), (y(0)=2).

**Answer:** (y=2e^{4t}).

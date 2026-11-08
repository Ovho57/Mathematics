# Lesson 10 — Data, Features, Labels, and Datasets

Models learn from examples. Data quality strongly affects usefulness.

## Example

Imagine predicting whether a student passes based on practice time:

| Practice hours | Passed? |
|---:|---|
| 1 | No |
| 2 | No |
| 5 | Yes |
| 7 | Yes |

- **Feature:** input information (practice hours).
- **Label/target:** answer to predict (pass/fail).
- **Sample:** one row.
- **Dataset:** collection of samples.

## Numerical and categorical features

Numerical: height, temperature, count, time.

Categorical: color, country, product type.

Models usually need numerical inputs. One-hot encoding represents categories as vectors:

- red → [1,0,0]
- blue → [0,1,0]
- green → [0,0,1]

## Feature scaling

Features may have different ranges. Scaling can help optimization.

Standardization:

`z = (x - mean) / standard_deviation`

This tells how many standard deviations x is from the mean.

## Missing data

Missing values may require removing rows, filling values with a justified method, or marking missingness. Do not automatically treat missing as zero.

## Data leakage

Leakage occurs when training uses information unavailable at prediction time. Example: using a final exam result to predict the result of that same exam. This creates misleadingly high performance.

## Practice

1. For house-price prediction, identify features and target.
2. What does one-hot encoding do?
3. Why is leakage a problem?

## Binomial Distribution

## Requirements
- Only outcomes `True` or `False`
- `const` probability
- we make `N` experiments
- Trials are independent

## Formula
**N**: Number of trials
**p**: probability of success
**x**: no. successes in the no. trials

$$
P(x) = \binom{N}{x} p^x (1-p)^{N-x}
$$

## Usage
>Pikes asks you questions about your code, and only 15% of it was written by you, the rest is by ChatGPT. Pikes asks everybody 10 questions about their code.
> 
> Q: To pass you need to answer 5 questions correctly, what is the chance you will pass?
> 
> Q: To get a 5 mark, you need to answer 8 or more questions right. What is the chance of you passing with the 5?

## Example Code
```python
from scipy.stats import binom

# Question 1
point_p = binom.pmf(5, 10, 0.15)
print(f"Answer 1: {point_p}")

# Question 2
cummulative_p = binom.cdf(2, 10, 1-0.15)
print(f"Answer 2: {cummulative_p}")
```
# Negative Binomial

## Requirements
- Only outcomes `True` or `False` 
- `const` probability 
- Trials are independant
- The last Trial is a success

## Formula
**N**: Number of Trails
**p**: probability of an event occurring
**k**: number of successes in the no. trials
$$
P(k) = \binom{N-1}{k-1} p^k (1-p)^{N-k}
$$

## Usage
>As a prof. of BoP Labs you know each time a student uploads code to STOS it has 13% chance of working. You want to reward the first 3 students that upload a working code with additional great fun homework.
> 
> Question: What is the probability that after 5 uploads you will be able to reward the students (all 3)
> 
> Question: What is the chance it will take over a 30 uploads?

## Example Code
```python
from scipy.stats import nbinom

p = 0.13
k = 3

p1 = nbinom.pdf(5, k, p)
print(f"Answer 1: {p1}")

p2 = nbinom.cdf(30, k, p)
print(f"Answer 2: {1-p2}")
```
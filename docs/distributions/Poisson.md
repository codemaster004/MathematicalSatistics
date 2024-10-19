# Poisson Distribution
Evaluates the probability of a rare event occurring. There are many opportunities but only a small amount are successful.

## Requirements
- Success in period of (time, volume, area, weight, distance)
- Rare independent event

## Formula
**$\lambda$**: mean no. successes per unit
**k**:  no. successes you look for
$$
P(k) = \frac {\lambda^k e^{-\lambda}} {k!}
$$

## Usage
>In your amazing application you are running adds to make money for further development. You find that on average you get 7 clicks per hour.
> 
> Q: If you would be running that ad for over 4 hours, what is the probability of you getting at least 25 clicks?

## Example Code
```python
from scipy.stats import poisson

lamb = 7

# Question 1
cummulative_p = poisson.cdf(25, 4*lamb)
print(f"Answer 1: {cummulative_p}")
```

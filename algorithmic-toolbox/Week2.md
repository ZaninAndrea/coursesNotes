# Week 2
This week the focus is to show why algorithms are important and how they can give enormous improvements in performance.

## Greatest Common Divisor
Key mathematical insight: `gcd(a,b) = gcd(a % b, b) = gcd(b, a % b)`

### Algorithm
```
def EuclidGCD(a,b):
    if b == 0: # 0 can be divded by any number so the gcd is just the other number
        return a
    return EuclidGCD(b, a % b)
```

### Performance
$$
~O(log(ab))
$$

## Big O notation
Big O notation is a simplification, because finding the accurate run time is really hard.
Big O is an asymptotic notation: it only tells us how the run time changes as we change the input size, not what the run time actually is.

Big O notations ignores any multiplicative constant, so 
$$
3*n^2 = \frac{n^2}{4} = O(n^2)
$$

Also smaller terms in a sum can be omitted
$$
n^2 + n = n^2 - 3 = O(n^2)
$$

Big O is the upper bound. To express a lower bound we use Big $\Omega$ and if Big $\Omega$ and Big O are equal we use Big $\Theta$.
Little o notation is a strict upper bound.

## Problem set
### 6 Advanced Problem: Sum of Fibonacci Numbers
I found this formula:

$$
\sum_{n=0}^k F_n = F_{k+2} -1
$$

Given that we only need to find the last digit we can simply use the insight from problem 5: compute all the Fibonacci numbers modulo 10, to improve performance.


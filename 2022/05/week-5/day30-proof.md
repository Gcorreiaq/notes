# Scope

- [Proofs](#proofs)


# Proofs

- **Proving arbitrary long sequences of _n_ non prime numbers**: For every natural number n, there exists a sequence of n consecutive natural numbers which contain no primes. \
\
As an example, the first several sequences of consecutive composites (nonprime) natural numbers with length two or more are < 8, 9, 10 >, < 14, 15, 16 >, < 20, 21, 22 >, < 24, 25, 26, 27, 28 >, < 32, 33, 34, 35, 36 >, < 38, 39, 40 >. \
\
Thus, a few sequences of two consecutive composite natural numbers are < 8, 9 >, < 9, 10 >, < 14, 15 >, < 15, 16 >, < 20, 21 > . . . And a few sequences of three consecutive composite numbers are < 8, 9, 10 >, < 14, 15, 16 >, < 20, 21, 22 >, < 24, 25, 26 >, < 25, 26, 27 >, < 26, 27, 28 >, . . . \
\
Notice in the following sequences of three consecutive composite numbers the first number is divisible by 2, the second number is divisible by 3, and the third number is divisible by 4: < 14, 15, 16 >, < 26, 27, 28 >, < 34, 35, 36 >, < 38, 39, 40 >. \
\
Consequently, for each natural number n, we would like to find, if possible, a number x such that the n consecutive natural numbers x, x + 1, . . ., x + (n − 1) are all composite, and, furthermore, x is divisible by 2, x + 1 is divisible by 3, . . ., x + i is divisible by i + 2, . . ., and x + (n − 1) is divisible by n + 1. \
\
Since 2, 3, . . ., (n + 1) all divide (n + 1)!, our first guess for x is x̂ = (n + 1)!  Clearly, 2 divides x̂. Checking x̂ + 1 = (n + 1)! + 1, we find it is not divisible by 3. We make our second guess for x by adding 2 to x̂, so that x = (n+1)!+2 will be divisible by 2. Rewriting x + 1 = [(n + 1)! + 2] + 1 as x + 1 = (n + 1)! + 3 = 3{[2 · 4 · 5 · · · (n + 1)] + 1}, we see that x + 1 is divisible by 3. And rewriting x + 2 = [(n + 1)! + 2] + 2 as x + 2 = (n + 1)! + 4 = 4{[2 · 3 · 5 · · · (n + 1)] + 1}, we see that x + 2 is divisible by 4. In general, for 0 ≤ i ≤ n − 1, we find: \
    ```
    x + i = [(n + 1)! + 2] + i = (n + 1)! + (2 + i)
    = (2 + i){[2 · · · (1 + i)(3 + i) · · · (n + 1)] + 1}.
    ```
    So, x + i is divisible by 2 + i for 0 ≤ i ≤ n − 1. \
\
**Corollary 2.16.1**: For every natural number n, there exists an infinite num- ber of sequences of n consecutive natural numbers which contain no primes. \
\
It follows from this corollary that if one searches sequentially through the natural numbers for prime numbers, one will often encounter arbitrarily long sequences of consecutive natural numbers which contain no prime.  

- **Side-Notes**: A corollary is a theorem which follows so obviously from the proof of another theorem that no proof, or almost no proof, is necessary.

## Birthday Problem

Suppose three people are in a room. What is the probability that at least two people share a birthday?

First, we can calculate the probability that there are _**no**_ repeating birthdays:

$P(\text{no repeating birthdays}) = P(A)$

$P(A) = \frac{(365 - 0) \cdot (365 - 1) \cdot (365 - 2)}{365^3}$

Since:
$(365 - 0) \cdot (365 - 1) \cdot (365 - 2) = P(n,r)$

Then the formula can be simplified to:

$P(A) = \frac{P(365,3)}{365^n}$

Therefor, the probability that a birthday does repeat is:

$P(repetition) = 1 - P(A)$

In the example above, that gives:

$1 - \frac{P(365,3)}{365^3} \approx 1-0.983644 \approx 0.016 \approx 1.6\%$

Therefor, the probability that of 4 people selected at random, at least one birthday is shared is $1.6\%$

**NOTE**: $P(365,3)$, also known as $Permutation$, is given as:

$P(n, k) = n\cdot (n-1)\cdot (n-2) ... (n-k+1) = \frac{n!}{(n-k)!}$
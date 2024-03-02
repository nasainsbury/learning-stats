## Cominbations

Combinations count the number of ways to choose a certain number of items from a larger set without considering the order in which they are chosen.

Combinations can be written as $n\choose r$, where $n$ respresents the total number of items in the set, and $r$ is the number of items you want to choose.

Suppose you have 4 colours, $red$, $green$, $blue$ and $yellow$. From the set we want to pick 2 of those colours. The following combinations could be written as:

- $red$ and $green$
- $red$ and $blue$
- $red$ and $yellow$
- $blue$ and $yellow$
- $blue$ and $green$
- $yellow$ and $green$

In the above example, we'd say that $4\space chooses \space 2$, or $4\choose2$.

To caulcate this value we can do:
$\frac{n!}{r!\cdot (n-r)!}$

## Birthday Problem

Suppose three people are in a room. What is the probability that at least two people share a birthday?

First, we can calculate the probability that there are _**no**_ repeating birthdays:

$P(\text{no repeating birthdays}) = P(A)$

How do we calculate that? Well, if there were 3 people, the first person could have any birthday, i.e $\frac{365}{365}$, the second person could have any day, minus the previous, i.e $\frac{365 - 1}{365}$, the third person would therefor have $\frac{365 - 2}{365}$.

If we multiple those together, we get the probability of none of the 3 people sharing a birthday.

$P(A) = \frac{(365 - 0) \cdot (365 - 1) \cdot (365 - 2)}{365^3}$

Since:
$(365 - 0) \cdot (365 - 1) \cdot (365 - 2) = P(n,r)$

Then the formula can be simplified to:

$P(A) = \frac{P(365,3)}{365^n}$

To find the chance that someone does share a birthday, we want the opposite of that, or the $compliment$.

$P(repetition) = 1 - P(A)$

In the example above, that gives:

$1 - \frac{P(365,3)}{365^3} \approx 1-0.983644 \approx 0.016 \approx 1.6\\%$

Therefor, the probability that of 4 people selected at random, at least one birthday is shared is $1.6\\%$

**NOTE**: $P(365,3)$, also known as $Permutation$, is given as:

$P(n, k) = n\cdot (n-1)\cdot (n-2) ... (n-k+1) = \frac{n!}{(n-k)!}$

### A birthday occurs $x$ times

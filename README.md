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

## The Newton–Pepys problem

Suppose you have a fair dice with 6 sides, consider the following events:

$A$: A dice is tossed $6$ times, what is the likelihood that at least _**one**_ $6$ appears.

$B$: A dice is tossed $12$ times, what is the likelihood that at least _**two**_ $6$'s' appears.

$C$: A dice is tossed $16$ times, what is the likelihood that at least _**three**_ $6$'s appears.

$P(A)$ can be calculated by finding the complement of the likelihood that none of the throws are $6$, $1 - (\frac{5}{6})^6$.

$P(A) = 1 - (\frac{5}{6})^6 \approx 0.6651$.

$P(B)$ can be calculated with the following information:

- $P(no\space6)$: no $6$ appears within $12$ dice as $(\frac{5}{6})^{12}$
- $P(one\space6)$: the probability that only _**one**_ $6$ appears as ${12\choose1}\cdot(\frac{1}{6})\cdot(\frac{5}{6})^{11}$. The reason for multiply by ${12\choose1}$ is that there are $12$ occurances where the $6$ could occur.

$P(B)$ can then be calculated as $1 - (P(no\space6) + P(one\space6))\approx 0.6187$.

$P(C)$ can the be summaries to be equal to: $1 - (P(no\space6) + P(one\space6) + P(two\space6))$.

In summary, the formula for this can be _simplified_ to:

$1 - \sum_{x=0}^{k} {6k\choose x}\cdot(\frac{1}{6})^{x}\cdot(\frac{5}{6})^{6k-x}$, where $k$ represents the number of groups.

Essentially, what we are doing in summing the probabilities that $n$ number of $6$'s occur from $n=0$.

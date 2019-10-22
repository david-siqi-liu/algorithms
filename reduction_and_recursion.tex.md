## Reduction

Reduction - use known algorithms to solve new problems.

### 2Sum

*2Sum* can be solved by

- Brute force - $O(n^2)$
- Sorting, and then then binary search on $m - B[i]$ for every $i$ - $O(n\log{n})$

### 3Sum

*3Sum* can be reduced to *2Sum*

- We want $A[i] + A[j] + A[k] = m$
- For every $k$, run *2Sum* with target $m - A[k]$

Total run time - $O(n \cdot n\log{n}) = O(n^2\log{n})$

However, notice that we only need to sort once, so the run time is actually $O(n\log{n}) + O(n^2) = O(n^2)$.

## Recursion

Recursion is a special type of reduction, where we reduce the original problem to the *same* problem, but on a *smaller* input.

$T(n)$ is the time complexity of the algorithm on arrays with $n$ entries.

### Recurrence Tree

1. Show at level $i$, how many nodes are there (assume starting at level 0), and how much work *at each node* (including the leaves)
2. Show how many levels there are. Specifically, solve for $k = f^{-1}(1)$, where $f$ is how $n$ gets divided
3. Add up total work $\sum_{i = 0}^{k}(work \cdot nodes)$

### Example - MergeSort

$$T(n) = T(\lfloor\frac{n}{2}\rfloor) + T(\lceil\frac{n}{2}\rceil) + \Theta(n)$$

Assume that $n$ is a power of 2, then

$$T(n) = 2T(\frac{n}{2}) + \Theta(n)$$

Recurrent tree:

![image-20191010150405973](pics/image-20191010150405973.png)

The recurrence tree has

- $2^i$ nodes per level (starting at level 0), with $\Theta(\frac{n}{2^i})$ work at each node 
- $1 = \frac{n}{2^k} \Rightarrow k = \log{n}$ levels

Total time complexity

$T(n) = \sum_{i = 0}^{\log{n}}2^i \cdot \Theta(\frac{n}{2^i})=\sum_{i = 0}^{\log{n}}\Theta(n) = \Theta(n\log{n})$

### Master Theorem

![image-20191010150827585](pics/image-20191010150827585.png)

This is because we can express $T(n)$ as

$T(n) = (1 + \frac{a}{b^c} + ... + (\frac{a}{b^c})^{\log_{b}{n}}) \cdot \Theta(n^c) = (\sum_{i = 0}^{\log_b{n}}(\frac{a}{b^c})^i) \Theta(n^c)$

which is a geometric series with ratio $\frac{a}{b^c}$.

### Geometric Series

![image-20191010151059728](pics/image-20191010151059728.png)

Then, for

- $0 < r < 1$, $f : n \longrightarrow 1 + r + r^2 + ... + r^n = \Theta(1)$ 
- $r > 1$, $f : n \longrightarrow 1 + r + r^2 + ... + r^n = \Theta(r^n)$ 


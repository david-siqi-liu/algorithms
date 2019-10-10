## Computational Model

**Definition** - the *Word RAM* model is the computation model in which for an algorithm run on an input of size *n*,

- The memory of the algorithm is broken up into *word* of length *w* (typically, *w* = $\lceil\log{n}\rceil$), and
- Any elementary operation (read, write, add, multiply, AND, etc.) on any single word in memory takes 1 time step

## Big-O Notation

**Definition** - the *worst-case time complexity* of an algorithm $A$ is the function $T_A : \N \longrightarrow \N$ obtained by letting $T_A(n)$ be the maximum time complexity of $A$ over any input of size $n$.

We care about the **asymptotic** rate of growth as the inputs get larger.

**Definition** - two functions $f, g : \N \longrightarrow \R^{\geq 1}$ satisfy $f = O(g)$ is there exist $c \in \R^+$ and $n_o \in \N$ such that for every $n \geq n_o$, we have $f(n) \leq cg(n)$


A *greedy* algorithm is one in which we:

1. Breakdown a problem into a sequence of decisions that need to be made, then
2. Make the decisions one at a time, each time choosing the option that is optimal **at the moment** (and not worrying about later decisions)

## Always Ahead

We show that at every point in the execution of our greedy algorithm, we can complete the partial solution we have obtained so far into a valid solution to the original problem.

### Proof Framework

First, we need to show the base case:

- Define $I^* = \{i_1, i_2, ..., i_k\}$ to be the *true* optimal solution
- Define $j_1$ to be the **first** index that our algorithm returns
- Show that $I^{1} = \{j_1, i_2, ..., i_k\}$ is also a valid (optimal) solution

Then, let the algorithm output be $I^{\dagger} = \{j_1, j_2, ..., j_m\}$.

We need to show that $I^{m} = \{j_1, j_2, ..., j_m, i_{m+1}, ..., i_k\}$ is also a valid (optimal) solution via induction

- Assume $I^{(c - 1)}$ is a solution
- Show that $I^{c}$ is also a solution

Lastly, show that $m = k$ by making structural arguments of the algorithm (e.g. the algorithm returns up until $m$ only if all other intervals with finish time greater than $j_m$ interset with some intervals already in $I^{\dagger}$).

### Example - Interval Scheduler

![image-20191012183401772](pics/image-20191012183401772.png)

![image-20191012184958631](pics/image-20191012184958631.png)

## Exchange

We show that given any valid solution to the problem, we can convert it to the algorithm output without compromising the metric.

### Proof Framework

1. (If necessary) assume w.o.l.g. that the arrays are sorted in increasing/decreasing order
2. Let $S^*$ be any arbitrary solution (not necessarily the optimal solution), and $S^{\dagger}$ be the solution produced by our algorithm
3. If $S^* \ne S^{\dagger}$, then there is consecutive/some pair where ...
4. Therefore, the current measure, in $S^*$ is ...
5. If we swap ... in $S^*$, the new measure would be ..., which **proves to be better than before**. May also need to prove that the new solution is valid.
6. If we iterately swap out of order pairs, we will eventually stop because
   1. There can be at most (n choose 2) possible swaps
   2. $S^* = S^{\dagger}$
7. Since we improve the measure along the way, this establishes that $S^{\dagger}$ is better than $S^*$, so $S^{\dagger}$ is the optimal solution

### Example - Fractional Knapsack

![image-20191012183428099](pics/image-20191012183428099.png)

![image-20191012184933789](pics/image-20191012184933789.png)

![image-20191012185448651](pics/image-20191012185448651.png)
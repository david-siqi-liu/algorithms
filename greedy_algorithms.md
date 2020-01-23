A *greedy* algorithm is one in which we:

1. Breakdown a problem into a sequence of decisions that need to be made, then
2. Make the decisions one at a time, each time choosing the option that is optimal **at the moment** (and not worrying about later decisions)

## Always Ahead

We show that at every point in the execution of our greedy algorithm, we can complete the partial solution we have obtained so far into a valid solution to the original problem.

### Proof Framework

First, we need to show the base case:

- Define <img src="/tex/658fedd8a8da85e40ecc516d7c18dfbf.svg?invert_in_darkmode&sanitize=true" align=middle width=129.8719686pt height=24.65753399999998pt/> to be the *true* optimal solution
- Define <img src="/tex/82b58c8d1599d08c33130ebcf4a2e7c8.svg?invert_in_darkmode&sanitize=true" align=middle width=13.321977899999991pt height=21.68300969999999pt/> to be the **first** index that our algorithm returns
- Show that <img src="/tex/c640cf7645a99779621acd0e09a84abb.svg?invert_in_darkmode&sanitize=true" align=middle width=130.79554455pt height=26.76175259999998pt/> is also a valid (optimal) solution

Then, let the algorithm output be <img src="/tex/37420f7004405c4ffe09d87290c849b2.svg?invert_in_darkmode&sanitize=true" align=middle width=136.8816372pt height=27.91243950000002pt/>.

We need to show that <img src="/tex/8e6532da69210ef39c38866bb5da7fe1.svg?invert_in_darkmode&sanitize=true" align=middle width=226.68047324999992pt height=24.65753399999998pt/> is also a valid (optimal) solution via induction

- Assume <img src="/tex/5cba7fc13306631eba197cdd5d0554b7.svg?invert_in_darkmode&sanitize=true" align=middle width=41.491218449999984pt height=29.190975000000005pt/> is a solution
- Show that <img src="/tex/402cf361f2a850d9ca72d626c8280622.svg?invert_in_darkmode&sanitize=true" align=middle width=14.39061854999999pt height=22.465723500000017pt/> is also a solution

Lastly, show that <img src="/tex/f80805478cd0481b545d6e3c84c5e74f.svg?invert_in_darkmode&sanitize=true" align=middle width=45.42610049999999pt height=22.831056599999986pt/> by making structural arguments of the algorithm (e.g. the algorithm returns up until <img src="/tex/0e51a2dede42189d77627c4d742822c3.svg?invert_in_darkmode&sanitize=true" align=middle width=14.433101099999991pt height=14.15524440000002pt/> only if all other intervals with finish time greater than <img src="/tex/2bd0ef3d70c4ab12c16c5faa6f14eb02.svg?invert_in_darkmode&sanitize=true" align=middle width=18.43428179999999pt height=21.68300969999999pt/> interset with some intervals already in <img src="/tex/7909829b6782f77c386ebff41cb40b5e.svg?invert_in_darkmode&sanitize=true" align=middle width=14.54339534999999pt height=27.91243950000002pt/>).

### Example - Interval Scheduler

![image-20191012183401772](pics/image-20191012183401772.png)

![image-20191012184958631](pics/image-20191012184958631.png)

## Exchange

We show that given any valid solution to the problem, we can convert it to the algorithm output without compromising the metric.

### Proof Framework

1. (If necessary) assume w.o.l.g. that the arrays are sorted in increasing/decreasing order
2. Let <img src="/tex/0e9acb8e323d122fa04eea6eb4e79496.svg?invert_in_darkmode&sanitize=true" align=middle width=17.76257669999999pt height=22.63846199999998pt/> be any arbitrary solution (not necessarily the optimal solution), and <img src="/tex/404761058ff6e600f83fd7b7226805d4.svg?invert_in_darkmode&sanitize=true" align=middle width=17.05481249999999pt height=27.91243950000002pt/> be the solution produced by our algorithm
3. If <img src="/tex/795f80c8a3bc1925b831c6b6f89f9cdf.svg?invert_in_darkmode&sanitize=true" align=middle width=57.55691369999999pt height=27.91243950000002pt/>, then there is consecutive/some pair where ...
4. Therefore, the current measure, in <img src="/tex/0e9acb8e323d122fa04eea6eb4e79496.svg?invert_in_darkmode&sanitize=true" align=middle width=17.76257669999999pt height=22.63846199999998pt/> is ...
5. If we swap ... in <img src="/tex/0e9acb8e323d122fa04eea6eb4e79496.svg?invert_in_darkmode&sanitize=true" align=middle width=17.76257669999999pt height=22.63846199999998pt/>, the new measure would be ..., which **proves to be better than before**. May also need to prove that the new solution is valid.
6. If we iterately swap out of order pairs, we will eventually stop because
   1. There can be at most (n choose 2) possible swaps
   2. $S^* = S^{\dagger}$
7. Since we improve the measure along the way, this establishes that <img src="/tex/404761058ff6e600f83fd7b7226805d4.svg?invert_in_darkmode&sanitize=true" align=middle width=17.05481249999999pt height=27.91243950000002pt/> is better than <img src="/tex/0e9acb8e323d122fa04eea6eb4e79496.svg?invert_in_darkmode&sanitize=true" align=middle width=17.76257669999999pt height=22.63846199999998pt/>, so <img src="/tex/404761058ff6e600f83fd7b7226805d4.svg?invert_in_darkmode&sanitize=true" align=middle width=17.05481249999999pt height=27.91243950000002pt/> is the optimal solution

### Example - Fractional Knapsack

![image-20191012183428099](pics/image-20191012183428099.png)

![image-20191012184933789](pics/image-20191012184933789.png)

![image-20191012185448651](pics/image-20191012185448651.png)
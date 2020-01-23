## Reduction

- ==2Sum==

![image-20191022084312032](pics/image-20191022084312032.png)

![image-20191022084322745](pics/image-20191022084322745.png)

Run time = $\Theta(n\log{n})$

- ==3Sum==

![image-20191022084342500](pics/image-20191022084342500.png)

![image-20191022084355687](pics/image-20191022084355687.png)

Run time = $\Theta(n^2\log{n})$, actually $\Theta(n^2)$ since we only need to sort once at the beginning

- ==MergeSort==

![image-20191022084458527](pics/image-20191022084458527.png)

Run time = $\Theta(n\log{n})$

## Divide and Conquer

- ==Counting Inversions==

![image-20191022084600657](pics/image-20191022084600657.png)

![image-20191022084612348](pics/image-20191022084612348.png)

Run time = $O(n\log{n})$

- ==Fast Integer Multiplication==

<img src="pics/image-20191209150520721.png" alt="image-20191209150520721" style="zoom:50%;" />

<img src="pics/image-20191209150547209.png" alt="image-20191209150547209" style="zoom:50%;" />

![image-20191022084700958](pics/image-20191022084700958.png)

![image-20191022084719199](pics/image-20191022084719199.png)

$T(n) = 3T(\frac{n}{2}) + O(n)$, as opposed to $T(n) = 4T(\frac{n}{2}) + O(n)$ if we were to do normal multiplication

Run time = $O(n^{\log_{2}{3}}) = O(n^{1.59})$

- ==Fast Matrix Multiplication - **Strassen's Algorithm**==

<img src="pics/image-20191209152559432.png" alt="image-20191209152559432" style="zoom:50%;" />

<img src="pics/image-20191209152610441.png" alt="image-20191209152610441" style="zoom:50%;" />

<img src="pics/image-20191209152643590.png" alt="image-20191209152643590" style="zoom:50%;" />

$T(n) = 7T(\frac{n}{2}) + O(n^2) = O(n^{\log_{2}{7}}) = O(n^{2.81})$

## Greedy

- ==Making Change==

![image-20191022084920712](pics/image-20191022084920712.png)

![image-20191022084929287](pics/image-20191022084929287.png)

Run time = $O(n)$

- ==Interval Scheduling (non-weighted)==

![image-20191022085021352](pics/image-20191022085021352.png)

Strategy: earliest finish time

![image-20191022085039910](pics/image-20191022085039910.png)

Run time = $\Theta(n\log{n})$

- ==Minimizing Lateness==

![image-20191022085144136](pics/image-20191022085144136.png)

![image-20191022085155500](pics/image-20191022085155500.png)

Strategy - earliest deadline

![image-20191022085212142](pics/image-20191022085212142.png)

Run time = $O(n^2)$

- ==Interval Colouring==

<img src="pics/image-20191212135151178.png" alt="image-20191212135151178" style="zoom:50%;" />

Run time = $O(n \log n)$, since we need to sort by start time

- ==Fractional Knapsack==

![image-20191022085247026](pics/image-20191022085247026.png)

Strategy - sort by decreasing $\frac{v_i}{w_i}$

![image-20191022085329674](pics/image-20191022085329674.png)

Run time = $O(n \log n)$, since we need to sort by $\frac{v_i}{w_i}$

## Dynamic Programming

- ==Text Segmentation==

![image-20191022085501127](pics/image-20191022085501127.png)

![image-20191022085526960](pics/image-20191022085526960.png)

![image-20191022085536147](pics/image-20191022085536147.png)

Run time = $O(n^2)$

- ==Longest Increasing Subsequence==

![image-20191022085633260](pics/image-20191022085633260.png)

![image-20191022085641961](pics/image-20191022085641961.png)

![image-20191022085651698](pics/image-20191022085651698.png)

Run time = $O(n^2)$

- ==Longest Common Subsequence==

![image-20191022085712450](pics/image-20191022085712450.png)

![image-20191022085735128](pics/image-20191022085735128.png)

![image-20191022085743119](pics/image-20191022085743119.png)

Run time = $\Theta(mn)$

- ==Edit Distance==

![image-20191022085900952](pics/image-20191022085900952.png)

![image-20191022085918492](pics/image-20191022085918492.png)

![image-20191022085927729](pics/image-20191022085927729.png)

Run time = $O(mn)$

- ==Interval Scheduling (weighted)==

![image-20191022085956194](pics/image-20191022085956194.png)

![image-20191022090004705](pics/image-20191022090004705.png)

![image-20191022090013465](pics/image-20191022090013465.png)

Run time = $O(n\log{n})$ since we've sorted by finish time

- ==Optimal Binary Search Tree==

![image-20191022090040451](pics/image-20191022090040451.png)

![image-20191022090052989](pics/image-20191022090052989.png)

![image-20191022090105184](pics/image-20191022090105184.png)

Runt time = $O(n^2)$

- ==0-1 Knapsack==

![image-20191022090133214](pics/image-20191022090133214.png)

![image-20191022090149628](pics/image-20191022090149628.png)

Run time = $\Theta(nW)$


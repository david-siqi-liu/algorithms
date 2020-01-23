## Reduction

- ==2Sum==

![image-20191022084312032](pics/image-20191022084312032.png)

![image-20191022084322745](pics/image-20191022084322745.png)

Run time = <img src="/tex/a69789444a61f0001aaf57f7ad5e8c50.svg?invert_in_darkmode&sanitize=true" align=middle width=72.01684874999998pt height=24.65753399999998pt/>

- ==3Sum==

![image-20191022084342500](pics/image-20191022084342500.png)

![image-20191022084355687](pics/image-20191022084355687.png)

Run time = <img src="/tex/1f83d2137ed79662b5967efb3bd6369b.svg?invert_in_darkmode&sanitize=true" align=middle width=79.39130759999998pt height=26.76175259999998pt/>, actually <img src="/tex/7f673488709d91c2cf326d97e5a437c3.svg?invert_in_darkmode&sanitize=true" align=middle width=42.81220349999999pt height=26.76175259999998pt/> since we only need to sort once at the beginning

- ==MergeSort==

![image-20191022084458527](pics/image-20191022084458527.png)

Run time = <img src="/tex/a69789444a61f0001aaf57f7ad5e8c50.svg?invert_in_darkmode&sanitize=true" align=middle width=72.01684874999998pt height=24.65753399999998pt/>

## Divide and Conquer

- ==Counting Inversions==

![image-20191022084600657](pics/image-20191022084600657.png)

![image-20191022084612348](pics/image-20191022084612348.png)

Run time = <img src="/tex/c55f40a98d74d6754f146e5384773404.svg?invert_in_darkmode&sanitize=true" align=middle width=72.2268393pt height=24.65753399999998pt/>

- ==Fast Integer Multiplication==

<img src="pics/image-20191209150520721.png" alt="image-20191209150520721" style="zoom:50%;" />

<img src="pics/image-20191209150547209.png" alt="image-20191209150547209" style="zoom:50%;" />

![image-20191022084700958](pics/image-20191022084700958.png)

![image-20191022084719199](pics/image-20191022084719199.png)

<img src="/tex/0855f59bf98da1465f84b0cf8a7f8b6c.svg?invert_in_darkmode&sanitize=true" align=middle width=157.16334644999998pt height=24.65753399999998pt/>, as opposed to <img src="/tex/aa8611e423057536829dfc40215727be.svg?invert_in_darkmode&sanitize=true" align=middle width=157.16334644999998pt height=24.65753399999998pt/> if we were to do normal multiplication

Run time = <img src="/tex/b48c175464e33d7b3746b46f33f91279.svg?invert_in_darkmode&sanitize=true" align=middle width=150.6353508pt height=27.91243950000002pt/>

- ==Fast Matrix Multiplication - **Strassen's Algorithm**==

<img src="pics/image-20191209152559432.png" alt="image-20191209152559432" style="zoom:50%;" />

<img src="pics/image-20191209152610441.png" alt="image-20191209152610441" style="zoom:50%;" />

<img src="pics/image-20191209152643590.png" alt="image-20191209152643590" style="zoom:50%;" />

<img src="/tex/0c856b24a5fe51fed2f2246af73266a7.svg?invert_in_darkmode&sanitize=true" align=middle width=337.09078754999996pt height=27.91243950000002pt/>

## Greedy

- ==Making Change==

![image-20191022084920712](pics/image-20191022084920712.png)

![image-20191022084929287](pics/image-20191022084929287.png)

Run time = <img src="/tex/1f08ccc9cd7309ba1e756c3d9345ad9f.svg?invert_in_darkmode&sanitize=true" align=middle width=35.64773519999999pt height=24.65753399999998pt/>

- ==Interval Scheduling (non-weighted)==

![image-20191022085021352](pics/image-20191022085021352.png)

Strategy: earliest finish time

![image-20191022085039910](pics/image-20191022085039910.png)

Run time = <img src="/tex/a69789444a61f0001aaf57f7ad5e8c50.svg?invert_in_darkmode&sanitize=true" align=middle width=72.01684874999998pt height=24.65753399999998pt/>

- ==Minimizing Lateness==

![image-20191022085144136](pics/image-20191022085144136.png)

![image-20191022085155500](pics/image-20191022085155500.png)

Strategy - earliest deadline

![image-20191022085212142](pics/image-20191022085212142.png)

Run time = <img src="/tex/3987120c67ed5a9162aa9841b531c3a9.svg?invert_in_darkmode&sanitize=true" align=middle width=43.02219404999999pt height=26.76175259999998pt/>

- ==Interval Colouring==

<img src="pics/image-20191212135151178.png" alt="image-20191212135151178" style="zoom:50%;" />

Run time = <img src="/tex/ff514eba41c59f90c20d895e80719763.svg?invert_in_darkmode&sanitize=true" align=middle width=72.2268393pt height=24.65753399999998pt/>, since we need to sort by start time

- ==Fractional Knapsack==

![image-20191022085247026](pics/image-20191022085247026.png)

Strategy - sort by decreasing <img src="/tex/8496e39ab9fa4b9b6393f1803ac53238.svg?invert_in_darkmode&sanitize=true" align=middle width=14.717089199999998pt height=23.388043799999995pt/>

![image-20191022085329674](pics/image-20191022085329674.png)

Run time = <img src="/tex/ff514eba41c59f90c20d895e80719763.svg?invert_in_darkmode&sanitize=true" align=middle width=72.2268393pt height=24.65753399999998pt/>, since we need to sort by <img src="/tex/8496e39ab9fa4b9b6393f1803ac53238.svg?invert_in_darkmode&sanitize=true" align=middle width=14.717089199999998pt height=23.388043799999995pt/>

## Dynamic Programming

- ==Text Segmentation==

![image-20191022085501127](pics/image-20191022085501127.png)

![image-20191022085526960](pics/image-20191022085526960.png)

![image-20191022085536147](pics/image-20191022085536147.png)

Run time = <img src="/tex/3987120c67ed5a9162aa9841b531c3a9.svg?invert_in_darkmode&sanitize=true" align=middle width=43.02219404999999pt height=26.76175259999998pt/>

- ==Longest Increasing Subsequence==

![image-20191022085633260](pics/image-20191022085633260.png)

![image-20191022085641961](pics/image-20191022085641961.png)

![image-20191022085651698](pics/image-20191022085651698.png)

Run time = <img src="/tex/3987120c67ed5a9162aa9841b531c3a9.svg?invert_in_darkmode&sanitize=true" align=middle width=43.02219404999999pt height=26.76175259999998pt/>

- ==Longest Common Subsequence==

![image-20191022085712450](pics/image-20191022085712450.png)

![image-20191022085735128](pics/image-20191022085735128.png)

![image-20191022085743119](pics/image-20191022085743119.png)

Run time = <img src="/tex/2c0902fcf368037e571671705d072017.svg?invert_in_darkmode&sanitize=true" align=middle width=49.87084409999999pt height=24.65753399999998pt/>

- ==Edit Distance==

![image-20191022085900952](pics/image-20191022085900952.png)

![image-20191022085918492](pics/image-20191022085918492.png)

![image-20191022085927729](pics/image-20191022085927729.png)

Run time = <img src="/tex/74ff9597b56d1e5ba834cc5569819dd1.svg?invert_in_darkmode&sanitize=true" align=middle width=50.080834649999986pt height=24.65753399999998pt/>

- ==Interval Scheduling (weighted)==

![image-20191022085956194](pics/image-20191022085956194.png)

![image-20191022090004705](pics/image-20191022090004705.png)

![image-20191022090013465](pics/image-20191022090013465.png)

Run time = <img src="/tex/c55f40a98d74d6754f146e5384773404.svg?invert_in_darkmode&sanitize=true" align=middle width=72.2268393pt height=24.65753399999998pt/> since we've sorted by finish time

- ==Optimal Binary Search Tree==

![image-20191022090040451](pics/image-20191022090040451.png)

![image-20191022090052989](pics/image-20191022090052989.png)

![image-20191022090105184](pics/image-20191022090105184.png)

Runt time = <img src="/tex/3987120c67ed5a9162aa9841b531c3a9.svg?invert_in_darkmode&sanitize=true" align=middle width=43.02219404999999pt height=26.76175259999998pt/>

- ==0-1 Knapsack==

![image-20191022090133214](pics/image-20191022090133214.png)

![image-20191022090149628](pics/image-20191022090149628.png)

Run time = <img src="/tex/058905365c80a81a569aeb06e95e047f.svg?invert_in_darkmode&sanitize=true" align=middle width=53.24600159999999pt height=24.65753399999998pt/>


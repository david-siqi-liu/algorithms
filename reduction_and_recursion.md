## Reduction

Reduction - use known algorithms to solve new problems.

### 2Sum

*2Sum* can be solved by

- Brute force - <img src="/tex/3987120c67ed5a9162aa9841b531c3a9.svg?invert_in_darkmode&sanitize=true" align=middle width=43.02219404999999pt height=26.76175259999998pt/>
- Sorting, and then then binary search on <img src="/tex/274f46cc0101f598ad9a2fdccfaddb97.svg?invert_in_darkmode&sanitize=true" align=middle width=62.61337004999998pt height=24.65753399999998pt/> for every <img src="/tex/77a3b857d53fb44e33b53e4c8b68351a.svg?invert_in_darkmode&sanitize=true" align=middle width=5.663225699999989pt height=21.68300969999999pt/> - <img src="/tex/c55f40a98d74d6754f146e5384773404.svg?invert_in_darkmode&sanitize=true" align=middle width=72.2268393pt height=24.65753399999998pt/>

### 3Sum

*3Sum* can be reduced to *2Sum*

- We want <img src="/tex/bfa70f52683e82b5291b02787702a356.svg?invert_in_darkmode&sanitize=true" align=middle width=163.36585979999998pt height=24.65753399999998pt/>
- For every <img src="/tex/63bb9849783d01d91403bc9a5fea12a2.svg?invert_in_darkmode&sanitize=true" align=middle width=9.075367949999992pt height=22.831056599999986pt/>, run *2Sum* with target <img src="/tex/f79e85a4a0ee64abb0fd4639f3d4e9b0.svg?invert_in_darkmode&sanitize=true" align=middle width=65.06090084999998pt height=24.65753399999998pt/>

Total run time - <img src="/tex/fe7c73862e6cf8beb896944a60e53568.svg?invert_in_darkmode&sanitize=true" align=middle width=195.4846278pt height=26.76175259999998pt/>

However, notice that we only need to sort once, so the run time is actually <img src="/tex/60c383a596226edafe9d3d167a99e7ac.svg?invert_in_darkmode&sanitize=true" align=middle width=200.28005084999998pt height=26.76175259999998pt/>.

## Recursion

Recursion is a special type of reduction, where we reduce the original problem to the *same* problem, but on a *smaller* input.

<img src="/tex/cc4152a1ba8a0ec113e9f2062a489b7d.svg?invert_in_darkmode&sanitize=true" align=middle width=34.54162139999999pt height=24.65753399999998pt/> is the time complexity of the algorithm on arrays with <img src="/tex/55a049b8f161ae7cfeb0197d75aff967.svg?invert_in_darkmode&sanitize=true" align=middle width=9.86687624999999pt height=14.15524440000002pt/> entries.

### MergeSort

<p align="center"><img src="/tex/e37059d466d873f8dfe5a83bac4f6fdc.svg?invert_in_darkmode&sanitize=true" align=middle width=238.27683pt height=29.47417935pt/></p>

Assume that <img src="/tex/55a049b8f161ae7cfeb0197d75aff967.svg?invert_in_darkmode&sanitize=true" align=middle width=9.86687624999999pt height=14.15524440000002pt/> is a power of 2, then

<p align="center"><img src="/tex/a26fbc5103e716e09e5e135871b0134b.svg?invert_in_darkmode&sanitize=true" align=middle width=158.6942115pt height=29.47417935pt/></p>

Recurrent tree:

![image-20191010150405973](pics/image-20191010150405973.png)

The recurrence tree has

- Depth <img src="/tex/542a64dff789dfddc99a1c72ab26067d.svg?invert_in_darkmode&sanitize=true" align=middle width=33.83944574999999pt height=22.831056599999986pt/>
- <img src="/tex/272e3ab168729ac17efd78e4c03be40f.svg?invert_in_darkmode&sanitize=true" align=middle width=35.43774299999999pt height=24.65753399999998pt/> of work at each level on compelting the merge

Total time complexity - <img src="/tex/53541bb0ee56860782369e89553ea6bb.svg?invert_in_darkmode&sanitize=true" align=middle width=128.47609995pt height=24.65753399999998pt/>

### Master Theorem

![image-20191010150827585](pics/image-20191010150827585.png)

### Geometric Series

![image-20191010151059728](pics/image-20191010151059728.png)

Then, for

- <img src="/tex/aeac939a260f6194ac77956d3c044107.svg?invert_in_darkmode&sanitize=true" align=middle width=68.14663515pt height=21.18721440000001pt/>, <img src="/tex/132f01596e0cb34b9c3244c2c7467885.svg?invert_in_darkmode&sanitize=true" align=middle width=266.93069535pt height=26.76175259999998pt/> 
- <img src="/tex/614574d0a2f0cc76a9a5f3892219f4c1.svg?invert_in_darkmode&sanitize=true" align=middle width=38.009795999999994pt height=21.18721440000001pt/>, <img src="/tex/a9e23f0f4e31573f779caa6f293761fc.svg?invert_in_darkmode&sanitize=true" align=middle width=275.532378pt height=26.76175259999998pt/> 


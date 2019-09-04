# Sorting Algorithms

## Loop Invariant

Can be used to help us understand why an algorith is correct

**Initialization**:  It is true prior to the first iteration of the loop

**Maintenance**: If it is true before an interation of the loop, it remains true before the next iteration

**Termination**: When the loop terminates, the invariant gives us a useful property that helps show that the algorithm is correct

## Insertion Sort

```pseudocode
for j = 2 to A.length
	key = A[j]
	// Insert A[j] into the sorted sequence A[1..j-1]
	i = j - 1
	// Start with the previous number and go backward
	while i > 0 and A[i] > key:
		A[i + 1] = A[i] // If A[i] > key, shift A[i] to the right by one
		i = i - 1 // Move onto the next number (on the left)
	A[i + 1] = key // A[i] < key, insert key into A[i+1]
```

**Initialization**: j is initialized to be 2, and subarray A[1] is trivially sorted

**Maintenance**: Given that A[1 .. j-1] is sorted, we can show that the algorithm correctly inserts the item in the right place. Strictly speaking we also need to show loop invariant for the *while* loop

**Termination**: The *foor* loop terminates when j > A.length = n, i.e. when j = n + 1. Substituting n + 1 for j in the wording of loop invariant, we have the the subarray A[1..n] is sorted

## Selection Sort

Consider sorting n numbers stored in array A by first finding the smallest element of A and exchanging it with the element in A[1]􏰀. Then find the second smallest element of A, and exchange it with A[2]. Continue in this manner for the first n - 1elements of A.

```python
for i, n in enumerate(A):
    smallest = i # Initalize smallest index to be the current index
    for j, k in enumerate(A[i:]): # Loop to the right
        if k < A[smallest]: # Find a smaller number
            smallest = j + i # Update smallest index
    A[i], A[smallest] = A[smallest], n # Swap numbers
```

## Merge Sort

Divide and conquer:

**Divide**: Divide the n-element sequence to be sorted into two sub-sequences of n/2 elements each

**Conquer**: Sort the two sub-sequences recursively using merge sort

**Combine**: Merge the two sorted sub-sequences to produce the sorted answer

The sub-routine *merge* works as follows:

1. We merge by calling an auxiliary procedure ***merge(A, p, q, r)***, where A is an array and p, q, and r are indices into the array such that p <= q < r
2. The procedure assumes that the sub-arrays A[p .. q] and A[q + 1 .. r]􏰀 are in sorted order
3. We choose the smaller number between the smallest numbers from each sub-array (since both are sorted), remove it from the sub-array, and place it into the output array
4. Repeat this step until one sub-array is empty, at which time we just take the remaining, other sub-array and put it all into the output array
5. Since each comparison step takes constant time, and we perform at most n steps, the *merge* function takes O(n) time

Psedocode for ***merge(A, p, q , r)***:

```pseudocode
n1 = q - p + 1
n2 = r - q

let L[1 .. n1 + 1] and R[1 .. n2 + 1] be new arrays

// Copy the sub-arrays into L (left) and R (right)
for i = 1 to n1:
	L[i] = A[p + i - 1]
for j = 1 to n2:
	R[j] = A[q + j]

// Sentinel cards, basically end conditions
L[n1 + 1] = inf
R[n2 + 1] = inf

// Start checking
i = 1
j = 1
for k = p to r: // k is the index in the original array (i.e. A)
	if L[i] <= R[j]: // L has the smaller value between the two smallest values, that has NOT been copied back into A
		A[k] = L[i] // In-line replacement
		i = i + 1 // Move onto the next smallest value in L
	else:
		A[k] = R[j]
		j = j + 1
```

![merge_sort_merge](/Users/dliu/GitHub/algorithms/intro_to_algorithms/pics/merge_sort_merge.png)

Procedure ***merge_sort(A, p, r)***:

```pseudocode
if p < r: // If p >= r, then the subarray has at most one element and is therefore already sorted
	q = floor((p + r) / 2)
	merge_sort(A, p, q)
	merge_sort(A, q + 1, r)
	merge(A, p, q, r)
```

To sort the entire sequence A, we can make the initial call:

```pseudocode
merge_sort(A, 1, A.length)
```

![image-20190904105914916](/Users/dliu/GitHub/algorithms/intro_to_algorithms/pics/merge_sort.png)

Since the total number of levels is about $log_2{n} + 1$, and each level has cost n, the total runtime is O(nlogn).

## Run Time Comparison

| Algorithm | Best Case | Average Case | Worst Case |
| --------- | --------- | ------------ | ---------- |
| Insertion | O(n)      | O(n^2)       | O(n^2)     |
| Selection | O(n^2)    | O(n^2)       | O(n^2)     |
| Merge     | O(nlogn)  | O(nlogn)     | O(nlogn)   |
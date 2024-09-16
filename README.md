# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Recall that a good pivot is one that is located in the middle half for of the array when sorted.
Choosing a random pivot arbitrarily (including simply choosing the first element), you have a $\frac{\frac{n}{2}}{n} = 50\\%$ chance of choosing a good pivot.

Now consider picking the median of the first, middle, and last elements of an array. Let $L,M,H$ denote elements from the sorted array lower than the lower than the middle half of the array, in the middle half of the array, and higher than the middle half of the array respectively.
It should be noted that the odds of picking an element in $M$ is as likely as picking it from $L + H$. In other words $|M| = |H| + |L|$.

Consider the following cases for selecting the three elements for the median pivot:

1 permuation of - $L, L, L$ 
1 permuation of - $H, H, H$
1 permuation of - $M, M, M$  - Each one could be from the lower half or higher half of M, so there are 8 times the permutations of these  
6 permuations of - $L, M, H$  - The M could be from the lower half or higher half of M, so there are 2 times the permutations of these  
3 permuations of - $M, M, L$  - Each one could be from the lower half or higher half of M, so there are 4 times the permutations of these  
3 permuations of - $H, H, L$
3 permuations of - $H, H, M$  - The M could be from the lower half or higher half of M, so there are 2 times the permutations of these  
3 permuations of- $H, M, M$  - Each one could be from the lower half or higher half of M, so there are 4 times the permutations of these  
3 permuations of- $L, L, M$  - The M could be from the lower half or higher half of M, so there are 2 times the permutations of these  
3 permuations of - $L, L, H$

Adding all of them up we have $1+1+8+2\cdot6+4\cdot3+1\cdot3+2\cdot3+4\cdot3+2\cdot3+1\cdot3 = 64$ of them. 

### Cases Resulting in a Good Pivot

These cases will result in a good pivot:

1 permuation of - $M, M, M$  - Each one could be from the lower half or higher half of M, so there are 8 times the permutations of these  
6 permuations of - $L, M, H$  - The M could be from the lower half or higher half of M, so there are 2 times the permutations of these  
3 permuations of - $M, M, L$  - Each one could be from the lower half or higher half of M, so there are 4 times the permutations of these   
3 permuations of- $H, M, M$  - Each one could be from the lower half or higher half of M, so there are 4 times the permutations of these 

Adding up the ones that would result in a good pivot, $8 \cdot 1G + 2 \cdot 6 G + 4 \cdot 3 G + 4 \cdot 3 G = 18 G$.  
So the odds of getting a good pivot when choosing the median of three pivots is $\frac{44}{64} = 68.75 \\%$.

Median of the three has a $68.75 \\%$ chance of being a good pivot and picking the first element of the array has a $50\\%$ chance of being a good pivot. Using the median of three method is better.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

I wasn't sure how to get started if my original one was wrong so I looked at this one to see how to go about doing it. I just used the same online and notation for L and H as them though, the computations are my own. 
https://github.com/COSC3020/quicksort-pivot-ZachRenz.git
Edit: I used it to check my work because I kept getting $2/3$. Once I noticed that I should be using permutations not combinations, I did the calculations oall on my own.

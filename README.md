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
Choosing a random pivot arbitrarily (including simply choosing the first element), you have a $\frac{\frac{n}{2}}{n} = 50\%$ chance of choosing a good pivot.

Now consider picking the median of the first, middle, and last elements of an array. Let $L,M,H$ denote elements from the sorted array lower than the lower than the middle half of the array, in the middle half of the array, and higher than the middle half of the array respectively.
It should be noted that the odds of picking an element in $M$ is as likely as picking it from $L + H$. In other words $|M| = |H| + |L|$.

Now consider the possible combinations for the group that each of the three elements belong to,
$$
\begin{align}
L,&M,H\\
M,&M,L\\
M,&M,M\\
H,&H,L\\
H,&H,M\\
H,&M,M\\
L,&L,M\\
L,&L,H\\
\end{align}

$$


I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
I wasn't sure how to get started if my original one was wrong so I looked at htis one to see how to go about doing it. I 

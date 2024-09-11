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

For picking the first element for a randomized array, the odds of choosing a good pivot (an element that would be in the middle half when sorted) are $1/2$ because it will must be part of the middle $n/2$ elements. If we were to pick the median of the first,middle, and last elements, we know it would atleast have one element on either side of it in the sorted array. Thus the probability of the median element being a good pivot is 
$$
\begin{align}
P(\text{good pivot| median of three random elements}) &= 1 - P(\text{not a good pivot| median of three random elements})\\ 
&= 1 - \frac{(n - 2)}{2 \dot n} 
\end{align}
$$

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

## This document will answer some questions about the first part of this PSET

---

## What were your results from ```compare_cow_transport_algorithms```? Which algorithm runs faster? Why?

The Greedy Algorithm runs significantly faster because it doesn't go through the exhaustive enumeration of handling every piece of data and generating every combinations. The Greedy Method basically sorts the data according to a heuristic and then inside the loop it checks if our value is greater than our limit and if it is, it ignores that value and goes to the next one. On the contrary the Brute Force method generates every possible combination and looks which one takes the least amount of trip, the Greedy Method has a runtime of O(nlog(n)) (because of the sort). The Brute Force method needs to generate every subset O(2^n) and then for copy all of them for each subset which takes up O(n) time. Therefore, the total Time Complexity is O(n2^n). For my specific case, the greedy algorithm was instant showing 0 seconds to run and the library that I used can measure up to milliseconds so this means that my algorithm ran under a millisecond, however the brute force took around half a second to run. Although, this difference might seem trivial, I ran this on a small dataset and still the difference was so large, so you can imagine running this on a large dataset would cause a huge difference

---

## Does the greedy algorithm return the optimal solution? Why/why not?

The problem with the greedy method is that it does not always return the optimal solution, it finds the local minimum and maximum, however the local minimum or maximum might not always lead to the global minimum or maximum. Let's use an example to illustrate that, for example imagine if we have a backpack of capacity 15 and we have items of weight [2,5,12,10]. Following the Greedy method, we would take 12 and then 2 (we cannot take 10 after 12, becasue the bag would overflow, for the same reason we cannot take 5 as well). Therefore, our max capacity we would fill is 14. However, if we take the value 10 and 5, we could easily reach 15, but the Greedy method just does not give us that. This is a counter example.

---

## Does the brute force algorithm return the optimal solution? Why/why not?

Yes, because for the brute force method we generate all the possible combinations and then we go through every combination and only select the one that has the best value while respecting to the constraint ie the optimal solution for the optimization problem



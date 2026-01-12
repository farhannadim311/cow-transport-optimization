## This document will answer some questions about the first part of this PSET

---

## What were your results from ```compare_cow_transport_algorithms```? Which algorithm runs faster? Why?

The Greedy Algorithm runs significantly faster because it doesn't go through the exhaustive enumeration of handling every piece of data and generating every combinations. The Greedy Method basically sorts the data according to a heuristic and then inside the loop it checks if our value is greater than our limit and if it is, it ignores that value and goes to the next one. On the contrary the Brute Force method generates every possible combination and looks which one takes the least amount of trip, the Greedy Method has a runtime of O(nlog(n)) (because of the sort). The Brute Force method needs to generate every subset O(2^n) and then for copy all of them for each subset which takes up O(n) time. Therefore, the total Time Complexity is O(n2^n)

---

## Does the greedy algorithm return the optimal solution? Why/why not?

The problem with the greedy method is that it does not always return the optimal solution, it finds the local minimum and maximum, however the local minimum or maximum might not always lead to the global minimum or maximum. Let's use an example to illustrate that, for example imagine if we have a backpack of capacity 15 and we have items of weight [2,5,12]. Following the Greedy method, we would take 12 and then 2 (we cannot take 5 after 12, becasue the bag would overflow, for the same reason we cannot take 12 again as well). Therefore, our max capacity we would fill is 14. However, if we take the value 5 3 times, we can fill the entire capacity of the bag as 5 * 3 = 15.

---


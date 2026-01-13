## Explain why it would be difficult to use a brute force algorithm to solve this problem if there were 30 different egg weights. You do not need to implement a brute force algorithm in order to answer this.

If we were to use 30 different eggs, there would be a lot of combinations that we would have to go through. For each weight, we would look through every possible combination and see if it reaches the target, so the time complexity would be the weight^30, which is really bad.

---

## If you were to implement a greedy algorithm for finding the minimum number of eggs needed, what would the objective function be? What would the constraints be? What strategy would your greedy algorithm follow to pick which coins to take? You do not need to implement a greedy algorithm in order to answer this.

My objective function is to find the minimum number of eggs needed to make a given capacity. My constraint would be the target weight as I cannot exceed that. The strategy would be to pick the biggest weight as many times as possible and if doing that exceeds the target, pick the next best possible weight which does not exceed the target and add that to the weight. If we reach a zero that means we reached a greedy solution, however if we go negative that means that the greedy solution does not even give us a solution.

---

## Will a greedy algorithm always return the optimal solution to this problem? Explain why it is optimal or give an example of when it will not return the optimal solution. Again, you do not need to implement a greedy algorithm in order to answer this.

No infact there might be cases where a solution would exist but Greedy will not even give one and also there will be cases where greedy will give us a solution but not the optimal one. Let's look at an example of the latter. Suppose this is the list [1,3,4,5] and our target is 7. The optimal solution is 4,3, therefore 2. However, if we did Greedy then we would choose 5, we have 2 remaining from our target. We can't choose 3 or 4 as that exceeds the target now, so we choose 1 two times, giving us 3 as the result. This is not the optimal solution. Similarly, if we did this [6,3,4,5], Greedy would not even give us a valid solution as we would pick 6 at first and then realise if we sum anything else up to 6, we would exceed the target
# Optimization & Dynamic Programming (MIT 6.0002)

This repository contains my Python solutions for **MIT 6.0002 (Introduction to Computational Thinking and Data Science)**, Problem Set 1. The project focuses on solving combinatorial optimization problems using Greedy algorithms, Brute Force search, and Dynamic Programming with memoization.

## 📂 Project Structure

**Part A (Space Cows):** Solves a variation of the Bin Packing Problem using both heuristic and exhaustive search methods to transport "cows" with weight constraints
**Part B (Golden Eggs):** Solves a variation of the Knapsack/Change-Making problem using Dynamic Programming to minimize resources (eggs) needed to meet a precise weight target

## 🛠️ Key Algorithms Implemented

### 1. Greedy Heuristic (`greedy_cow_transport`)
**Strategy:** Iteratively selects the heaviest available item (cow) that fits within the remaining capacity of the current transport "trip" 
* **Complexity:** $O(N^2)$ (sorting + linear scan per trip).
**Trade-off:** Extremely fast execution but does not guarantee a globally optimal solution

### 2. Brute Force Search (`brute_force_cow_transport`)
**Strategy:** Enumerates every possible partition of the set of cows to find the one requiring the minimum number of trips 
**Implementation:** Utilizes a generator to yield set partitions 
* **Complexity:** Exponential $O(B_n)$ (Bell number), making it intractable for large datasets but guaranteed to find the optimal solution.

### 3. Dynamic Programming (`dp_make_weight`)
**Strategy:** Uses recursion with **memoization** to solve the minimization problem for transporting "Golden Eggs"
* **Logic:** Deconstructs the problem into optimal substructures: $Cost(w) = 1 + min(Cost(w - egg\_weight))$ for all valid eggs.
* **Performance:** Reduces time complexity from exponential (Brute Force) to pseudo-polynomial $O(W \cdot N)$, where $W$ is the target weight and $N$ is the number of egg types.

## 🚀 Usage

### Prerequisites
* Python 3.5+
* No external dependencies required (uses standard library `time`, `copy`, etc.).

### Running Part A (Transport Optimization)
Compare the execution time and efficiency of Greedy vs. Brute Force:
```bash
python3 ps1a.py
```

runs the ```dp_make_weight``` function against test cases to verify optimal resource allocation.

### Running Part B (DP Optimization)
Compare the execution time and efficiency of Greedy vs. Brute Force:
```bash
python3 ps1b.py
```



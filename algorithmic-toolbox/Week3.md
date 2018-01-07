# Week 3
## Greedy algorithms
### Car fueling problem
Example problem: the car fueling problem

> You have a car such that if you fill it up to full tank, you can travel with it up to 400 kilometers without refilling it. And you need to get from point A to point B, and the distance between them is 950 kilometers. Of course, you need to refill on your way, and luckily, there are a few gas stations on your way from A to B. These are denoted by blue circles, and the numbers above them mean the distance from A to the corresponding gas station along the way from A to B. And you need to find the minimum number of refills to get from A to B. 

The greedy solution is to always travel to the farthest reachable gas station.

This example already shows us the gist of greedy algorithms: you haave a big problem, you make a greedy choice that then leaves you with a subproblem, you do another greddy choice, ... , until you have no problem left.

In a greedy algorithm a move is called safe if it's the first move of an optimal solution.

### Grouping children
> you need to divide children into the minimum possible number of groups. Such that the age of any two children in any group differs by at most one year. 

The greedy solution is to start by the youngest child, create a group containg him and everybody else in a 1-year range, this is your first group, the remaining children are the sub-problem.

### Fractional Knapsack
> We have n items with weights $w_1$ through $w_n$ and values $v_1$ though $v_n$ And a bag of capacity big W. And we want to maximize the total value of fractions of items that fit into this bag. 

We can take any fraction of any item.

The greedy algorithm is to always take the maximum amount of the item that has the maximum $\frac{\text{value}}{\text{weight}}$, the maximum amount is either the whole item if it fits in the knapsack or the amount correspondig to the space left in the knapsack.


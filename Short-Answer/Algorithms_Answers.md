#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) O(n)
Explanation: We can focus on the while loop only running for amount of times on n (this case n^3 for n times n times n). Because coeffients are dropped, just O(n). O(n) is linear time, while n increase, time increases. So if n is small, will take smaller time. If n is bigger, n will take longer running time.

b) O(n log(n))
Explanation: We can focus on the two loops within the function. Fist, they're nested. The outer one is what we usually see of n increasing steadily by n. The inner one, is different as j is being multiplied by 2 giving us j being doubled until n (log n). For example when looking at n as 10, it will loop through as 2, 4, 8, and start again at the next i when it hits 16 (because 16 (j) is not less than n (10)).

c)O(n)
Explanation: This function is recursive thus dependent on n. The bigger n, the more time it will run until it reaches 0.

## Exercise II

Have: n-story building and plenty of eggs.

Egg gets broken if thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f.

Devise a strategy to determine: the value of f
such that the number of dropped + broken eggs is minimized.

## Proposed algorithm in plain English or pseudocode:

I would take a binary search approach. In order to do a binary search, your data has to be sorted but since floors in a building are sorted, I would not have to worry about sorting them first. I can start in the middle most floor of the building or (n/2, n being the number of floors in the building) and drop an egg. If the egg breaks, I can focus on the bottom half of the building. If it does not, I can focus on the floors above. This plan should minimize the number of eggs I drop and number of broken eggs.

## AND give the runtime complexity of your solution:

My solution is a binary search, which has a runtime complexity of O(log n). It increases by a constant, if n doubles the runtime increases by constant that is smaller than n.

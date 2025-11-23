# NP (Nondeterministic Polynomial Time)

Saturday, November 22, 2025

## What does NP mean?

A set of problems that can be  __verified in polynomial time__ if the answer is __yes__.

### Example: Traveling Salesman

Can I visit all _x_ cities just once and have the total length of the route be less than 1,000 miles?

If the answer is YES, you can easily prove that answer.  You add up the miles between each city and check if the sum is less than 1,000 miles.

If the answer is NO, there might not be a succinct way to communicate that fact.

This is an example of an __NP-Complete__ problem.  It is _exponentially_ hard to find a solution, but it only takes _polynomial_ time to evaluate the proposed solution.
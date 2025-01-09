# JavaScript Closure Issue in `setTimeout` Loop

This repository demonstrates a common JavaScript closure issue related to using `setTimeout` within a loop.  The problem is that the `setTimeout` callback doesn't capture the value of `i` at the time of its creation, but rather captures a reference to the `i` variable itself.

**Bug:** The `bug.js` file contains the buggy code which demonstrates this problem.  The expected behavior would be to print the numbers 0 through 9, each after a one-second delay. However, due to the closure issue, the code will print the final value of `i` (10) ten times.

**Solution:** The `bugSolution.js` file provides a corrected version that utilizes an immediately invoked function expression (IIFE) to create a separate scope for each iteration of the loop.  This ensures that the correct value of `i` is captured for each callback. 

**How to Run:**
1. Clone the repository
2. Navigate to the repository's directory in your terminal
3. Execute `node bug.js` to see the incorrect behavior
4. Execute `node bugSolution.js` to see the corrected behavior.
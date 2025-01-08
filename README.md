# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop.  The problem stems from how closures capture variables from their surrounding scope.

## The Bug
The `bug.js` file contains a function `myFunction` that uses a `for` loop and `setTimeout` to log the value of `i` after a 1-second delay.  The expected output would be numbers 0 through 9, each printed after a one-second delay. However, due to the closure issue, all instances of the `setTimeout` callback function end up capturing the final value of `i` (which is 10) after the loop finishes.

## The Solution
The `bugSolution.js` file provides a corrected version of the code using an immediately invoked function expression (IIFE) or `let` to create a new scope for each iteration, ensuring that each closure captures a distinct value of `i`.

## How to run the code
1. Clone the repository.
2. Open `bug.js` and `bugSolution.js` in a text editor or IDE.
3. Run each file in a JavaScript environment (e.g., a browser's console or Node.js).
4. Observe the differences in output.
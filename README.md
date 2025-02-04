# Julia Bug: Unexpected Floating-Point Result in Conditional Function

This repository demonstrates a subtle bug in a seemingly simple Julia function. The function aims to return the square of the input, making it negative if the input is negative. However, it unexpectedly returns a floating-point zero (0.0) instead of an integer zero (0) when the input is 0.

## Bug Description
The `myfunction` function calculates the square of the input, negating it if the input is negative.  The unexpected behavior occurs when the input is 0; the function returns `0.0` instead of `0`.

## How to Reproduce
1.  Clone this repository.
2.  Run `bug.jl` using the Julia REPL.
3.  Observe the output for inputs 2, -2, and 0.

## Solution
The `bugSolution.jl` file contains a corrected version of the function that addresses the issue by explicitly handling the case where x is 0. This ensures the consistent return of an integer type.
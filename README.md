# Tcl == Operator Pitfall

This repository demonstrates a common, subtle error in Tcl related to the `==` operator.  The `==` operator in Tcl performs string comparison, not numerical comparison. This means that `1 == 1` evaluates to true, but `1 == "1"` evaluates to false.  This can lead to unexpected results in code that handles numbers that might be passed in as strings. The example shows how this can lead to incorrect program logic and how to avoid such issues.

## How to reproduce:

1. Clone this repository.
2. Open `bug.tcl` and run the code.
3. Note the unexpected result of the second comparison.
4. Open `bugSolution.tcl` to see how to correct the issue.

## Solution:
The solution involves using the `expr` command to explicitly perform numerical comparison.
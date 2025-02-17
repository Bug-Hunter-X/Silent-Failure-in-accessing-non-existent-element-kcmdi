# Silent Failure in accessing non-existent element
This repository demonstrates a subtle bug in HTML where attempting to access a non-existent element using Javascript leads to a silent failure, without any error messages.

The bug is in `bug.html`.  The solution is in `bugSolution.html`.

The problem is that accessing a non-existent element with `document.getElementById()` returns `null`.  Attempting to set the `innerHTML` of `null` will cause no error to be thrown but the change will not occur.

## Solution
The solution involves checking if the element exists before attempting to modify it.
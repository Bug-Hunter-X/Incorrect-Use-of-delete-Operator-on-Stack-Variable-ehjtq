# Incorrect Use of delete Operator on Stack Variable

This repository demonstrates a common C++ error: attempting to use the `delete` operator on a variable allocated on the stack.  This can lead to undefined behavior, crashes, or memory corruption.

The `bug.cpp` file contains the erroneous code.  The `bugSolution.cpp` file shows the corrected version.

**Bug:**  The `delete` operator should only be used for dynamically allocated memory (memory allocated using `new`). Stack variables, like the integer `x` in the example, are automatically deallocated when they go out of scope.

**Solution:**  Avoid using `delete` on stack variables.  If dynamic memory is required, use `new` to allocate it and `delete` to deallocate it when finished.
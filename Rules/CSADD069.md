# CSADD069 - Only Initialize in Init method

**Severity:** ![Error](images/Error.png) Error

Reports when `Init()`, `ctor()` or `__Init()` is called on a field of a `struct` attributed with `[Structure]` outside its `Init()` method.

## Solution

You can also use the provided automatic Code Fix to remove the method call. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu)

Remove the method call.
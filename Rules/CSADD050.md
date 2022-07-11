# CSADD050 - Input or Output fields and parameters shall not be pointers

**Severity:** ![Error](../images/Error.png) Error

Checks `[Input]` and `[Output]` attributes, when their field/parameter is a pointer type a diagnostic is reported

## Solution

Change the type to a type that is not a pointer.
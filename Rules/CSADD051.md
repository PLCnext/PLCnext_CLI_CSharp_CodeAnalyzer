# CSADD051 - Structures must not have Any or Pointer fields

**Severity:** ![Error](../images/Error.png) Error

Checks `struct`s with the attributes `[Structure]`, reports a diagnostic for each field that is of type `Any` or a pointer type.

## Solution

Change the field type.
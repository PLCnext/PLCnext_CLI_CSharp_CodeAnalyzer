# CSADD023 - Program port types must not be of an Any type or a structure with Any type fields

**Severity:** ![Error](../images/Error.png) Error

Fields with the attributes `[InPort]` or `[OutPort]` must not have the type `Any` or a `struct`s attributed with `[Structure]`, `[Array]` or `[String]` that has a field of type `Any`.

## Solution

Remove the attribute or change the data type to resolve the diagnostic.

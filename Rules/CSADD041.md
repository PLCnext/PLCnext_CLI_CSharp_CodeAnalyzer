# CSADD041 - Init/ctor must only be called once in Init or __Init

**Severity:** ![Error](../images/Error.png) Error

The `__Init()` method (in classes attributed with `[FunctionBlock]`) and the `Init()` method of a user type (`struct` 's attributed with `[Structure]`, `[Array]` or `[String]`) must only call `ctor()`/`Init()` once on their fields.

## Solution

You can also use the provided automatic Code Fix to remove the duplicate calls to `ctor()`/`Init()` methods on a field. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the duplicate calls to `ctor()`/`Init()` on a field.
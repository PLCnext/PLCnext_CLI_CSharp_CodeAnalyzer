# CSADD022 - Return types must not be of an Any type or a structure

**Severity:** ![Error](../images/Error.png) Error

Return types of IEC methods/functions must not be of the type `Any` or a user type (`struct`s attributed with `[Structure]`, `[Array]` or `[String]`).
IEC methods/functions that can have return values are methods that either:

* have the attribute `[User]`
* have the attribute `[Execution]`, are called `__Process` and are in a class with the attribute `[Function]`
* have the attribute `[Function]` and are in a class with the attribute `[FunctionContainer]`

## Solution

You can also use the provided automatic Code Fix to convert the return type into an `[InOut]` parameters. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Convert the return to a parameter attributed with `[InOut]`.
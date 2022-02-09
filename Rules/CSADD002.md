# CSADD002 - Name of POU type is too long

**Severity:** ![Error](../images/Error.png) Error

Names are only allowed to have up to 90 characters.

Checks the name of:

* classes with the attribute `[Function]`, `[FunctionBlock]` or `[Program]`
* structs with the attribute `[Structure]`, `[Array]` or `[String]`
* methods with the attribute `[User]` or `[Function]`
* fields or parameters with the attribute `[Input]`, `[Output]`, `[InOut]`, `[InPort]` or `[OutPort]`


## Solution

Shorten the name to max. 90 characters.

# CSADD060 - Only use Hidden on user defined data types and POUs

**Severity:** ![Error](../images/Error.png) Error

Checks all `[Hidden]` attributes, reports if not used on:
* `struct`s attributed with `[Array]`, `[Structure]` or `[String]`
* or `enum`s attributed with `[Enumeration]`
* or `class`es attributed with `[Function]`, `[FunctionBlock]`, `[FunctionContainer]` or `[Program]`

## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the attribute or meet the attribute's requirements named above.
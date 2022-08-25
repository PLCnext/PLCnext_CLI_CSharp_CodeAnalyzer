# CSADD063 - Only use Native where possible

**Severity:** ![Error](../images/Error.png) Error

Reports usages of the attribute `[Native] if it is not used:
- on a `class` attributed with `[Function]`
- or on a `class` attributed with `[FunctionContainer]`
- or on a `class` attributed with `[FunctionBlock]`
- or on a `class` attributed with `[Program]`
- or on a method

## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the attribute or meet the attribute's requirements named above.
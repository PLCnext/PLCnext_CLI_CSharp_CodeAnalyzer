# CSADD053 - GdsRetain should only be used in FB or Program

**Severity:** ![Error](../images/Error.png) Error

Checks the attribute `[GdsRetain]`, reports a diagnostic if it is not inside a class attributed with `[FunctionBlock]` or `[Program]`.

## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the attribute.
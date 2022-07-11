# CSADD061 - Only use NotOverridable on POUs

**Severity:** ![Error](../images/Error.png) Error

Checks all `[NotOverridable]` attributes, reports if not used on classes attributed with `[Function]`, `[FunctionBlock]`, `[FunctionContainer]` or `[Program]`.

## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the attribute or meet the attribute's requirements named above.
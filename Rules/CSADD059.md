# CSADD059 - Only use Retaining where possible

**Severity:** ![Error](../images/Error.png) Error

Reports if the attribute `[Retain]` or `[GdsRetain]` is used apart from fields of classes attributed with `[Program]` or `[FunctionBlock]`. The fields must not have the attributes `[Input]` or `[InOut]`.

## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the attribute or meet the attribute's requirements named above.
# CSADD062 - Only use OPC, Ehmi, ProfiCloud and Redundant where possible

**Severity:** ![Error](../images/Error.png) Error

Checks all `[OPC]`, `[Ehmi]`, `[ProfiCloud]` and `[Redundant]` attributes, reports if one is not:

    on fields of classes attributed with `[FunctionBlock]` or `[Program]`
    being of primitive or string/wstring type

## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the attribute or meet the attribute's requirements named above.
# CSADD045 - Output parameter must be ref or out

**Severity:** ![Error](../images/Error.png) Error

Any parameter with the attribute `[Output]` must have either the modifier `ref` or `out`.


## Solution

You can also use the provided automatic Code Fix to add the `out` modifier to the parameter. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 


Add the `out` (or `ref`) modifier to the parameter.
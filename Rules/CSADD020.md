# CSADD020 - Methods attributed Execution or Initialization are not allowed to have parameters

**Severity:** ![Error](../images/Error.png) Error

Methods with the attribute `[Execution]` or `[Initialization]` in classes attributed with `[FunctionBlock]` or `[Program]` must not have parameters.

## Solution

You can also use the provided automatic Code Fix to remove the parameters. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 


Remove the parameters.
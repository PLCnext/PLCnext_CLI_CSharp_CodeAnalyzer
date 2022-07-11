# CSADD048 - Only use Initialization and Execution in FB and Program

**Severity:** ![Error](../images/Error.png) Error

Checks the attributes `[Initialization]` and `[Execution]`, reports a diagnostic if they are not inside a class attributed with `[FunctionBlock]` or `[Program]`.

## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 


Remove the attribute.
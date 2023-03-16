# CSADD070 - Only use Invisible where possible

**Severity:** ![Error](images/Error.png) Error

Reports the usage of the `[Invisible]` attribute if it is not on fields attributed with `[Input]`, `[Output]` or `[InOut]` inside `class`es attributed with `[FunctionBlock]`.

## Solution

You can also use the provided automatic Code Fix to remove the `[Invisible]` attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the `[Invisible]` attribute.
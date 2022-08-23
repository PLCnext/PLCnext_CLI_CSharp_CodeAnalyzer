# CSADD001 - Old Attributes are not allowed

**Severity:** ![Warning](../images/Warning.png) Warning

The following attributes are deprecated and should not be used anymore:

* `[VAR_INPUT]`
* `[VAR_IN_OUT]`
* `[VAR_OUTPUT]`
* `[FUNCTION_BLOCK]`
* `[FUNCTION]`
* `[PROGRAM]`

## Solution

You can also use the provided automatic Code Fix to replace the attributes with the new equivalents. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Replace the attributes with their new equivalent:

* `[VAR_INPUT]` --> `[Input]`
* `[VAR_IN_OUT]` --> `[InOut]`
* `[VAR_OUTPUT]` --> `[Output]`
* `[FUNCTION_BLOCK]` --> `[FunctionBlock]`
* `[FUNCTION]` --> `[Function]`
* `[PROGRAM]` --> `[Program]`
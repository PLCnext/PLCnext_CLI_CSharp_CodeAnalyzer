# CSADD018 - Structure fields should be pointers

**Severity:** ![Warning](../images/Warning.png) Warning

Checks fields with the attributes `[Output]`, ` [Input]`, `[InOut]`, `[InPort]` or `[OutPort]` when the field type is a struct that was declared with `[Structure]` or `[Array]` attribute.
These fields should be pointers with the `[InOut]` parameter to improve the performance.

The field is reported if:
- it is not a pointer type
- or it does not have the `[InOut]` parameter

## Solution

You can also use the provided automatic Code Fix to change the type to pointer and change the attribute to `[InOut]`. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 



Change the type to be a pointer and change the attribute to `[InOut]`. Don't forget to refactor the references.
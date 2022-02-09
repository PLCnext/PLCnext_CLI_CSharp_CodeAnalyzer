# CSADD019 - Functions are not allowed to have attributed fields

**Severity:** ![Error](../images/Error.png) Error

Classes with the attribute `[Function]` are not allowed to have fields attributed with `[Output]`, ` [Input]` or `[InOut]`.


## Solution

You can also use the provided automatic Code Fix to remove the attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 


Remove the attribute. If the field is intended to be an `[Input]` parameter for the IEC `[Function]` make it an `[Input]` parameter of the method where it is used.
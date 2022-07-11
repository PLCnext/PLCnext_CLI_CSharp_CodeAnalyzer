# CSADD055 - Strings must not have fields apart from the IecStringEx s field

**Severity:** ![Error](../images/Error.png) Error

Checks all `struct`s attributed with `[String]`, if they have fields apart from the `IecStringEx s` field a diagnostic is reported.

## Solution

You can also use the provided automatic Code Fix to remove the field. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the field.
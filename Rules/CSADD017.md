# CSADD017 - Structure fields should be InOut

**Severity:** ![Suggestion](../images/Suggestion.png) Suggestion

Fields that are of user types (`struct`s attributed with `[Structure]`, `[Array]` or `[String]`) should not be attributed with ` [Input]` or `[Output]`.
A better performance is possible using the attribute `[InOut]` which uses call by reference.

## Solution

You can also use the provided automatic Code Fix to change the attribute to `[InOut]`. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Change the attribute to `[InOut]`.
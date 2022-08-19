# CSADD040 - Structure parameters should be ref Output

**Severity:** ![Suggestion](../images/Suggestion.png) Suggestion

Parameters that are of user types (`struct`s attributed with `[Structure]`, `[Array]` or `[String]`) should not be attributed with ` [Input]` or `[InOut]` and they should have a `ref` keyword.
A better performance is possible using the attribute `[Output]` and `ref` which uses call by reference.

## Solution

You can also use the provided automatic Code Fix to change the attribute to `[Output]` and/or add the keyword `ref`. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Change the attribute to  `[Output]` and/or add the keyword `ref`.
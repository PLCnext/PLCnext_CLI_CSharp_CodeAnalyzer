# CSADD040 - Structure parameters should use ref

**Severity:** ![Suggestion](../images/Suggestion.png) Suggestion

Parameters that are of user types (`struct`s attributed with `[Structure]`, `[Array]` or `[String]`) attributed with `[Input]`, `[Output]` or `[InOut]` should have a `ref` keyword.
A better performance is possible using the `ref` keyword which uses call by reference.

## Solution

You can also use the provided automatic Code Fix to add the keyword `ref`. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Add the keyword `ref`.
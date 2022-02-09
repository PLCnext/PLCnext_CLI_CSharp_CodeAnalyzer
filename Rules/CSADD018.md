# CSADD018 - Structure fields should be pointers

**Severity:** ![Warning](../images/Warning.png) Warning

Fields attributed with `[Output]`, ` [Input]` or `[InOut]`, `[InPort]` or `[OutPort]` of a user type (`struct`s attributed with `[Structure]`, `[Array]` or `[String]`) should be pointers to these types instead to improve the performance.

## Solution

You can also use the provided automatic Code Fix to change the type to pointers. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 



Change the type to be a pointer. Don't forget to refactor the references.
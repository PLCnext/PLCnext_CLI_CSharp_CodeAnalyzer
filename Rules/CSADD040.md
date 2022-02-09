# CSADD040 - Only Init methods of pointer arrays may be unsafe

**Severity:** ![Warning](../images/Warning.png) Warning

The `Init()` method of a user type (`struct` 's attributed with `[Structure]`, `[Array]` or `[String]`) should not be `unsafe`.
`[Array]`s that have a pointer type `Anchor` field are an exception to this rule.

## Solution

You can also use the provided automatic Code Fix to remove the `unsafe` keyword. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 


Remove the `unsafe` keyword.
# CSADD038 - Init Methods of user types must not have an Initialization attribute

**Severity:** ![Warning](../images/Warning.png) Warning

The `Init()` method of a user type (`struct` 's attributed with `[Structure]`, `[Array]` or `[String]`) must not be attributed with `[Initialization]`.

## Solution

You can also use the provided automatic Code Fix to remove the `[Initialization]  ` attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the  `[Initialization]  ` attribute.
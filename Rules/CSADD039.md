# CSADD039 - User type Init methods must not have parameters

**Severity:** ![Error](../images/Error.png) Error

One `Init()` method of a user type (`struct` 's attributed with `[Structure]`, `[Array]` or `[String]`) must not have parameters.

## Solution

You can also use the provided automatic Code Fix to remove the parameters. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Remove the parameters from one `Init()`method.
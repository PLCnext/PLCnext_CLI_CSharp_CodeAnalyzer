# CSADD027 - IEC Structure and all its fields have to be public

**Severity:** ![Error](../images/Error.png) Error

All `struct`s with the attribute `[Structure]` have to be `public`. All fields of the `struct`  have to be `public` as well (exception `const` or `static` fields).

## Solution

You can also use the provided automatic Code Fix to make the `struct`  and its fields `public`. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Make the `struct` and its fields `public`.
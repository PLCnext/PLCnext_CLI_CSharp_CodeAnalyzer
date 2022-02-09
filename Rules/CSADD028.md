# CSADD028 - String length and size have to be correct

**Severity:** ![Error](../images/Error.png) Error

The size of user strings has to be correct. `struct`s with the attribute `[String]` have to fulfill:
* The `maximumLength` of the string's `IecStringEx` field (set in `Init()` ) has to be equal to the first parameter (size) of the `[String]` attribute.
* The `Size` parameter of the `StructLayout` attribute has to be 6 greater than the first parameter (size) of the `[String]` attribute.

Also see the `[String]` pattern [CSADD026](CSADD026.md) asks for.

You can also view an [explanation and example of a string implementation on Gitub](https://github.com/PLCnext/CSharpExamples/blob/master/PLCnext_CSharpExamples/05_IECString/IECString.md)

## Solution

You can also use the provided automatic Code Fix to adjust the sizes to the definition in the `[String]` attribute. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Assign the `size` defined in the `[String]` attribute to the `IecStringEx` field. Set it increased by 6 as the `[StructLayout]` attribute's `Size` parameter.
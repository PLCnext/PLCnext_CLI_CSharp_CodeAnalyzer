# CSADD025 - IEC Array pattern has to be correct

**Severity:** ![Error](../images/Error.png) Error

All `struct`s with the attribute `[Array]` must have these elements:
* attribute: `[ArrayDimension]`
* attribute (with Size parameter): `[StructLayout(Size=x)]`
* Anchor declaration: 
	```c#
	[FieldOffset(0)]
	public <here has to be the array type> Anchor;
	```
* lower bound declaration:
    ```c#
    public const int LB = <here has to be the value>;
    ```
*  upper bound declaration:
    ```c#
    public const int UB = <here has to be the value>;
    ```

## Solution

You can also use the provided automatic Code Fix to add all missing elements. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Provide all missing elements.
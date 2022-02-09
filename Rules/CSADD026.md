# CSADD026 - IEC String Pattern has to be correct

**Severity:** ![Error](../images/Error.png) Error

All `struct`s with the attribute `[String]` must have these elements:
* attribute (with Size parameter): `[StructLayout(LayoutKind.Explicit, Size = <value + 6>)]`
* IecStringEx declaration: 
	```c#
	[FieldOffset(0)]
	public IecStringEx s;
	```
* `Init` method that sets the `minimumLength`:
    
    ```c#
	public void Init()
	{
		s.maximumLength = <value>;
    }	
	```
	

You can also view an [explanation and example of a string implementation on Gitub](https://github.com/PLCnext/CSharpExamples/blob/master/PLCnext_CSharpExamples/05_IECString/IECString.md)
## Solution

You can also use the provided automatic Code Fix to add all missing elements. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Provide all missing elements.
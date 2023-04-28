# CSADD044 - Output parameter name unequal to method name

**Severity:** ![Error](../images/Error.png) Error

The parameter must have the same name as the method.
It applies when this is the case:

* inside a `class` attributed with `[FunctionContainer]`
* method attributed with `[Function]`
* first parameter has attribute `[Output]` or the keyword `ref` or the keyword `out`
* return value of method is
	* either
		* `void`
	* or
		* `bool`
		* and the method has the attribute `[Eno]` ( [see this GitHub example for an explanation of Eno](https://github.com/PLCnext/CSharpExamples/blob/master/PLCnext_CSharpExamples/13_EN_ENO/EN_ENO.md) )
* the name of the parameter is different than the method name




## Solution

You can also use the provided automatic Code Fix to rename the parameter. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 


Rename the parameter to match the method name (or the other way round).
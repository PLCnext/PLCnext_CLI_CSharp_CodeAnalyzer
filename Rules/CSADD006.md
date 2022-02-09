# CSADD006 - Parameter type has to be IEC compaible

**Severity:** ![Error](../images/Error.png) Error

All parameters (attributed with `[Output]`, ` [Input]` or `[InOut]`) of IEC methods/functions have to be compatible with IEC.

IEC methods/functions that can have parameters are methods that either:
* have the attribute `[User]`
* have the attribute `[Execution]`, are called `__Process` and are in a class with the attribute `[Function]`
* have the attribute `[Function]` and are in a class with the attribute `[FunctionContainer]`

**Explicitly allowed types are**

CSharp basic types:

* `bool`
* `sbyte`
* `short`
* `int`
* `long`
* `byte`
* `ushort`
* `uint`
* `ulong`
* `float`
* `double`

.Net basic types:

* `Boolean`
* `SByte`
* `Int16`
* `Int32`
* `Int64`
* `Byte`
* `UInt16`
* `UInt32`
* `UInt64`
* `Single`
* `Double`

IEC types:

* `IecStringEx`
* `IecString80`
* `IecWString`
* `IecWString80`
* `Any`
* Structures attributed with `[Structure]`, `[Array]` or `[String]`
* `enums` attributed with `[Enumeration]`

## Solution

Change the parameter type to one of the explicitly allowed types.

# CSADD007 - Field type has to be IEC compatible

**Severity:** ![Error](../images/Error.png) Error

All fields attributed with `[Local]`, `[Output]`, `[Input]`, `[InOut]`, `[InPort]` or `[OutPort]` have to be of a type compatible with IEC.

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

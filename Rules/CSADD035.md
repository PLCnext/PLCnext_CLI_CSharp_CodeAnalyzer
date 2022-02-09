# CSADD035 - Structure field type has to be IEC compatible

**Severity:** ![Error](../images/Error.png) Error

Checks user `[Structure]`s (`struct`s with the attribute `[Structure]`).
All fields have to be of a type that is compatible with IEC.

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
* Structures attributed with `[Structure]`, `[Array]` or `[String]`
* `enums` attributed with `[Enumeration]`

## Solution

Change the field type to one of the explicitly allowed types.


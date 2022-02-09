# CSADD011 - Return type needs correct DataType attribute

**Severity:** ![Error](../images/Error.png) Error

The `[DataType]` attribute of IEC methods/functions has to fit to the return type.

IEC methods/functions that can have return values are methods that either:
* have the attribute `[User]`
* have the attribute `[Execution]`, are called `__Process` and are in a class with the attribute `[Function]`
* have the attribute `[Function]` and are in a class with the attribute `[FunctionContainer]`

If either
* the return type is `void`
* or the return type is bool and the method has the attribute `[Eno]` ( [see this GitHub example for an explanation of Eno](https://github.com/PLCnext/CSharpExamples/blob/master/PLCnext_CSharpExamples/13_EN_ENO/EN_ENO.md) )

and the first parameter

* has the `out` modifier
* or has `ref` modifier
* or has the attribute `[Output]`

the parameter type is checked instead of the return type.


The Correct mapping is shown inside the Readme.txt of each VS Template and looks like this:

| IEC 61131-3         | .NET Framework                   | C#       |
| ------------------- | -------------------------------- | -------- |
|    `BOOL`           | `System.Boolean`                 | `bool`   |
|    `SINT`           | `System.SByte`                   | `sbyte`  |
|    `INT`            | `System.Int16`                   | `short`  |
|    `DINT`           | `System.Int32`                   | `int`    |
|    `LINT`           | `System.Int64`                   | `long`   |
|    `USINT`          | `System.Byte`                    | `byte`   |
|    `UINT`           | `System.UInt16`                  | `ushort` |
|    `UDINT`          | `System.UInt32`                  | `uint`   |
|    `ULINT`          | `System.UInt64`                  | `ulong`  |
|    `REAL`           | `System.Single`                  | `float`  |
|    `LREAL`          | `System.Double`                  | `double` |
|    `TIME`           | `System.Int32`                   | `int`    |
|    `LTIME`          | `System.Int64`                   | `long`   |
|    `LDATE`          | `System.Int64`                   | `long`   |
|    `LTIME_OF_DAY`   | `System.Int64`                   | `long`   |
|    `LDATE_AND_TIME` | `System.Int64`                   | `long`   |
|    `BYTE`           | `System.Byte`                    | `byte`   |
|    `WORD`           | `System.UInt16`                  | `ushort` |
|    `DWORD`          | `System.UInt32`                  | `uint`   |
|    `LWORD`          | `System.UInt64`                  | `ulong`  |
|    `STRING`         | `System.Iec61131Lib.IecStringEx` | -------- |
|    `STRING`         | `System.Iec61131Lib.IecString80` | -------- |
|    `WSTRING`        | `System.Iec61131Lib.IecWString`  | -------- |
|    `WSTRING`        | `System.Iec61131Lib.IecWString80`| -------- |
|    `ANY`            | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_MAGNITUDE`  | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_NUM`        | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_INT`        | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_SIGNED`     | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_UNSIGNED`   | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_REAL`       | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_BIT`        | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_ELEMENTARY` | `System.Iec61131Lib.Any`         | -------- |
|    `ANY_STRING`     | `System.Iec61131Lib.Any`         | -------- |

## Solution

You can also use the provided automatic Code Fix to change the `[DataType]` attribute argument to all possible mappings to choose from. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Change parameter type or IEC type in the `[DataType]` attribute to fit to each other.
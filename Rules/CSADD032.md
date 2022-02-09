# CSADD032 - Array element type needs correct DataType attribute

**Severity:** ![Error](../images/Error.png) Error

Checks user `[Array]`s (`[struct]`s with the attribute `[Array]`).
The `[DataType]` attribute of the `Anchor` has to fit to the Anchor type.

The correct mapping is shown inside the Readme.txt of each VS Template and looks like this:



| IEC 61131-3      | .NET Framework                    | C#       |
| ---------------- | --------------------------------- | -------- |
| `BOOL`           | `System.Boolean`                  | `bool`   |
| `SINT`           | `System.SByte`                    | `sbyte`  |
| `INT`            | `System.Int16`                    | `short`  |
| `DINT`           | `System.Int32`                    | `int`    |
| `LINT`           | `System.Int64`                    | `long`   |
| `USINT`          | `System.Byte`                     | `byte`   |
| `UINT`           | `System.UInt16`                   | `ushort` |
| `UDINT`          | `System.UInt32`                   | `uint`   |
| `ULINT`          | `System.UInt64`                   | `ulong`  |
| `REAL`           | `System.Single`                   | `float`  |
| `LREAL`          | `System.Double`                   | `double` |
| `TIME`           | `System.Int32`                    | `int`    |
| `LTIME`          | `System.Int64`                    | `long`   |
| `LDATE`          | `System.Int64`                    | `long`   |
| `LTIME_OF_DAY`   | `System.Int64`                    | `long`   |
| `LDATE_AND_TIME` | `System.Int64`                    | `long`   |
| `BYTE`           | `System.Byte`                     | `byte`   |
| `WORD`           | `System.UInt16`                   | `ushort` |
| `DWORD`          | `System.UInt32`                   | `uint`   |
| `LWORD`          | `System.UInt64`                   | `ulong`  |
| `STRING`         | `System.Iec61131Lib.IecStringEx`  | -------- |
| `STRING`         | `System.Iec61131Lib.IecString80`  | -------- |
| `WSTRING`        | `System.Iec61131Lib.IecWString`   | -------- |
| `WSTRING`        | `System.Iec61131Lib.IecWString80` | -------- |
| `ANY`            | `System.Iec61131Lib.Any`          | -------- |
| `ANY_MAGNITUDE`  | `System.Iec61131Lib.Any`          | -------- |
| `ANY_NUM`        | `System.Iec61131Lib.Any`          | -------- |
| `ANY_INT`        | `System.Iec61131Lib.Any`          | -------- |
| `ANY_SIGNED`     | `System.Iec61131Lib.Any`          | -------- |
| `ANY_UNSIGNED`   | `System.Iec61131Lib.Any`          | -------- |
| `ANY_REAL`       | `System.Iec61131Lib.Any`          | -------- |
| `ANY_BIT`        | `System.Iec61131Lib.Any`          | -------- |
| `ANY_ELEMENTARY` | `System.Iec61131Lib.Any`          | -------- |
| `ANY_STRING`     | `System.Iec61131Lib.Any`          | -------- |

## Solution

You can also use the provided automatic Code Fix to change the `[DataType]` attribute argument to all possible mappings to choose from. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Change the `Anchor`'s type or IEC type in the `[DataType]` attribute to fit to each other.
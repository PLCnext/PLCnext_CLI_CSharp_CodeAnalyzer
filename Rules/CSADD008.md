# CSADD008 - Return type is ambiguous in IEC and should be explicitly defined with a DataType attribute

**Severity:** ![Suggestion](../images/Suggestion.png) Suggestion

When the return type of IEC methods/functions can be mapped to multiple IEC types, a default type is used.
Consider using the `[DataType]` attribute to explicitly choose a mapped type.

IEC methods/functions that can have return values are methods that either:
* have the attribute `[User]`
* have the attribute `[Execution]`, are called `__Process` and are in a class with the attribute `[Function]`
* have the attribute `[Function]` and are in a class with the attribute `[FunctionContainer]`

Ambiguous types and their IEC types are shown in the following table (all mappings are shown inside the Readme.txt of each VS Template). If no `[DataType]` attribute is specified the type is mapped by default to the IEC data type in **bold** letters:

| C#       | .NET Framework           | IEC 61131-3 types                                            |
| -------- | ------------------------ | ------------------------------------------------------------ |
| `byte`   | `System.Byte`            | **`USINT`**, `BYTE`                                          |
| `int`    | `System.Int32`           | **`DINT`**, `TIME`                                           |
| `long`   | `System.Int64`           | **`LINT`**, `LTIME`, `LDATE`, `LTIME_OF_DAY`, `LDATE_AND_TIME` |
| `ushort` | `System.UInt16`          | **`UINT`**, `WORD`                                           |
| `uint`   | `System.UInt32`          | **`UDINT`**, `DWORD`                                         |
| `ulong`  | `System.UInt64`          | **`ULINT`**, `LWORD`                                         |
| ---      | `System.Iec61131Lib.Any` | `ANY`, `ANY_MAGNITUDE`, `ANY_NUM`, `ANY_INT`, `ANY_SIGNED`, `ANY_UNSIGNED`, `ANY_REAL`, `ANY_BIT`, `ANY_ELEMENTARY`, `ANY_STRING` |
## Solution

You can also use the provided automatic Code Fixes to add a `[DataType]` attribute with one of the possible mappings inside. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu)

Insert a `[DataType]` attribute with the name of the IEC type you want to map to.
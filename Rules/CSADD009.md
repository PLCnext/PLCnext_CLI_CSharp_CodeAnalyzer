# CSADD009 - Parameter type is ambiguous in IEC and should be explicitly defined with a DataType attribute

**Severity:** ![Suggestion](../images/Suggestion.png) Suggestion

When the parameter type (attributed with `[Output]`, ` [Input]` or `[InOut]`) of IEC methods/functions (attributed with `[User]`, `[Initialization]` or `[Execution]`) can be mapped to multiple IEC types, a default type is used.
Consider using the `[DataType]`attribute to explicitly choose a mapped type.

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

You can also use the provided automatic Code Fix to add a `[DataType]` attribute with all possible mappings inside to choose from. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Insert a `[DataType]` attribute with the name of the IEC type you want to map to.
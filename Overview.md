# IecAnalyzer for Phoenix Contact C# Add-In

The IecAnalyzer is a roslyn based Code Analyzer with the goal to help the development with the Phoenix Contact C# Add-In.

For general information on the PLCnext C# developement have a look at our [samples on github](https://github.com/PLCnext/CSharpExamples).

## Installation

The IecAnalyzer is installed via the PLCnext Toolchain.
The PLCnext Toolchain also installs the Visual Studio Project Template "PLCnext C# Firmware Library".
If you create a new Project with this Template the IecAnalyzer is active in the new project by default.

## Disable the IecAnalyzer

You may disable the IecAnalyzer by changing UseIecAnalyzer to false in the .csproj file:

```
<PropertyGroup>
    <UseIecAnalyzer>false</UseIecAnalyzer>
</PropertyGroup>
```

## Change the severity of the rules the IecAnalyzer provides

You can adjust the severity of each rule  with a `.editorconfig`. Additional information about automatic or manual creation at [.Net Code-Analysis Configuration](https://docs.microsoft.com/en-gb/visualstudio/code-quality/use-roslyn-analyzers)

* An example that disables the rule [Iec001](Rules/Iec001.md) in all .cs files (on and beneath the level of the EditorConfig file) would be: 

```
[*.cs] # next block applies to all .cs files
# sets Iec001 severity to none (possible severities: default|none|silent|suggestion|warning|error)
dotnet_diagnostic.Iec001.severity = none
```

## Suppression

You can also suppress a rule only for a single code region [using the context menu to create a SuppressMessage attribute or pragma](https://docs.microsoft.com/en-us/visualstudio/code-quality/in-source-suppression-overview?view=vs-2019#suppress-violations-in-source-code).

## Overview of all rules

| Diagnostic ID                      | Summary                                                                                                      | Default Severity                                |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------------- |
| [Iec001](Rules/Iec001.md)      | Old Attributes are not allowed                                                                                   | ![Warning](images/Warning.png) Warning          |
| [Iec002](Rules/Iec002.md)      | Name of the pou type too long                                                                                    | ![Error](images/Error.png) Error                |
| [Iec003](Rules/Iec003.md)      | Method missing that FunctionBlock/Function/Program needs                                                         | ![Error](images/Error.png) Error                |
| [Iec004](Rules/Iec004.md)      | Parameters of user types or Any have to use ref                                                                  | ![Warning](images/Warning.png) Warning          |
| [Iec005](Rules/Iec005.md)      | Return Type has to be IEC compatible                                                                             | ![Error](images/Error.png) Error                |
| [Iec006](Rules/Iec006.md)      | Parameter type has to be IEC compaible                                                                           | ![Error](images/Error.png) Error                |
| [Iec007](Rules/Iec007.md)      | Field type has to be IEC compatible                                                                              | ![Error](images/Error.png) Error                |
| [Iec008](Rules/Iec008.md)      | Return type is ambiguous in IEC and should be explicitly defined with a DataType attribute                       | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec009](Rules/Iec009.md)      | Parameter type is ambiguous in IEC and should be explicitly defined with a DataType attribute                    | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec010](Rules/Iec010.md)      | Field type is ambiguous in IEC and should be explicitly defined with a DataType attribute                        | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec011](Rules/Iec011.md)      | Return type needs correct DataType attribute                                                                     | ![Error](images/Error.png) Error                |
| [Iec012](Rules/Iec012.md)      | Parameter type needs correct DataType attribute                                                                  | ![Error](images/Error.png) Error                |
| [Iec013](Rules/Iec013.md)      | Field type needs correct DataType attribute                                                                      | ![Error](images/Error.png) Error                |
| [Iec014](Rules/Iec014.md)      | Fields of type Any must not be Outputs                                                                           | ![Error](images/Error.png) Error                |
| [Iec015](Rules/Iec015.md)      | Do not use GdsRetain                                                                                             | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec018](Rules/Iec018.md)      | Structure fields should be InOut pointers                                                                        | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec019](Rules/Iec019.md)      | Functions and FunctionContainers are not allowed to have attributed fields                                       | ![Error](images/Error.png) Error                |
| [Iec020](Rules/Iec020.md)      | Methods attributed Execution or Initialization are not allowed to have parameters                                | ![Error](images/Error.png) Error                |
| [Iec021](Rules/Iec021.md)      | Methods can only have one Output parameter at the first position                                                 | ![Error](images/Error.png) Error                |
| [Iec022](Rules/Iec022.md)      | Return types must not be Any or IecString or user structure                                                      | ![Error](images/Error.png) Error                |
| [Iec023](Rules/Iec023.md)      | Program port types must not be of type Any                                                                       | ![Error](images/Error.png) Error                |
| [Iec024](Rules/Iec024.md)      | Silently reports any struct declaration to provide templates for User Array, Structure and String                | Silent                                          |
| [Iec025](Rules/Iec025.md)      | IEC Array pattern has to be correct                                                                              | ![Error](images/Error.png) Error                |
| [Iec026](Rules/Iec026.md)      | IEC String Pattern has to be correct                                                                             | ![Error](images/Error.png) Error                |
| [Iec027](Rules/Iec027.md)      | IEC Structure and all its fields have to be public                                                               | ![Error](images/Error.png) Error                |
| [Iec028](Rules/Iec028.md)      | String length and size have to be correct                                                                        | ![Error](images/Error.png) Error                |
| [Iec029](Rules/Iec029.md)      | Init/ctor has to be called in Initialization for FunctionBlock fields that provide Init/ctor                     | ![Error](images/Error.png) Error                |
| [Iec030](Rules/Iec030.md)      | IEC Structs have to provide an Init Method calling field's Init/ctor method when any fields have it              | ![Error](images/Error.png) Error                |
| [Iec031](Rules/Iec031.md)      | Array element type is ambiguous and should be explicitly defined with a DataType attribute                       | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec032](Rules/Iec032.md)      | Array element type needs correct DataType attribute                                                              | ![Error](images/Error.png) Error                |
| [Iec033](Rules/Iec033.md)      | Array element type has to be IEC compatible                                                                      | ![Error](images/Error.png) Error                |
| [Iec034](Rules/Iec034.md)      | Structure field type is ambiguous and should be explicitly defined with a DataType attribute                     | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec035](Rules/Iec035.md)      | Structure field type has to be Iec compatible                                                                    | ![Error](images/Error.png) Error                |
| [Iec036](Rules/Iec036.md)      | Structure field needs correct DataType attribute                                                                 | ![Error](images/Error.png) Error                |
| [Iec037](Rules/Iec037.md)      | Program must not have Input Output or InOut attributes                                                           | ![Error](images/Error.png) Error                |
| [Iec038](Rules/Iec038.md)      | Init Methods of user types must not have an Initialization attribute                                             | ![Warning](images/Warning.png) Warning          |
| [Iec039](Rules/Iec039.md)      | User type Init methods must not have parameters                                                                  | ![Error](images/Error.png) Error                |
| [Iec040](Rules/Iec040.md)      | Structure parameters should use ref                                                                              | ![Suggestion](images/Suggestion.png) Suggestion |
| [Iec041](Rules/Iec041.md)      | Init/ctor must only be called once in Init or __Init                                                             | ![Error](images/Error.png) Error                |
| [Iec042](Rules/Iec042.md)      | unsafe blocks are only allowed when pointers are used inside                                                     | ![Warning](images/Warning.png) Warning          |
| [Iec043](Rules/Iec043.md)      | Output parameter name unequal to class name                                                                      | ![Error](images/Error.png) Error                |
| [Iec044](Rules/Iec044.md)      | Output parameter name unequal to method name                                                                     | ![Error](images/Error.png) Error                |
| [Iec045](Rules/Iec045.md)      | Output parameter must be ref or out                                                                              | ![Error](images/Error.png) Error                |
| [Iec046](Rules/Iec046.md)      | Function Container Functions have to be static                                                                   | ![Error](images/Error.png) Error                |
| [Iec047](Rules/Iec047.md)      | Arrays must not have fields apart from the Anchor field                                                          | ![Error](images/Error.png) Error                |
| [Iec048](Rules/Iec048.md)      | Only use Initialization and Execution where correct                                                              | ![Error](images/Error.png) Error                |
| [Iec049](Rules/Iec049.md)      | User attribute should only be used in Function Blocks	                                                        | ![Error](images/Error.png) Error                |
| [Iec050](Rules/Iec050.md)      | Input or Output fields and parameters shall not be pointers                                                      | ![Error](images/Error.png) Error                |
| [Iec051](Rules/Iec051.md)      | Structures must not have Any or Pointer fields	                                                                | ![Error](images/Error.png) Error                |
| [Iec052](Rules/Iec052.md)      | Retaining on Input can be better achieved with Variable Flag	                                                    | ![Warning](images/Warning.png) Warning          |
| [Iec053](Rules/Iec053.md)      | Retaining should only be used in FB or Program	                                                                | ![Error](images/Error.png) Error                |
| [Iec054](Rules/Iec054.md)      | Only use Function attribute in Function Container or on classes                                                  | ![Error](images/Error.png) Error                |
| [Iec055](Rules/Iec055.md)      | Strings must not have fields apart from the s field                                                              | ![Error](images/Error.png) Error                |
| [Iec056](Rules/Iec056.md)      | Do not use intern attributes	                                                                                    | ![Error](images/Error.png) Error                |
| [Iec057](Rules/Iec057.md)      | Namespace names must not be keywords                                                                             | ![Error](images/Error.png) Error                |
| [Iec058](Rules/Iec058.md)      | Do not mix Retain and GdsRetain		                                                                            | ![Error](images/Error.png) Error                |
| [Iec059](Rules/Iec059.md)      | Only use Retaining where possible                                                                                | ![Error](images/Error.png) Error                |
| [Iec060](Rules/Iec060.md)      | Only use Hidden on user defined data types and POUs	                                                            | ![Error](images/Error.png) Error                |
| [Iec061](Rules/Iec061.md)      | Only use NotOverridable on POUs	                                                                                | ![Error](images/Error.png) Error                |
| [Iec062](Rules/Iec062.md)      | Only use OPC, Ehmi, ProfiCloud and Redundant where possible                                                      | ![Error](images/Error.png) Error                |
| [Iec064](Rules/Iec064.md)      | Exported fields have to be public                                                                                | ![Error](images/Error.png) Error                |
| [Iec065](Rules/Iec065.md)      | Do not use the suffix attribute when using attributes                                                            | ![Error](images/Error.png) Error                |
| [Iec066](Rules/Iec066.md)      | Methods returning values must not have Output parameters                                                         | ![Error](images/Error.png) Error                |
| [Iec067](Rules/Iec067.md)      | Do not use partial                                                                                               | ![Warning](images/Warning.png) Warning          |
| [Iec068](Rules/Iec068.md)      | Initialize all Array elements                                                                                    | ![Error](images/Error.png) Error                |
| [Iec069](Rules/Iec069.md)      | Only Initialize in Init method                                                                                   | ![Error](images/Error.png) Error                |
| [Iec070](Rules/Iec070.md)      | Only use Invisible where possible                                                                                | ![Error](images/Error.png) Error                |
| [Iec071](Rules/Iec071.md)      | Elements need unique names                                                                                       | ![Error](images/Error.png) Error                |
| [Iec072](Rules/Iec072.md)      | Use Init instead of old ctor                                                                                     | ![Warning](images/Warning.png) Warning          |
| [Iec073](Rules/Iec073.md)      | rctor is deprecated                                                                                              | ![Warning](images/Warning.png) Warning          |
| [Iec074](Rules/Iec074.md)      | Multidimensional Arrays are not supported yet                                                                    | ![Error](images/Error.png) Error                |
| [Iec075](Rules/Iec075.md)      | Only use Eno where possible                                                                                      | ![Error](images/Error.png) Error                |
| [Iec076](Rules/Iec076.md)      | Do not use POU attributes on abstract classes                                                                    | ![Error](images/Error.png) Error                |
| [Iec077](Rules/Iec077.md)      | Exported Identifiers must not be keywords                                                                        | ![Error](images/Error.png) Error                |
| [Iec078](Rules/Iec078.md)      | Parameters of type Any must not be InOuts                                                                        | ![Error](images/Error.png) Error                |
| [Iec079](Rules/Iec079.md)      | Only use Port attributes in Program	                                                                            | ![Error](images/Error.png) Error                |
| [Iec080](Rules/Iec080.md)      | DataType Attribute can only be used on classes if they are Functions	                                            | ![Error](images/Error.png) Error                |
| [Iec081](Rules/Iec081.md)      | DataType Attribute can only be used on methods if they are User methods or Function methods in FunctionContainer	| ![Error](images/Error.png) Error                |
| [Iec082](Rules/Iec082.md)      | DataType Attribute for Output parameters positioned on class or method instead                                   | ![Error](images/Error.png) Error                |
| [Iec084](Rules/Iec084.md)      | Generic methods are not supported                                                                                | ![Error](images/Error.png) Error                |
| [Iec085](Rules/Iec085.md)      | Max 8 type parameters are supported                                                                              | ![Error](images/Error.png) Error                |
| [Iec086](Rules/Iec086.md)      | Do not nest type arguments                                                                                       | ![Error](images/Error.png) Error                |
| [Iec087](Rules/Iec087.md)      | Generic delegates can not be parameters                                                                          | ![Error](images/Error.png) Error                |
| [Iec088](Rules/Iec088.md)      | Fields must not use class type parameters                                                                        | ![Error](images/Error.png) Error                |
| [Iec089](Rules/Iec089.md)      | Also implement non-generic IComparer when implementing generic IComparer                                         | ![Error](images/Error.png) Error                |

## Rule  groups

### Typing

* compatability of C# dotnet types to IEC
  * [Iec005](Rules/Iec005.md), [Iec006](Rules/Iec006.md) [Iec007](Rules/Iec007.md) [Iec035](Rules/Iec035.md) [Iec033](Rules/Iec033.md)
* ambiguous C# dotnet types that can be converted to multiple IEC types. Therefore a DataType attribute for clarification might be necessary.
  * [Iec008](Rules/Iec008.md) [Iec009](Rules/Iec009.md) [Iec0010](Rules/Iec0010.md)  [Iec034 ](Rules/Iec034.md)[Iec031](Rules/Iec031.md)
* IEC type defined in DataType attributes have to suit the C# dotnet type
  * [Iec011](Rules/Iec011.md) [Iec012](Rules/Iec012.md) [Iec0013 ](Rules/Iec0013.md)[Iec036](Rules/Iec036.md) [Iec032](Rules/Iec032.md)
* special rules for the type Any (and User Types and IecStrings)
  * [Iec014](Rules/Iec014.md) [Iec018](Rules/Iec018.md) [Iec022](Rules/Iec022.md) [Iec023](Rules/Iec023.md) [Iec040](Rules/Iec040.md) [Iec078](Rules/Iec078.md) 

### IEC element structure

[Iec002](Rules/Iec002.md) [Iec020](Rules/Iec020.md) [Iec021](Rules/Iec021.md)

* `[FunctionBlock]`
  * [Iec003](Rules/Iec003.md) [Iec071](Rules/Iec071.md) [Iec076](Rules/Iec076.md)
* `[Function]`
  * [Iec003](Rules/Iec003.md) [Iec019](Rules/Iec019.md) [Iec076](Rules/Iec076.md)
 * `[FunctionContainer]`
  * [Iec046](Rules/Iec046.md) [Iec076](Rules/Iec076.md)
* `[Program]`
  * [Iec003](Rules/Iec003.md) [Iec037](Rules/Iec037.md) [Iec076](Rules/Iec076.md)
* User Types
  * [Iec024](Rules/Iec024.md) [Iec038](Rules/Iec038.md) [Iec039](Rules/Iec039.md)
  * `[String]`
    * [Iec026](Rules/Iec026.md) [Iec028](Rules/Iec028.md) [Iec055](Rules/Iec055.md)
  * `[Structure]`
    * [Iec027](Rules/Iec027.md) [Iec051](Rules/Iec051.md) [Iec069](Rules/Iec069.md)
  * `[Array]`
    * [Iec025](Rules/Iec025.md) [Iec047](Rules/Iec047.md) [Iec068](Rules/Iec068.md) [Iec074](Rules/Iec074.md)

### IEC type Initialization

* [Iec041](Rules/Iec041.md)
* [Iec072](Rules/Iec072.md)
* [Iec073](Rules/Iec073.md)
* `[Structure]`
  * [Iec030](Rules/Iec030.md)
* `[Array]`
  * [Iec068](Rules/Iec068.md)
* `[FunctionBlock]`
  * [Iec029](Rules/Iec029.md)

### Pointers and References

* [Iec004](Rules/Iec004.md) [Iec018](Rules/Iec018.md) [Iec042](Rules/Iec042.md) [Iec050](Rules/Iec050.md)

### Generics

* [Iec084](Rules/Iec084.md)
* [Iec085](Rules/Iec085.md)
* [Iec086](Rules/Iec086.md)
* [Iec086](Rules/Iec086.md)
* [Iec087](Rules/Iec087.md)
* [Iec088](Rules/Iec088.md)
* [Iec089](Rules/Iec089.md)

### Attribute Usage

* Deprecated Attributes
  * [Iec001](Rules/Iec001.md)
* Attribute suffix
  * [Iec065](Rules/Iec065.md)
* `[Input]`, `[Output]`, `[InOut]`, `[Local]`, `[InputPort]` and `[OutputPort]`
  *  [Iec064](Rules/Iec064.md)
* `[User]`
  * [Iec049](Rules/Iec049.md)
* `[GdsRetain]` and `[Retain]`
  * [Iec053](Rules/Iec053.md) [Iec052](Rules/Iec052.md) 
* `[Function]`
  * [Iec054](Rules/Iec054.md) 
* `[Output]`
  * [Iec043](Rules/Iec043.md) [Iec044](Rules/Iec044.md) [Iec045](Rules/Iec045.md) [Iec066](Rules/Iec066.md)
* `[Initialization]` and `[Execution]`
  * [Iec048](Rules/Iec048.md)
* `[Skip]` and `[ReadOnly]`
  * [Iec056](Rules/Iec056.md)
* `[Retain]` and `[GdsRetain]`
  * [Iec058](Rules/Iec058.md) [Iec059](Rules/Iec059.md) [Iec015](Rules/Iec015.md)
* `[Hidden]`
  * [Iec060](Rules/Iec060.md)
* `[NotOverridable]`
  * [Iec061](Rules/Iec061.md)
* `[OPC]`, `[Ehmi]`, `[ProfiCloud]` and `[Redundant]`
  * [Iec062](Rules/Iec062.md)
* `[Invisible]`
  * [Iec070](Rules/Iec070.md)
* `[Eno]`
  * [Iec075](Rules/Iec075.md)
* `[DataType]` positioning
  * [Iec080](Rules/Iec080.md) [Iec081](Rules/Iec081.md) [Iec082](Rules/Iec082.md) [Iec083](Rules/Iec083.md)

# Add-In-Analyzer for Phoenix Contact C# Add-In

The Add-In-Analyzer is a roslyn based Code Analyzer with the goal to help the development with the Phoenix Contact C# Add-In.

For general information on the PLCnext C# developement have a look at our [samples on github](https://github.com/PLCnext/CSharpExamples).

## Installation/Deployment

The Add-In-Analyzer can be used as a NuGet-package. 

For additional information on how to use NuGet Packages have a look at the [Visual Studio - NuGet Guide](https://docs.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)

## Optional Configuration

You can adjust the severity of each rule  with a `.editorconfig`. Additional information about automatic or manual creation at [.Net Code-Analysis Configuration](https://docs.microsoft.com/en-gb/visualstudio/code-quality/use-roslyn-analyzers)

* An example that disables the rule [CSADD001](Rules/CSADD001.md) in all .cs files (on and beneath the level of the EditorConfig file) would be: 

```
editorconfig
[*.cs] # next block applies to all .cs files
# sets CSADD001 severity to none (possible severities: default|none|silent|suggestion|warning|error)
dotnet_diagnostic.CSADD001.severity = none
```

## Suppression

You can also suppress a rule only for a single code region [using the context menu to create a SuppressMessage attribute or pragma](https://docs.microsoft.com/en-us/visualstudio/code-quality/in-source-suppression-overview?view=vs-2019#suppress-violations-in-source-code).

## Overview of all rules

| Diagnostic ID                      | Summary                                                                                              | Default Severity                                |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| [CSADD001](Rules/CSADD001.md)      | Old Attributes are not allowed                                                                       | ![Warning](images/Warning.png) Warning          |
| [CSADD002](Rules/CSADD002.md)      | Name of the pou type too long                                                                        | ![Error](images/Error.png) Error                |
| [CSADD003](Rules/CSADD003.md)      | Method missing that FunctionBlock/Function/Program needs                                             | ![Error](images/Error.png) Error                |
| [CSADD004](Rules/CSADD004.md)      | Parameters of user types or Any have to use ref                                                      | ![Warning](images/Warning.png) Warning          |
| [CSADD005](Rules/CSADD005.md)      | Return Type has to be IEC compatible                                                                 | ![Error](images/Error.png) Error                |
| [CSADD006](Rules/CSADD006.md)      | Parameter type has to be IEC compaible                                                               | ![Error](images/Error.png) Error                |
| [CSADD007](Rules/CSADD007.md)      | Field type has to be IEC compatible                                                                  | ![Error](images/Error.png) Error                |
| [CSADD008](Rules/CSADD008.md)      | Return type is ambiguous in IEC and should be explicitly defined with a DataType attribute           | ![Suggestion](images/Suggestion.png) Suggestion |
| [CSADD009](Rules/CSADD009.md)      | Parameter type is ambiguous in IEC and should be explicitly defined with a DataType attribute        | ![Suggestion](images/Suggestion.png) Suggestion |
| [CSADD010](Rules/CSADD010.md)      | Field type is ambiguous in IEC and should be explicitly defined with a DataType attribute            | ![Suggestion](images/Suggestion.png) Suggestion |
| [CSADD011](Rules/CSADD011.md)      | Return type needs correct DataType attribute                                                         | ![Error](images/Error.png) Error                |
| [CSADD012](Rules/CSADD012.md)      | Parameter type needs correct DataType attribute                                                      | ![Error](images/Error.png) Error                |
| [CSADD013](Rules/CSADD013.md)      | Field type needs correct DataType attribute                                                          | ![Error](images/Error.png) Error                |
| [CSADD014](Rules/CSADD014.md)      | Output fields/parameters must not be Any                                                             | ![Error](images/Error.png) Error                |
| [CSADD017](Rules/CSADD017.md)      | Structure fields should be InOut                                                                     | ![Suggestion](images/Suggestion.png) Suggestion |
| [CSADD018](Rules/CSADD018.md)      | Structure fields should be pointers                                                                  | ![Warning](images/Warning.png) Warning          |
| [CSADD019](Rules/CSADD019.md)      | Functions are not allowed to have attributed fields                                                  | ![Error](images/Error.png) Error                |
| [CSADD020](Rules/CSADD020.md)      | Methods attributed Execution or Initialization are not allowed to have parameters                    | ![Error](images/Error.png) Error                |
| [CSADD021](Rules/CSADD021.md)      | Methods can only have one Output parameter at the first position                                     | ![Error](images/Error.png) Error                |
| [CSADD022](Rules/CSADD022.md)      | Return types must not be of an Any type or a structure                                               | ![Error](images/Error.png) Error                |
| [CSADD023](Rules/CSADD023.md)      | Program port types must not be of type Any                                                           | ![Error](images/Error.png) Error                |
| [CSADD024](Rules/CSADD024.md)      | Silently reports any struct declaration to provide templates for User Array, Structure and String    | Silent                                          |
| [CSADD025](Rules/CSADD025.md)      | IEC Array pattern has to be correct                                                                  | ![Error](images/Error.png) Error                |
| [CSADD026](Rules/CSADD026.md)      | IEC String Pattern has to be correct                                                                 | ![Error](images/Error.png) Error                |
| [CSADD027](Rules/CSADD027.md)      | IEC Structure and all its fields have to be public                                                   | ![Error](images/Error.png) Error                |
| [CSADD028](Rules/CSADD028.md)      | String length and size have to be correct                                                            | ![Error](images/Error.png) Error                |
| [CSADD029](Rules/CSADD029.md)      | Init/ctor has to be called in Initialization for FunctionBlock fields that provide Init/ctor         | ![Error](images/Error.png) Error                |
| [CSADD030](Rules/CSADD030.md)      | IEC Structs have to provide an Init Method calling field's Init/ctor method when any fields have it  | ![Error](images/Error.png) Error                |
| [CSADD031](Rules/CSADD031.md)      | Array element type is ambiguous and should be explicitly defined with a DataType attribute           | ![Suggestion](images/Suggestion.png) Suggestion |
| [CSADD032](Rules/CSADD032.md)      | Array element type needs correct DataType attribute                                                  | ![Error](images/Error.png) Error                |
| [CSADD033](Rules/CSADD033.md)      | Array element type has to be IEC compatible                                                          | ![Error](images/Error.png) Error                |
| [CSADD034](Rules/CSADD034.md)      | Structure field type is ambiguous and should be explicitly defined with a DataType attribute         | ![Suggestion](images/Suggestion.png) Suggestion |
| [CSADD035](Rules/CSADD035.md)      | Structure field type has to be Iec compatible                                                        | ![Error](images/Error.png) Error                |
| [CSADD036](Rules/CSADD036.md)      | Structure field needs correct DataType attribute                                                     | ![Error](images/Error.png) Error                |
| [CSADD037](Rules/CSADD037.md)      | Program must not have Input Output or InOut attributes                                               | ![Error](images/Error.png) Error                |
| [CSADD038](Rules/CSADD038.md)      | Init Methods of user types must not have an Initialization attribute                                 | ![Warning](images/Warning.png) Warning          |
| [CSADD039](Rules/CSADD039.md)      | User type Init methods must not have parameters                                                      | ![Error](images/Error.png) Error                |
| [CSADD040](Rules/CSADD040.md)      | Structure parameters should be ref Output                                                            | ![Suggestion](images/Suggestion.png) Suggestion |
| [CSADD041](Rules/CSADD041.md)      | Init/ctor must only be called once in Init or __Init                                                 | ![Error](images/Error.png) Error                |
| [CSADD042](Rules/CSADD042.md)      | unsafe blocks are only allowed when pointers are used inside                                         | ![Warning](images/Warning.png) Warning          |
| [CSADD043](Rules/CSADD043.md)      | Output parameter name unequal to class name                                                          | ![Error](images/Error.png) Error                |
| [CSADD044](Rules/CSADD044.md)      | Output parameter name unequal to method name                                                         | ![Error](images/Error.png) Error                |
| [CSADD045](Rules/CSADD045.md)      | Output parameter must be ref or out                                                                  | ![Error](images/Error.png) Error                |
| [CSADD046](Rules/CSADD046.md)      | Function Container Functions have to be static                                                       | ![Error](images/Error.png) Error                |
| [CSADD047](Rules/CSADD047.md)      | Arrays must not have fields apart from the Anchor field                                              | ![Error](images/Error.png) Error                |
| [CSADD048](Rules/CSADD048.md)      | Only use Initialization and Execution where correct                                                  | ![Error](images/Error.png) Error                |
| [CSADD049](Rules/CSADD049.md)      | User attribute should only be used in Function Blocks	                                            | ![Error](images/Error.png) Error                |
| [CSADD050](Rules/CSADD050.md)      | Input or Output fields and parameters shall not be pointers                                          | ![Error](images/Error.png) Error                |
| [CSADD051](Rules/CSADD051.md)      | Structures must not have Any or Pointer fields	                                                    | ![Error](images/Error.png) Error                |
| [CSADD052](Rules/CSADD052.md)      | Retaining on Input can be better achieved with Variable Flag	                                        | ![Warning](images/Warning.png) Warning          |
| [CSADD053](Rules/CSADD053.md)      | Retaining should only be used in FB or Program	                                                    | ![Error](images/Error.png) Error                |
| [CSADD054](Rules/CSADD054.md)      | Only use Function attribute in Function Container or on classes                                      | ![Error](images/Error.png) Error                |
| [CSADD055](Rules/CSADD055.md)      | Strings must not have fields apart from the s field                                                  | ![Error](images/Error.png) Error                |
| [CSADD056](Rules/CSADD056.md)      | Do not use intern attributes	                                                                        | ![Error](images/Error.png) Error                |
| [CSADD058](Rules/CSADD058.md)      | Do not mix Retain and GdsRetain		                                                                | ![Error](images/Error.png) Error                |
| [CSADD059](Rules/CSADD059.md)      | Only use Retaining where possible                                                                    | ![Error](images/Error.png) Error                |
| [CSADD060](Rules/CSADD060.md)      | Only use Hidden on user defined data types and POUs	                                                | ![Error](images/Error.png) Error                |
| [CSADD061](Rules/CSADD061.md)      | Only use NotOverridable on POUs	                                                                    | ![Error](images/Error.png) Error                |
| [CSADD062](Rules/CSADD062.md)      | Only use OPC, Ehmi, ProfiCloud and Redundant where possible                                          | ![Error](images/Error.png) Error                |

## Rule  groups

### Typing

* compatability of C# dotnet types to IEC
  * [CSADD005](Rules/CSADD005.md), [CSADD006](Rules/CSADD006.md) [CSADD007](Rules/CSADD007.md) [CSADD035](Rules/CSADD035.md) [CSADD033](Rules/CSADD033.md)
* ambiguous C# dotnet types that can be converted to multiple IEC types. Therefore a DataType attribute for clarification might be necessary.
  * [CSADD008](Rules/CSADD008.md) [CSADD009](Rules/CSADD009.md) [CSADD0010](Rules/CSADD0010.md)  [CSADD034 ](Rules/CSADD034.md)[CSADD031](Rules/CSADD031.md)
* IEC type defined in DataType attributes have to suit the C# dotnet type
  * [CSADD011](Rules/CSADD011.md) [CSADD012](Rules/CSADD012.md) [CSADD0013 ](Rules/CSADD0013.md)[CSADD036](Rules/CSADD036.md) [CSADD032](Rules/CSADD032.md)
* special rules for the type Any (and User Types)
  * [CSADD014](Rules/CSADD014.md) [CSADD017](Rules/CSADD017.md) [CSADD018](Rules/CSADD018.md) [CSADD022](Rules/CSADD022.md) [CSADD023](Rules/CSADD023.md) [CSADD040](Rules/CSADD040.md) 

### IEC element structure

[CSADD002](Rules/CSADD002.md) [CSADD020](Rules/CSADD020.md) [CSADD021](Rules/CSADD021.md)

* `[FunctionBlock]`
  * [CSADD003](Rules/CSADD003.md)
* `[Function]`
  * [CSADD003](Rules/CSADD003.md) [CSADD019](Rules/CSADD019.md)
 * `[FunctionContainer]`
  * [CSADD046](Rules/CSADD046.md)
* `[Program]`
  * [CSADD003](Rules/CSADD003.md) [CSADD037](Rules/CSADD037.md)
* User Types
  * [CSADD024](Rules/CSADD024.md) [CSADD038](Rules/CSADD038.md) [CSADD039](Rules/CSADD039.md)
  * `[String]`
    * [CSADD026](Rules/CSADD026.md) [CSADD028](Rules/CSADD028.md) [CSADD055](Rules/CSADD055.md)
  * `[Structure]`
    * [CSADD027](Rules/CSADD027.md) [CSADD051](Rules/CSADD051.md)
  * `[Array]`
    * [CSADD025](Rules/CSADD025.md) [CSADD047](Rules/CSADD047.md)

### IEC type Initialization

* [CSADD041](Rules/CSADD041.md)
* User Types
  * [CSADD030](Rules/CSADD030.md)
* `[FunctionBlock]`
  * [CSADD029](Rules/CSADD029.md)

### Pointers and References

* [CSADD004](Rules/CSADD004.md) [CSADD018](Rules/CSADD018.md) [CSADD042](Rules/CSADD042.md) [CSADD050](Rules/CSADD050.md)

### Attribute Usage

* Deprecated Attributes
  * [CSADD001](Rules/CSADD001.md)
* `[User]`
  * [CSADD049](Rules/CSADD049.md)
* `[GdsRetain]` and `[Retain]`
  * [CSADD053](Rules/CSADD053.md) [CSADD052](Rules/CSADD052.md) 
* `[Function]`
  * [CSADD054](Rules/CSADD054.md)
* `[Output]`
  * [CSADD043](Rules/CSADD043.md) [CSADD044](Rules/CSADD044.md) [CSADD045](Rules/CSADD045.md)
* `[Initialization]` and `[Execution]`
  * [CSADD048](Rules/CSADD048.md)
* `[Skip]` and `[ReadOnly]`
  * [CSADD056](Rules/CSADD056.md)
* `[Retain]` and `[GdsRetain]`
  * [CSADD058](Rules/CSADD058.md) [CSADD059](Rules/CSADD059.md)
* `[Hidden]`
  * [CSADD060](Rules/CSADD060.md)
* `[NotOverridable]`
  * [CSADD061](Rules/CSADD061.md)
* `[OPC]`, `[Ehmi]`, `[ProfiCloud]` and `[Redundant]`
  * [CSADD062](Rules/CSADD062.md)
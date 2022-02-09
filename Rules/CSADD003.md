# CSADD003 - Method missing that FunctionBlock/Function/Program needs

**Severity:** ![Error](../images/Error.png) Error

`Function`s  need the following method and attribute:

```c#
[Execution]
public static __Process()
{
}
```

`[FunctionBlock]`s and `[Program]`s need the following methods and attributes:

```c#
[Initialization]
public __Init()
{
}
```

```c#
[Execution]
public __Process()
{
}
```


## Solution

You can also use the provided automatic Code Fix to create the missing methods. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 


Insert the missing methods with their attributes to resolve the error.
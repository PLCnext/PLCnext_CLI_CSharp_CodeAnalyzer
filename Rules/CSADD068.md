# CSADD068 - Initialize all Array elements

**Severity:** ![Error](images/Error.png) Error

Reports the `Init` method / or declaration of a struct attributed with `[Array]` when the type of the `Anchor` has an `Init`, `__Init` or `ctor` method and an initialization similar to the following pattern is not inside the `Init` method:

````
fixed (#Anchor type#* ptr = &this.Anchor)
{
    for (int i = 0; i < UB - LB + 1; i++)
    {
        ptr[i].#call to Init, __Init or ctor depending on existence for the Anchor type#();
    }
}
```

The #Anchor type# has to be the same as the type of the `Anchor` of the Array.
The #call to Init, __Init or ctor depending on existence for the Anchor type# is the name of the initialization method the `Anchor` has.

## Solution

You can also use the provided automatic Code Fix to add the correct pattern. ( Press Alt + Enter on the Error line to find the Code Fix in the context menu) 

Add the correct initialization pattern.
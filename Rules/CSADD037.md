# CSADD037 - Program must not have Input, Output or InOut attributes

**Severity:** ![Error](../images/Error.png) Error

Classes with the attribute `[Program]` must not have `[Output]`, ` [Input]` or `[InOut]` attributes.
The provided attributes for programs are `[InputPort]` or `[OutputPort]`.

## Solution

Use `[InputPort]` or `[OutputPort]` attributes to implement the program.
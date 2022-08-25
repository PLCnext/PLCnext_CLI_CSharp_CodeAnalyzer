# CSADD071 - Method parameters and fields of FunctionBlocks need different names

**Severity:** ![Error](images/Error.png) Error

Checks parameters that are inside a `class` attributed with `[FunctionBlock]`, when a field with a `[Input]`, `[InOut]` or `[Output]` attribute has the same name, the parameter name and field name are reported.

## Solution

Rename the parameter or the field.
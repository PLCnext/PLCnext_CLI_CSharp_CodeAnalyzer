# CSADD052 - Retaining on Input can be better achieved with Variable Flag

**Severity:** ![Warning](images/Warning.png) Warning

Checks the use of the `[GdsRetain]` and the `[Retain]` attribute, when it is used in Combination with the `[Input]` attribute the diagnostic is reported.

## Solution

Remove the attribute and instead set the linked variable's Retain flag in the PLCnext Engineer.
# CSADD067 - Do not use the partial

**Severity:** ![Warning](images/Warning.png) Warning

Reports all `partial` keywords because the analyzer might not find all problems in partial classes.

## Solution

Remove the `partial` modifier and merge the classes.
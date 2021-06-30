+++
+++

Functions in PRSE are defined as follows:
```cpp
function <name>(<comma separated list of parameters>): <return type> {}
```

The name of your function may be any identifier that has not been previously used. `main`
is reserved for the main function of the program. Any libraries you include that define
their own functions reserve the names of said functions.

You may use `func` in place of `function` if you choose; either is syntactically valid.



# Return types

Functions can return all of the [primitive types](/introduction/first_program#prse-primitive-types),
plus `void`. Functions are of type `void` by default if you omit the `: <return type>`
from the function header.

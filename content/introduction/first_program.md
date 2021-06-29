+++
title = "Writing your first PRSE program"
+++

{{< toc >}}

# Creating the program file

Using a text editor, create a file with whatever title you please (or, if you want
an example, use `main`). Ensure the program's filetype is `.prse`.

# Variables

Code example:
```cpp
let <var>: <type> = 20;
```
Assigning a variable to a value is as simple as typing the syntax above.
`<var>` can be any [valid C-style variable string](https://en.wikibooks.org/wiki/C_Programming/Variables#Naming_Variables);
`<type>` dictates the variable's type, which remains static until the variable goes out of scope.
See [primitive types](#prse-primitive-types) for what you can use in place of `<type>`.

# PRSE primitive types
| Type   | Desc. | Valid values |
|---|---|---|
| `bool`   | Boolean |`true`, `false`|
| `int`    | Integer | Any whole number |
| `float`  | Float | Any whole number, plus fractional numbers |
| `char`   | Character | Any single ASCII character (e.g. 'a', 'b', 'c', and so on) |
| `string` | String | Any valid ASCII character string |

# The `main` function

As with most programming languages, the `main` function is the primary entry
point into your program. All other instructions are run here. Nothing will be executed
if no main function is present.

```cpp
function main() {
    // Code here
}
```

You may use `func` in place of `function`, if you desire. Either is syntactically valid.

# Printing to the console

Somewhere at the beginning of your file, before you declare any variables, place
the following `use` statement:  
`use "io"`

This will allow you to use the `print()` function, among other things. Now for the inaugural
"hello world":
```cpp
function main() {
    println("Hello world");
}
```

Assuming you either have `prsec` added to your `PATH`, run:  
`prsec <your file name>.prse`

If you are running `prsec` from within the folder you compiled it, put `./` before `prsec`
on your command line.

At this point, the compiler should have produced no output to the console, but
you should now have a file `a.out` in the same directory as your program file. Run `./a.out`.
`Hello world` should have printed to the console window.
+++
+++

{{< expand "History" >}}
I first concieved of the PRSE language sometime circa 2018. I didn't have an idea of what
I actually wanted to make the language look like, just that I wanted to make a language.
It was not until 2019, having completed my compilers class in my Junior year of college,
that I knew how to make a programming language, and further had an idea of how I wanted
it to look. From that point, I sketched an idea of the language's grammar and syntax
and during the summer of 2020, further generated ideas in preparation for my senior
project, at which point the program went into full development.  

At the time of writing, there is no community around the language, which is to be
expected--I didn't promote the language at all, and if I did it's doubtful anyone would
want to pick it up. Even I realize that several features are missing. Still, I've written
this documentation in the hopes that anyone who wishes to pick up the language may
do so with clarity.
{{< /expand >}}

## Installation

The PRSE compiler itself is relatively straightforward to compile, granted that you
are running a *nix-based system such as Linux:

1. [Clone the git repository from GitHub](#TODO)
2. `cd prse/src`
    - Install prerequisite libraries[^1]:
    - Bison 3.7.1 or newer
    - Flex 2.6.4 or newer
    - Clang++ 10.0.0 or newer
    - **Ensure that these programs are up to date:  
`bison --version; flex --version; clang++ --version`**
3. `make`
4. Compiled binary is `prsec`. Use it to compile any PRSE code you write, or
compile any of the examples in `/prse/src/examples`.

## Usage

Run `prsec` like any other compiler:  
`prsec [OPTIONS] [FILE]`  

The program will let you know if any options you have set are not recognized, or
need additional parameters to be set.

[^1]: {{< expand "Why do I need these specific versions?" >}}
It's generally a good idea to have your tools up-to-date, as newer versions will
contain various bug fixes, and often new features which offer convieniences to developers
working with them. In particular, Bison 3.7.1+ contains a feature which generates
counter-examples if some grammar rule is not set up properly. You can easily edit
the Makefile and remove the `-Wcex` flag from `BISON_FLAGS`, but I cannot guarantee
compatibility if you don't use the versions I specified since I didn't test compilation
with those versions.
{{< /expand >}}
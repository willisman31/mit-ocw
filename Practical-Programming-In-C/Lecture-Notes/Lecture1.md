# Lecture 1

## What is C?

- Created by Dennis Ritchie at Bell labs in 1972 for the 16-bit DEC PDP-11 computer
- used today for some of the following reasons:
    - extending existing architecture
    - efficiency/high performance
    - low-level access

## Features of C

- few keywords
- pointers
- structs, unions
- external standard library
- compiles to native code
- macro preprocessor

## Versions of C

1972 - C invented
1978 - *C Programming Language* published
1989 - ANSI C (C89 standard)
1990 - ANSI C accepted by ISO (C90 standard)
1999 - C99 standard
2023 - C23 standard, latest C standard (expected publication in 2024)

## For what is C Used?

- systems programming
    - operating systems
    - embedded systems
    - processors
    - etc.

## C vs Related Languages

- derivatives include C++, C#, Java, Perl
- lacks the following:
    - exceptions
    - range-checking
    - garbage colleciton
    - OOP
    - polymorphism
- lower level ~~> faster code (generally)

## Warning: low-level language

- no range checking
- limited compile-time type safety
- no runtime type checking
- always run in a debugger (such as gdb)
- never run as admin/root
- avoid running untested on devices you care about

## Editing C Code

- *.c* extension on raw code
- directly editable

## Compiling a Program

- GCC compiler (GNU C Compiler)
    - included in most Linux distros
- *.o* extension on compiled programs
    - must be specified in GCC

## More about GCC

- run gcc:
    ```gcc -Wall infilename.c -o outfilename.o```
- -Wall flag enables compiler warnings

## Debugging

- use gdb
- GDB = GNU Project Debugger

## Using GDB

- useful commands:
```break <linenumber>``` - create a breakpoint at specified line
```break <file>:<linenumber>``` - create breakpoint at line in file
```run``` - run program
```c``` - continue execution
```next``` - execute next line
```step``` - execute next line or step into function
```quit``` - quit gdb
```print <expression>``` - print the current expression value
```help <command>``` - in-program help for command specified

## Memory debugging

- use valgrind for diagnosis of memory-related bugs

## IDE - All-in-One Solution

- integrated editor with compiler, debugger
- very convenient for larger programs

## Using Eclipse

- use Eclipse CDT for C programs
- New -> C Project -> Hello world ANSI C Project (for simple project)
    - "Linux GCC toolchain" sets up gcc and gdb

## Structure of a .c file

- begin with comments about file contents
``` /* comment */ ```
- insert statements and preprocessor definitions
``` #include <stdio.h> ```
- function prototypes and variable declarations
``` const char[] msg = "a raw string"; ```
- define main() function
```
int main(void)
{
    const char msg[] = "Hello world";
    puts(msg);
    return 0;
}
```
- define other functions

## Comments

- can span multiple lines in the format above
- ignored completely by the compiler
- may appear anywhere in program

## The #include Macro

- macros are code that is replaced by their value
- the #include macro reads in the contents of a header file
    - e.g. #include <stdio.h> - provides basic I/O functionality

## Hello World

- [Hello World C program](../Programs/HelloWorld.c)
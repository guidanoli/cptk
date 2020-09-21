# Competitive Programming Language-Agnostic Toolkit

![](media/competitive.gif)

## Description

A toolkit for language-agnostic competitive programming, focused on _POSIX_ systems.

## Motivation

Even though C and C++ dominate the competitive programming ecosystem, it's not hard to spot some submissions using Python, Perl, Java, or even Fortran.
Every language has its pros and cons. Knowing many different languages can not only make you a better programmer but also a better competitor.

The problem is: keeping a polyglot development environment consistent and tidy is oftentimes harder than it may seem.
What this toolkit promotes is an abstraction for developing with different programming languages at once.

## Mechanism

Even though powerful, the toolkit only needs to remember one thing: the current programming language.
With this information, it triggers all the functionalities specific to that programming language.
For example, running a C++ application involves one list of commands; while running a Python script
involves a different list. But for the user, these are abstracted away into a single command: `./run`.

**The current programming language is the one that was last made explicit in a command.**

These commands can also take additional arguments. For example, compiling a C++ application may take custom compiler flags as in `./run c++ -O2`. Note that when additional arguments are present, the programming language name must be explicit, even when it is the default.

After cloning this repository, you need to define the programming language for the first time, by running, for example, `./src LANGUAGE`.

## Dependencies

### Core dependencies

* [bash](https://www.gnu.org/software/bash/)

### Peripherals dependencies

* **Editing**: [vim](https://www.vim.org/)
* **Clipboard**: [xclip](https://linux.die.net/man/1/xclip) or [clip.exe](https://docs.microsoft.com/en-us/windows/wsl/about)

### Languages dependencies

Since the project deals with a bunch of different languages, it's quite natural the need to have some software pre-installed on your machine.
Since you're most likely to work with only a few portion of them, the following table should summarize which are the dependencies that apply to your usage.

| Programming Language | Compiling and running | Debugging |
| :- | :- | :- |
| c | [gcc](https://gcc.gnu.org/), [make](https://www.gnu.org/software/make/) | [gdb](https://www.gnu.org/software/gdb/) |
| c++ | [g++](https://gcc.gnu.org/), [make](https://www.gnu.org/software/make/) | [gdb](https://www.gnu.org/software/gdb/) |
| c# | [mcs](https://www.mono-project.com/), [make](https://www.gnu.org/software/make/) | |
| go | [go](https://golang.org/) | |
| java | [javac](https://docs.oracle.com/javase/7/docs/technotes/tools/windows/javac.html), [java](https://docs.oracle.com/javase/7/docs/technotes/tools/windows/java.html), [make](https://www.gnu.org/software/make/) | |
| kotlin | [kotlinc](https://kotlinlang.org/docs/tutorials/command-line.html), [java](https://docs.oracle.com/javase/7/docs/technotes/tools/windows/java.html), [make](https://www.gnu.org/software/make/) | |
| pascal | [fpc](https://www.freepascal.org/), [make](https://www.gnu.org/software/make/) | |
| perl | [perl](https://www.perl.org/) | |
| python | [python](https://www.python.org/) | |
| ruby | [ruby](https://www.ruby-lang.org/en/) | |

## Contribution

If you have a language that you'd like to be added, don't hesitate to send a pull request.

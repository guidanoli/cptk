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

These commands can also take additional arguments. For example, compiling a C++ application may take custom compiler flags as in `./run cpp -O2`. Note that when additional arguments are present, the programming language name must be explicit, even when it is the default.

After cloning this repository, you need to define the programming language for the first time, by running, for example, `./src LANGUAGE`.

## Dependencies

If you're using any _POSIX_ distribution, you're most likely good to go.

### Base scripts

* bash
* vim

### C

* make
* diff
* C compiler

### C++

* make
* diff
* C++ compiler

### Python

* Python interpreter

### Java

* JDK

### Ruby

* Ruby interpreter

### Kotlin

* Kotlin compiler
* JDK

## Contribution

If you have a language that you'd like to be added in the cfg/langs folder, don't hesitate to send a PR request.

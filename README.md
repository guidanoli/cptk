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

Once you have cloned this repository, you may first set the current language by running `./edit LANG`.
(You can close the text editor without saving for now)

Now that the current language is set to LANG, the next time you want to edit the code in this language, you can omit it from the command (`./edit`).
This implicitness applies to the other commands too: `./run` and `./src`.

## Dependencies

If you're using any _POSIX_ distribution, you're most likely good to go.

### Base scripts

* bash
* vim

### C/C++ support

* make
* diff

## Contribution

If you have a language that you'd like to be added in the cfg/langs folder, don't hesitate to send a PR request.

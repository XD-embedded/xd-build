---
title: XD-build
author: Esben Haabendal
---

### What is XD-build

As a part of the XD-embedded project, XD-build is a build system, part of the
@XD-embedded project.  XD-build is designed for for cross-compiling entire
embedded Linux systems.  It is not limited to development of embedded Linux
systems, but design choices are made with this in mind, so it might or might
not be usable for other purposes.

XD-build has it origins in the OE-lite project, which again is based on
OpenEmbedded (and thus indirectly Yocto Project).


#### Project goals

To be a bit more concrete, the goal of the XD-build project is to develop a
build system with the following features:

* software projects integrated into XD-build is build using their own build
  system
* build host can be any Linux machine (given enough memory and diskspace)
* target software is cross-compiled
* build output is independent of build host
* builds are reliable and reproducible


#### Technological choices

To reach the goal of this project, the following technological choices are
made (current plan):

* XD-build is written in Python (3.4+)
* XD-build recipes are written in a custom DSL (domain specific language),
  which is mostly based on Python syntax, but borrowing some features from
  OE-lite/OpenEmbedded
* Each task (fx. glibc do_compile) are executed in its own docker container


#### Focus on developers

In this phase of the project, the focus is to serve the need of XD-build
developers.  This includes both developers wanting to help develop the
XD-build system, and those wanting to help develop recipes for XD-build.

As a consequence, we must focus on:

* Developer documentation, both source-code and design documentation
* Code quality
* Developer friendly features, fx. debug features


#### KISS

Oh, and just as with OE-lite: KISS.


#### Contact

I haven't set up a mailing list, so if you find this interesting, and would
like to hear more.  Don't hestitate to contact me: esben@haabendal.dk

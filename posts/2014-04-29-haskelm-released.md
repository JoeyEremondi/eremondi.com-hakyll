---
title: Haskelm released
author: Joey Eremondi
date: 2014-04-29 0:00
comments: true
description: Haskelm, my Haskell to Elm translation library
tags: haskell, elm, translation
---

I've created a library, which I lovlingly refer to as Haskelm.
It uses TemplateHaskell to read Haskell source and translate it into
Elm code, which can be compiled and run in the browser.
The library also automatically generates the Elm code to convert
JSON objects to ADTs using the same scheme as Haskell's Aeson.TemplateHaskell.

You see the package on [hackage](http://hackage.haskell.org/package/haskelm) or 
[github](https://github.com/JoeyEremondi/haskelm).
It as a Haskell library, embedding Elm source
in Haskell code at compile-time using Template Haskell.
It also contains an executable, which reads Haskell source from stdin
and outputs Elm on stdout.

I see two main uses for this.
The first is having unified algebraic data types between the
front and backend of a server. This would allow you to use Yesod,
Happstack or Snap as your web framework, but write your interface
in Elm.

The second is to allow for the fast porting of Haskell libraries
to Elm. This should allow the Elm ecosystem to grow quickly,
and packages to be developed easily.

If you're unfamiliar with Elm, it's a nifty language: pure, functional,
and based around reactive programming (FRP).
It compiles to JavaScript, and allows for fast development of
interactive web games and programs.
You can read more about it at [the Elm website](http://elm-lang.org),
or [try it in the browser](http://elm-lang.org/try).

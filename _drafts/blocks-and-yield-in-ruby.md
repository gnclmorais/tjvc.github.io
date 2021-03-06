---
layout: post
title:  "Blocks and yield in Ruby"
date:   2020-01-03
---

I've found that the simplest way to think about blocks is as functions passed into methods for execution later.

`yield` calls a block. Any arguments passed to `yield` are passed to the block. You can pass a block explicitly (as opposed to implicitly), to a method with an ampersand parameter, which allows you to then `call` that block. Passing a block like this converts it to a proc.

Procs and lambdas are like blocks, but they can be stored in variables. Both retain the scope within which they were defined (they are closures). Procs and lambdas behave slightly differently: calling `return` in a proc will return from the calling method, whereas a lambda will just return from itself; lambdas enforce arguments, whereas procs do not.

A good reference: <https://blog.appsignal.com/2018/09/04/ruby-magic-closures-in-ruby-blocks-procs-and-lambdas.html>

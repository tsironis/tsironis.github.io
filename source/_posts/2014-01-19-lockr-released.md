---
layout: post
title: "Lockr v0.5.0 released"
---
Few months ago, I have written a prototype of a library to use ```localStorage``` more efficiently. In the meantime, I totally forgot about it until I started writing the v2.0.0 of the [BugSense JavaScript SDK](https://github.com/bugsense/bugsense.js).

So I started development for bugsense.js and I run into the same issues using the native ```localStorage``` API. I needed something modular, lightweight and with a very small bytesize.

And then it came to me. I had already written most of the library, although it needed some work to be combat-ready.

Eventually, I designed the API wrapper very much influenced by the [node_redis](https://github.com/mranney/node_redis/) client. I wrote some specs for it, make sure everything is working as it should and here it is.

It's a very early version, but I do want to keep it that simple in the future, maybe with some extra features.

I would love your feedback to make it more awesome and to have more stuff in v1.0.0. Give it [some love](https://github.com/tsironis/lockr/star) or [fork it](https://github.com/tsironis/lockr/fork) to make it better!


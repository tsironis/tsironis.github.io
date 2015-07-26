---
layout: post
title: Enjoyable Javascript
---

## The first handshake
When I started learning the building elements of the Web, I had the impression that Javascript is that hefty, untamable
beast that nobody really understands, a language so wicked that noone really
wants to write it anyway, although it's inevitable.

Let's get this out of the way. Javascript is not an inherently bad language. Its notoriety
originates mainly on some crappy browser and DOM APIs, bad implementations of specs
and the general ambiguity that reigns in the Browser Vendors Land. Yes, it is a
stil very immature language but that doesn't mean it's not powerful enough.

## Getting more intimate

For people that aren't very familiar with it, writing Javascript is just a matter of registering some jQuery events which control animations. Writing webapps in Javascript puts you in a completely different state in which you **need** to write modular, maintanable and testable code. You have to organize your code efficiently in order to avoid having a "spaghetti code" codebase.

When I joined [BugSense](http://bugsense.com/), I immediately started to put all of the above principles in
practice. Backbone.js isn't opinionated enough to force me to structure or code in some particular
pattern, so I was starting anew. Coming from a more opinionated background, in which
I had a basic code structure already layed out, I was kinda freaked out.

It turns out that taking key decisions about my project on my own is one of the best things that I
learned while writing Javascript.

## Javascript is flexible

One of the wow moments I had with Javascript, was the ability to easily do
evaluations, one-liners (almost LISPy things) without having to bleed through
my ears. Events, closures, functional js, being able to do this...
{% highlight js %}
X ? doSomething() : doSomethingElse()
{% endhighlight %}

...made me fall in love with it after a while.

## Building a decent workflow

I think this point is true for every language. You should try moving things out
of your way, optimizing your everyday work, organizing your project's structure as well as possible and having repetitive tasks done automatically. It should be just you and the language, nothing more. Especially for Javascript you should try having multiple files and concatenating or minifying them with Grunt.

## Getting serious

If you're in a state that you want to take it to the next level, then I think you should try strict mode. Just put ```use 'strict';``` at the top of your js files. This have
will help you write more consistent code across implementations and [other
things](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/Strict_mode).

Most importantly, don't hate Javascript, but instead you can try to get the most out of it. All languages and tools have their limitations after all.

The question is could you rise to the occassion?

[Join the discussion on Hacker News!](https://news.ycombinator.com/item?id=6790254)

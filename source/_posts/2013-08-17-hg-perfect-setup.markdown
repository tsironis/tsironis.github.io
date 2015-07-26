---
layout: post
title: Mercurial's perfect setup [Part. I]
---

I've been using Mercurial every day, since I joined BugSense a few
months ago. At the time, I was an advanced Git user and it took me a
while to understand what exactly is Mercurial's philosophy and adapt my
workflow to the new system.

So, I spent a good amount of time to finetune my configuration and find the perfect setup for my Mercurial
workflow. I use a handful of already built-in (but not enabled by default) extensions, some external extensions and some custom aliases to
facilitate some more complex tasks.

As of this writing, the <code>hg \-\-version</code> is 2.6. If you haven't update it yet,
please do since some the following extensions are available only in
newer versions of Mercurial.

### Rebase
I think the feature of git that I really missed is
rebase. Mercurial's rebase is not as hardcore as Git's rebase but it
does the work done. You can enable it in your <code>~/.hgrc</code> file.
```bash
[extensions]
rebase = 
```
 I mainly use rebase for fetching commits from the
upstream repository (Bitbucket, self-hosted hg, you name it). This is a very basic
usage of rebase extension and it actually does have a lot more built-in functions but I don't really need them in my current workflow.
```bash
$ hg pull --rebase
```

This is very useful in my case because it solves
Mercurial's serious flaw (in my opinion) with continuous merges, that
litter repo's history with useless merge commits.

### hg-prompt
This is an awesome extension by [Steve Losh](http://stevelosh.com/), that allows
you to display all the useful info about the Mercurial current repo in your
terminal.

Steve has an [excellent documentation](http://sjl.bitbucket.org/hg-prompt/) about installing and getting started with this extension but also, has written a blog [about his
zsh setup](http://stevelosh.com/blog/2010/02/my-extravagant-zsh-prompt/#mercurial-repository-information), including several details about <code>hg-prompt</code> .

### graphlog
Graphlog is a built-in extension for Mercurial, which is the equivalent of
<code>git log \-\-graph</code> and it ***formats the output as a graph representing the revision history using ASCII characters to the left of the log***, quoting extension's description.

In order to use it just enable it in your <code>~/.hgrc</code> config
file and your good to go. 
```bash
[extensions]
graphlog =
```
You can use it by typing the following in your
terminal:
```bash
$ hg log -G
# or
$ hg glog
```
Personally, I use it via an alias, just a shorthand to make it more accessible,
nothing fancy at all. It still accepts all the options of glog.
```bash
[alias]
lg = glog
```

### hg blame
One other Git command that Mercurial really needs is the <code>git
blame</code>. This one isn't exactly what you might think, it's just for
finding in which commit or changeset a line was added or last modified.
It's pretty handy as the time goes by and chances are you have forgotten
what you have written a few months ago.

So the [solution](http://stackoverflow.com/questions/2228188/finding-the-author-of-a-line-of-code-in-mercurial) I found on Stack Overflow was using the <code>annotate</code> command with a few arguments. I took this and after I added my preferred arguments I create an alias in order to create <code>hg blame</code>.

Here is the code for this alias:
```bash
[alias]
blame = annotate --user -c
```
Now, you can just type the following and you will
be greeted with a nice output showing user and changeset number next to
each line.

```bash
$ hg blame <path-to-file>
```

Combine that with <code>grep</code> or <code>ack</code> and you have a
power tool in your hands!

```bash
$ hg blame <path-to-file> | grep "some words"
``` 

### pager
Very nice and handy plugin to add <code>less</code>-like functionality for commands that have huge outputs, eg. log, diff etc.

It's easy to setup and already included with Mercurial.
```bash
[pager]
pager = LESS='FSRX' less
attend = cat, diff, glog, log, incoming, outgoing, lg, show, lg
```

### The end
I will come back with a second part, covering the rest of the plugins I'm using.

Head over to [Hacker News](https://news.ycombinator.com/item?id=6319979) for the discussion


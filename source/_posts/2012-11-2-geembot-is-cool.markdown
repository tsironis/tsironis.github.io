---
layout: post
title: Geembot is cool!
---

## How we deployed our own robot in da cloud

Few months ago, I started following [@holman](http://zachholman.com/) on Github and Twitter. He's doing a great job on Github and on open-source projects and he's creating some very interesting video and screencasts.

One of the videos was about Play, a music manager by Github and how they can play their music from the Campfire chat rooms using Hubot, which is a very cool little robot written in Node.js.

At the time, I was thinking it would be cool to deploy my own Hubot but I didn't find any cause for doing such (except being a geek). So, when I started Geembo last month or so, I started thinking of using Hubot to have some fun but also, to automate some of our everyday tasks.

So, Geembot was born today, after few hours of screwing around its source code. The initial plan was that it would be deployed on Heroku, but soon enough we found out that Heroku and Node.js or perhaps hubot don't match very well together.

So, I fired up a fresh Ubuntu 12.04.1 LTS VM and deployed Geembot.

I can tell you, it's not easy to deploy a hubot. But if you're an advanced system administrator, I think you would success soon enough.

Geembot is very cool, fast and very extensible. The scripts already written for hubot are literally hundreds and we have to search what we gonna do with him.
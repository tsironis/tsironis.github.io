---
layout: post
title: "(maximum-awesome)^2"
---

### In the quest for the perfect conf

In my previous post, I wrote about my experience [switching to Vim](/posts/how-to-vim/). After getting familiar with using Vim, I started to search on ways to improve my workflow. At the time, I was using Janus build and I have to say, I didn't enjoy it too much. So I had two choices; the first was to start off and build my own Vim configuration from the ground up and the second was to find a "pret-a-porter" solution. I chose the latter and head to Github to start the quest of finding the perfect Vim configuration. I had already excluded Janus because way too complicated to mess around with and it's pretty heavy as well. Then, I remembered about [Subvim](https://github.com/fatih/subvim/) which is a great effort to emulate Sublime Text 2 in a Vim environment. That didn't suit me as well, found it to be heavy and just not my taste.

### The Holy Grail

And then I remembered about [maximum awesome](https://github.com/square/maximum-awesome), made with love by Square and decided to install it right away to test it out. And boy, it is good! First of all, the installation process is simple, painless and quick. I fired up my MacVim and tried it out. My first impression was that it felt agile, looked beautiful but lacked some functionality that I've been used from my previous configurations.

Almost right away, I decided to fork it and made my changes available for all and also, have them backed up in Github (just in case).

### A minimal Vim configuration

And that's how [(maximum-awesome)^2](https://github.com/tsironis/maximum-awesome-squared) was born, humbly named after his great ancestor!

Right away, I had some issues with the status line, so initially I went with Powerline and minibufexplorer, but after a while I switched to the vim-airline which does both things (and which I love). Also, around that time I started using Jellybeans colorscheme. Made some other changes in the vimrc and I was pretty happy with my setup.

![Maximum Awesome Squared animation](http://i.imgur.com/GUUm9q0.gif)

### Ubuntu support?

Ok, maximum awesome is built for Mac OS X, but I didn't see any valid reasons why it couldn't play on Ubuntu as well. And also, I really, really needed my config in my Ubuntu desktop as well. So, I made the decision to hack the original Rakefile in order to made it work nicely with Ubuntu. Although I'm not that happy with the quality of the new version, I made it work. Maybe some time in the future I'll do some optimisation.

### Customize it!

The great advantage with the maximum-awesome is that you can easily hack it, change it, make it unique. I was familiar with the code in about thirty minutes or so. If you want to change the plugins, just edit the ```.gitmodules``` file and run ```rake```. Make your personal changes (changes that will only be interesting to you, that is) in the ```vimrc.local``` file. The script will download the new plugins and everything else should be taken care of by Pathogen.

### Future plans

#### Full Ubuntu/Debian support
There are some things that are very sloppy about the rakefile, I plan on making some optimizations and also, finding a way to offer greater support for Ubuntu/Debian systems but also, other Linux distros as well.
#### Better installation experience in both platforms
Currently, the implementation of the installation plugin is not that elegant and I want to encourage the customization and make it as easy and seamless as possible.
#### Better handling of Git submodules (plugins)
The downloaded plugins in the ```vim/bundle``` folder shouldn't be added in the repo, instead they should be just local copies and everything should be handled through the ```.gitmodules``` file. I plan on improving that.
#### Improve Vim performance
Sometimes, MacVim and Vim feels heavy, especially after some hours of usage. I plan on making make it faster and less heavyweight (or at least, investigate why)

### Conclusion

[(maximum-awesome)^2](https://github.com/tsironis/maximum-awesome-squared) is just my take on the original project. If you like it, fork it and let's make it better!

[Join the discussion on HackerNews](https://news.ycombinator.com/item?id=6462427)


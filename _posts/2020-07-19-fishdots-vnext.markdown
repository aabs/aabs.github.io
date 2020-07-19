---
layout: post
title: fishdots rewrite
---

Fishdots and its plugins were groaning under their own weight. It's in-memory function definitions model, inherited from before it was even a fishy thing, led to some serious load time lag.  Combine that with extensive use of tmux, and you have a recipe for frustration!

The repo [fishdots2](http://github.com/aabs/fishdots2) ports everything over to use the inate autoloading capabilities of fish shell.  In the process of the rewrite, i've taken the chance to break it up, and make fd2 simpler and more clearly focused.

It now has just these roles:

1. auto-run user and machine supplied dotfiles during shell startup
2. provide logging functions 
3. simple autoenv style functionality
4. simple file finding, selection and searching

Everything else that it used to do is now gone.  This includes installers, plugin commands etc.  In future just use fisher or omf.

Over the next few weeks, expect more plugins to be released, as I port existing fishdots v1 plugins over.
---
layout: post
title: "Zaw Plugin"
date: 2015-02-04 12:44:15 +1300
comments: false
categories:
 - zsh
---

### What is zaw ###

Zaw is zsh plugin which acts like a widget to bring together a wealth of resources
making it easier to find what you need in you shell.

<!-- more -->

### How do I use it ###

I use zaw mainly to replace the reverise lookup functionality of zsh, why?
Because zaw allows wildcard and incomplete searching of commands as well as a
nice scrollable list.

I also like it because I can hit `tab` and get an option to edit the histroy
command in the buffer before executing it.

### Installation ###

My installation is available off my dotfiles repo, but if want to install this
manually - to how I run it, follow these steps:

Im making an assumption you're using the [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) framework.

#### Step 1: Clone the repo ####

`git clone git://github.com/zsh-users/zaw.git`

#### Step 2: Update zaw plugin ####

We want to update the zaw plugin code to use ^R key binding, and to limit the output to 10 lines,
do to this open `zaw.plugin.zsh` file in the root of the zaw repo and update the following lines:

{% codeblock %}
  bindkey '^R' zaw-history
  bindkey '^Z' zaw

  #zstyle ':filter-select:highlight' matched fg=green
  zstyle ':filter-select' max-lines 15
  zstyle ':filter-select' rotate-list yes
  zstyle ':filter-select' case-insensitive yes
  zstyle ':filter-select' extended-search yes # see https://github.com/zsh-users/zaw for explanation
{% endcodeblock %}



#### Step 3: Setup zshrc opts ####

Here we want to disable search dups in our history as zaw by default loads your entire history file,
which can make it bloated, slow and hard to get what you want fast.

Add the following options to your `~/.zshrc` file:

{% codeblock ~/.zshrc %}
setopt APPEND_HISTORY
setopt EXTENDED_HISTORY
setopt INC_APPEND_HISTORY
setopt HIST_FIND_NO_DUPS
setopt HIST_IGNORE_SPACE
setopt NO_HIST_BEEP
setopt SHARE_HISTORY
setopt HIST_IGNORE_ALL_DUPS
setopt HIST_IGNORE_DUPS
{% endcodeblock %}



#### Step 4: Reload zsh ####

Lastly reload your zsh shell by using `source ~/.zshrc` or loading a new terminal window.

---
layout: post
title: "Cloning Your Octopress Blog"
date: 2015-02-10 08:43:56 +1300
comments: true
categories:
 - git
 - octopress
---

I've spent hours and many 'dud' commits to my github repository trying to figure
out too re-clone my octopress repository to either my current development
computer, or too another one. I have found one working solution.

<!--more-->

**Attempt 1: Straight Clone: Failed** - Dont clone only the master branch as this
only contains your site static code and not the development branch.

**Attempt 2: Clone source branch: Failed** - I have the correct source but no
static content on the master branch.

**Attempt 3: Git Submodules: Failed** - Dont use submodules to manage the master
branch - They'll give you a world of hurt and constant commit hash errors when
you deploy your site with changes.

**Attempt 4: Clone into \_deploy: Sucess!** - This works a treat as I realised
`_deploy` is in the default `.gitignore` file of octopress. So it wont error on
changes or be commited up when you push the source branch.

**How I Got There:**

1. `git clone -b source https://github.com/daniel-gadd/daniel-gadd.github.io`</li>
1. `cd daniel-gadd.github.io`</li>
1. Accept `.rvmrc`, allowing rvm to create a gemset and bundler install to the gems</li>
1. `git clone -b master https://github.com/daniel-gadd/daniel-gadd.github.io ./_deploy`</li>

Thats it!

You dont need to re-set up the github pages configuration as this is already setup in the gitrepo

**NB:** Remember to push both your source and master branches after each change, if your working on two computers, your local repos can get out of sync badly requiring some rebasing and merging.

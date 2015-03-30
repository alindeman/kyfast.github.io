---
layout: post
title: "Hub for GitHub"
description:
category: tools
---
I'm trying to keep track of the tools I use most and also remember how to use them. Since I have a terrible memory I'm doing the thing where you write you blog posts as reminders for yourself so here's the first one:

### Hub

What is Hub? [Hub](https://github.com/github/hub) is a command line tool that wraps `git` in order to extend it with extra features and commands that make working with GitHub easier. (*Ed note: A+ copy-pasting Kylie!*). The hub project recommends you alias `git` to `hub` but I prefer not to do that so I can remember which are `hub` commands and which are `git` commands.

I mostly use hub for creating pull requests from the command line and for creating GitHub remotes. I still use a few gui-based tools for development(namely my [editor](http://www.sublimetext.com/)), but I'm getting comfortable with more "keyboard-only" tools and feel I'm able to move faster when I use them.

### Hub Pull-Request

Hub's `pull-request` is the command I use most. `hub pull-request` allows you to create a pull request between your current branch and any other branch on your project. This is particularly handy for me because my workflow for work involves feature branches that are merged into a `staging` branch where features are accepted or rejected before being merged into a `master` branch that goes into production.

Despite the fact that I use this command near daily, I almost always forget that I need to push my branch to the GitHub remote to create a pull request. Just like using the GitHub web gui you can't create a pull request for a remote that doesn't exist. Here's the workflow I use when I write features:

1. Check out a feature branch

`$ git co -b kyfast/excellent-feature`

2. Write & commit code

3. Push feature branch to remote. I should also note I have git configured to automatically set up remotes when I check out a new branch on existing GitHub projects.(*Ed note: this is the part you always forget*)

`$ git push`

4. Open Pull-Request from the command line. There are a few options you can pass in her but I usually just use -b to indicate which branch I want to open my pull request against:

`$ hub pull-request -b staging`

That command opens up your git config editor so you can write a pull request title:

```
  0 
  1 # Requesting a pull to kyfast:staging from kyfast:excellent-feature
  2 #
  3 # Write a message for this pull request. The first block
  4 # of text is the title and the rest is description.
```
all done! Hub will spit out the url of the pull request in your terminal so you can check it out online.


### Hub Create

My second most used `hub` command is `create`. `hub create` creates a github remote for you on your default account in any git repository. Here's the basic workflow from within your project's directory:

1. Initialize git repo(let me know if I'm going too fast):

`$ git init`

2. Create a remote with hub:

`$ hub create`

that's it. That's the whole thing. Hub will spit out a confirmation that your remote has been created:

```
Updating origin
created repository: KyFaSt/excellent_project
```

### Hubbub About Hub

If you are already using git-cli to interact with GitHub and enjoy it, I recommend you install and try out hub. It's easy to use and saves extra clicks that you should be using on [cookies](http://orteil.dashnet.org/cookieclicker/) instead.

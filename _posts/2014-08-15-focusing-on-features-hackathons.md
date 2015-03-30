---
layout: post
title: "Focusing on Features at Hackathons"
category: tips
---

You might have a lot of reasons to participate in a hackathon but one of my goals is to learn something new. For me at least, I hope that something new will be how to implement a feature I haven't before or get more comfortable with an unfamiliar language. To make it easier to learn something new, I have picked up a few things that help me reduce distractions and focus on writing code.

### Stop

Before I get ahead of myself thinking about the awesome feature-packed app I want to build, I try to take a minute to make sure I have all the tools I need. For me, that includes making sure  I'll be able to make something that not only works well internally but also appeals to users.

I like to try to find someone with front end development or design experience to work with, then  my app looks great and I've met someone new. A site with appealing design confers professionalism and an essence of completeness to judges.

If you're unable to find a designer to work with, and you promise you really tried (sometimes I get too shy to ask anyone, so that doesn't count) you can always use some prepackaged styling. The biggest mistake I've made before in this area is thinking it's easy and waiting until the last minute to "slap bootstrap on there." I try now to include styling as one of the first few steps after `rails new`. [Twitter Bootstrap](http://getbootstrap.com/) is very popular but I also like [Zurb Foundation](http://foundation.zurb.com/).

### Collaborate

Working with other developers, designers & possibly non-technical team members can be challenging especially if you feel like you don't speak the same language.

Encourage teammates to focus on single responsibility additions to your code base by using git branches for features. This makes it easier to merge in individual features, and helps to keep each contributor laser focused on one task at a time. Additionally if someone needs to trade off of a feature, someone else can pull down that feature branch to get just the code they need.

Keeping track of all of those feature branches can be time consuming, and possibly complicated for less technical teammates. A friend introduced me to a chat room-like software called [Gitter](https://gitter.im/), which integrates with Github, Bitbucket, Trello, Travis & several more code/project management tools. It has a chatroom & shows a feed on the right of recents commits, pushes & updates. I think it is a great way to integrate non-technical team members into the development process & can reduce possible "us vs. them" mentality.

### Listen

At the end of a hackathon, each team is usually asked to create a 5-10 minute demo of their work. Some teams might be scrambling to implement features or others might be there physically but maybe not so there mentally. I try to think of things that will make it easier for an audience to watch the presentation, or if the final product allows it, try out the app themselves.

The first thing is pre-populating the database, either by writing some [custom rake tasks](http://railscasts.com/episodes/66-custom-rake-tasks?view=comments) or using the ruby gem [faker](https://github.com/stympy/faker). Filling the app with some information helps the audience visualize how it will look in production as well as really making any of features based on user-input or data analysis shine.

Another thing I like to keep in mind is preventing the user from seeing the dreaded Heroku "We're sorry, something went wrong" page. This can happen for any number of reasons but recently I've experienced it by letting a user pass a nil value to a required field. To prevent this in the future, I like to user either [HTML5 validations](http://diveintohtml5.info/forms.html#validation) or a rails formbuilder like [Formtastic](https://github.com/justinfrench/formtastic) or [Simple Form](https://github.com/plataformatec/simple_form) which select the user input field type based on the database column-type. The form builder options can really come in handy when you don't have a dedicated designer on your team.

### A Brand New Invention

A lot of what I've collected above is pretty rails-focused, because that's primarily what I've worked with during hackathons (excluding a misguided but semi-successful [attempt at JavaScript](http://earthspy.herokuapp.com/)). Hopefully I'll be able to find some tools to make features my main focus in other languages and frameworks soon. For now though, I'm pretty excited about the idea of doing some purely ruby based hacking. If you are too, you should join me at Big Nerd Ranch's [Ruby Data Structure Hack Night](http://www.bignerdranch.com/blog/data-structure-hack-night-at-big-nerd-ranch/) on Monday August 25th 2014!
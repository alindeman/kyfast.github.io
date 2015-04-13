---
layout: post
title: "Letters to a Young Developer, pt. 2"
description:
category: letters-to-a-young-developer
---

Full disclosure, I still consider myself a new-ish developer. I've only been in my current job for about a year (I was intern at the same company before hand but I kind of don't count that). I've also been on the same project the entire time. That's all to say, I haven't been able to test these things out on a totally new project.

### Read About the Dependencies

If you're new to a Ruby project, read the whole Gemfile & find out what each of the gems do. Each of the gems (should) correspond to features or developer tools on the project. If it's not a Ruby project, look up each of the non-standard libraries your project is dependent on. If your project doesn't have a lot of non-standard libraries, there's probably a reason for that. Maybe it's an older project with no support for newer libraries. Maybe your product requires extremely strict auditing of outside tools so it makes more sense to roll your own. If you research the dependencies really well, you might even notice that a dependency is unused and can be removed (hello, first pull request).


### Read and Write Tests

Your new project hopefully has some tests in place. Even if someone says "Oh our test suite needs work," Read those tests! I have a lot of thoughts on tests, but the one that's relevant here is the idea that a good test suite can be your app's documentation. I definitely hear and understand the argument that good code should be it's own documentation but in the real world I don't think it's always possible. Complicated logic might be a code smell, but if that's the nature of the application then the true behavior might be easier for a newbie to parse from tests rather than the code itself.

More likely than not though, there are probably a few places in your new test suite that need coverage. You can use code climate (if your project has it set up) or ask someone on your team for units or features that need testing. You'll learn a lot about the project & it's a great way to add value for everyone on your team. A strong, trustworthy test suite inspires confidence in merges and deployments to production.

### Pair Program

Pair program with everyone on your team. I wouldn't try too hard to pick up a lot of new tools (unless you need them) right now, just try to get more knowledge of the domain. Unfortunately, many teams rely on tribal knowledge and the only way you'll learn some of the quirks of your new is by hearing about them from someone else. More importantly though, you'll get to know your new teammates. It's much easier to interpret out-of-sync communications (emails, slack messages, comments on code review) charitably when you already have a good relationship with those on your team.

###Learning How to Join a Team

So what would I tell 1.5 years younger Kylie? You're not having a hard time of this because you're a newbie developer, you're having a hard time of this because joining a new team is hard.

Don't try to drink from the firehose on day 1. It's tempting, you feel like because you've been hired as a developer that you're expected to write great code from the start. You might be able to, but if you're not don't feel terrible. You don't have the context of the whole project yet, and that's okay as long as you have a plan.

Here's a good plan until you start to get a hang of the project:

- Read the Gemfile, figure out what this project depends on and why.

- Read and write tests, tests can contain knowledge of user features and interesting edge cases that might be difficult to otherwise divine.

- Pair program. Don't schedule to pair once and then never do it again out of shyness. If someone tells you to pair with them whenever they're available, take them up on this. Schedule to pair with each person on your new team at least 1x a week.

### Letters to a Young Developer

This was part two of a series called "Letters to a Young Developer" where I'll share the great advice I got, or the advice I wish I'd gotten when I first started learning Ruby. This post was written as a pre-cursor to a post I'll write soon about moving from feeling like an individual contributor to feeling like a full team member. I was inspired by Kate Heddleston's talk from GoGaRuCo on [Technical OnBoarding, Training and Mentoring](https://www.youtube.com/watch?v=3XfwanJe77s).

When I first started my current project, I had a lot of good internal resources from my company but I pretty quickly got muddled with all the new information. The stuff I wrote about here are the things I wish I'd kept in mind when I first onboarded.

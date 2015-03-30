---
layout: post
title: "Refreshing my Site with Github Pages & Google Domains"
category: tips
---

### Dang
You might be thinking "dang, this is a pretty good looking site." 

You would be correct in thinking that, this site looks pretty good. Thanks to [a sweet new theme](https://github.com/poole/hyde) and a few simple tools, refreshing my site was easy and painless.

### Tools

This site is built with [jekyll](http://jekyllrb.com/) so the first thing I did was select a proper theme. Previously I'd cobbled together the css for my site on my own and without any design experience, it looked messy and busy. I chose the hyde theme by [@mdo](https://twitter.com/mdo) because of how simple it looks. But because it actually has a fairly simple structure it provides the flexibility to customize later.

I chose to continue hosting through [GitHub Pages](https://pages.github.com/) because pushing changes to my live site is just as simple as `git push`. This is a fairly simple setup (not to mention easy to maintain) but without a domain name, the site still sits as a subdomain of github. There's certainly nothing wrong with that but I think I'd like something a bit fancier.

That's where the fun part comes in. I'd actually never purchased a domain before or put a site on the web that wasn't a rails or javascript app so this is foreign territory. Fortunately with GitHub Pages & the newly introduced [Google Domains](http://domains.google.com/about/)* setting up a custom domain is virtually effortless.

### The Hard Part

Just kidding, this was a walk in the park. First things first, I purchased the kyfast.net domain name from Google Domains for a reasonable price of $12/yr.

In the root folder of my project I created a file called `CNAME` that only contains the domain name I want my site to be hosted at:
<script src="https://gist.github.com/KyFaSt/3e5799c9c9cb90f80090.js"></script>

I pushed this up to the master branch on github & then checked on the repo's settings that changes would be pushed to my domain:
![github pages](/assets/img/site-refresh-github-pages-settings.png)

That wasn't too bad, just one step remained: pointing the the domain to the web server where my site was hosted. This part was a little trickier, I knew I needed to set up a custom resource record but I wasn't certain which type to use.

After some searching through GitHub Pages' help resources I found [this page](https://help.github.com/articles/tips-for-configuring-an-a-record-with-your-dns-provider). Here I determined I could set up my custom resource route as type 'A'. After navigating to the 'advanced' section of this domain's management page I input the IPs provided from the GitHub Pages help:
![github pages](/assets/img/site-refresh-custom-rscrc-records.png)

I ran `dig kyfast.net` from my command line & returned the two IPs I set in the resource record:
![github pages](/assets/img/site-refresh-dig.png)

Alternatively, you can always just hit your site & make sure it's serving the content you expect.

### Retrospective

Updating and maintaining my personal site has been a frustrating experience until now. I thought because I'm a developer I should be able to figure out how to do the design piece of a website, but I'm not at that point in design yet. By really simplifying the theme and being realistic about what I need my site to do, I'm able to screen out distractions (like my old garish color schemes) & focus on the content that matters.

*Google Domains is still in invite-only beta mode as of 08-08-2014
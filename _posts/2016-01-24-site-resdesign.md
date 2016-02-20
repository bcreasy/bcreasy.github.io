---
layout: post
title: "Site Redesign"
date: 2016-01-24 14:30:00 -0600
published: true
comments: false
categories:
- Meta
tags:
- Meta
- Web Development
---
I spent nearly all of my time this past weekend working on switching this site to a new and updated framework: just plain old [Jekyll](https://www.jekyllrb.com).

(Apologies for any RSS migration issues.  I'm 301 redirecting the old atom.xml to the current feed.xml.)

<!-- more -->

Since [2013]({% post_url 2013-05-06-back-to-the-future %}), when I brought this site to life, I'd been using [Octopress](http://octopress.org) as its static content generator.  Octopress started out as a fork of Jekyll that was highly customized, but over the years, it's seen less and less development.  I was in the mood for redesigning my website, but the amount of work that I would have needed to put into working with the old version of Octopress just wasn't worth it.  So I decided to just start fresh with plain old Jekyll and no third party stuff.

A nice thing about Jekyll is that it's pretty minimal as far as features go.  Like Octopress, Jekyll uses [Liquid](http://liquidmarkup.org) as its templating engine.  Because it's stripped down, I had to do a lot of customization to get things to behave how I wanted them to.

Some of the features of Octopress I wanted to bring over were:

- Post archive page
- Browsing of categories and tags
- Pagination with excerpts

Because Jekyll's documentation is also fairly minimal, I had to dig through all manner of discussion threads and github source code of other peoples' sites to find solutions or examples.

I eventually got things functioning how I wanted, though.  You can see my commit history leading up to where I felt it was ready for production [here](https://github.com/bcreasy/briancreasy.com/commits/8805fec33fef49f0b8c38c0f83726107482bc98e).

During this project, I had to refresh my memory on writing [SASS](http://sass-lang.com) and bring myself up to speed with modern web standards.  Not to mention having to dig deep into how Liquid templates are developed.

The site itself is still statically generated and contains zero javascript.  This ensures a fast page load times with the added benefit of being very secure.  I simply clone my repository, commit/push whatever work is needed, then run `jekyll build`.  This generates everything to a `_site` directory which I can then just rsync up to my server.  I like this workflow.

Now that I'm on an up-to-date framework, I'll likely start playing around more with redesigning the site often.  I may actually write more content.  I have a long list of post ideas written down.

Some TODO items:

- Find somewhere to put the little "about" blurb on the main page
- Maybe include Twitter and Strava feeds again

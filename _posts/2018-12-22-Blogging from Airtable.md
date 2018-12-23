---
layout: post
title:  "Using Integromat to automate post updates via Airtable, outputting to Medium, Website, Twitter, etc."
date:   2018-12-23
---
# Automate your posting via Integromat, Airtable, GIthub pages, and more

[Integromat](https://www.integromat.com) is a great tool to help automate manual processes around the internet. It also has a really nice visual layout for displaying your scenarios. This has set the tool apart from the others (IFTTT, Zapier, custom code) for me. 
Having a visual way to understand all of the various places my information flows is extremely useful for my brain to handle more complex systems. The other fun thing to do is to build a prototype of ideas using the tool and then sort out how to build a bespoke solution and turn it into a platform for others to use (more on that later).
Here's my use case: I have a personal website on Github pages that's running a Jekyll Theme. I typically use a Markdown Editor for MacOS. [Mou](http://25.io/mou/) and [Macdown](https://macdown.uranusjr.com/) are two nice editors, but you just need a text editor and [a guide](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) to use Markdown. 
Once I'm happy with my post, I'll save the file to my git repo for [robertcedwards.com]
(https://robertcedwards.com) with a specific file format with the date and title in the file name so Jekyll can understand.
I then push my changes to Github where a Github Pages build happens on the Jekyll theme, and the static website is update automatically.

This workflow is fine for my personal stuff, but I'm needing to automate and collaborate for other projects with teams involved, so using Integromat was the solution that will help me get the post out and be able to manage multiple projects and posts with others involved in the process too. 

I'm going to focus on using Integromat to poll an Airtable containing posts or articles and then create a new file via via my personal website that lives on Github Pages (w/Jekyll). This is a bit specific and meant for my needs, but you can see how easy it is to customize to use for all sorts of uses.
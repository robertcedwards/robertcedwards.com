---
layout: post
title:  "Tracking Supplements"
date:   2015-09-26
---

Having started down the path of understand my genes, my diseases and my need for supplementation I've found myself in a place with a ton of inputs that I'm introducing to my life and no way of tracking the madness that is a panoply of single supplements, vitamins, and nootropics. Along with the need to track the individual supplements, their dosages, frequency, etc. I also have the desire to, more seriously, track my symptoms and episodes, and more casually, track my mood, focus, energy levels, etc.. This would give me the ability to compare the various factors that may have be contributing to how I and my body feel.

This led me to, as per usual, end up hacking a solution for myself that I hope would expand into something useful for others. :thumbsup:

I started working on a simple static tools using javascript and Mixpanel to make simple buttons with a text field for dosage. The heavy lifting on the analytics side is handled exclusively my Mixpanel and allows me to concentrate on the front-end while still having robust tools for analyzing custom data.
![Mixpanel Supplement Report Screenshot](./images/mixpanel.jpg)

The basic page is just a set of buttons with text fields nested inside. When you click on a button the script grabs the name of the button and the number for dosage. It then sends it off to Mixpanel:

```javascript
mixpanel.track("Took", {"Supplement": this.text, "Dose": $(this).next('input').val();});
```

![Codepen example with buttons, screenshot](./images/gawVLE.jpg)



The next part is to wrap this in a proper web app so we can login and store new supplements and other things we want to track on the fly without the need to code anything more.
To accomplish this task we'll be using a combination of Angular.js and Firebase to help us with Simple Login via email or Social accounts, allow users privacy and the ability to add new items easily.

{% gist 1bbfacc094a378be285d gawVLE.markdown %}

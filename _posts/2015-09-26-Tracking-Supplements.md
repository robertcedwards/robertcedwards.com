---
layout: post
title:  "Tracking Supplements"
date:   2015-09-26
---

Having started down the path of understand my genes, my diseases and my need for supplementation I've found myself in a place with a ton of inputs that I'm introducing to my life and no way of tracking the madness that is a panoply of single supplements, vitamins, and nootropics. Along with the need to track the individual supplements, their dosages, frequency, etc. I also have the desire to, more seriously, track my symptoms and episodes, and more casually, track my mood, focus, energy levels, etc.. This would give me the ability to compare the various factors that may have be contributing to how I and my body feel.

This led me to, as per usual, end up hacking a solution for myself that I hope would expand into something useful for others. :thumbsup:

I started working on a simple static tools using javascript and Mixpanel to make simple buttons with a text field for dosage. The heavy lifting on the analytics side is handled exclusively my Mixpanel and allows me to concentrate on the front-end while still having robust tools for analyzing custom data.
![Mixpanel Supplement Report Screenshot](./images/%23action%3Asegment%2Carb_event%3ATook%2Cbool_op%3Aand%2Cchart_analysis_type%3Alinear%2Cchart_type%3Aline%2Cfrom_date%3A-3%2Cms_checked%3A%28%27Alpha%20GPC%27%3A%21t%2C%27Grapeseed%20Extract%27%3A%21t%2C%27Methyl%20B12%27%3A%21t%2C%27Methyl%20Folate%27%3A%21t%2C%27Neuro%20Optimizer%27%3A%21t%2CL-Theanine%3A%21t%2CNAC%3A%21t%2CP-5-P%3A%21t%2CTaurine%3A%21t%2Cddf%3A%21t%29%2Cms_values%3A%21%28NAC%2C%27Methyl%20Folate%27%2CP-5-P%2C%27Methyl%20B12%27%2CTaurine%2C%27Alpha%20GPC%27%2CL-Theanine%2C%27Grapeseed%20Extract%27%2Cddf%2C%27Neuro%20Optimizer%27%29%2Csegfilter%3A%21%28%28property%3A%28name%3ASupplement%2Csource%3Aproperties%2Ctype%3Astring%29%2Cselected_property_type%3Astring%2Ctype%3Astring%29%29%2Csegment_type%3Astring%2Cto_date%3A0%2Ctype%3Ageneral%2Cunit%3Aday.jpg?resizeSmall&width=550&alpha="Mixpanel Supplement Report")

The basic page is just a set of buttons with text fields nested inside. When you click on a button the script grabs the name of the button and the number for dosage. It then sends it off to Mixpanel:

```javascript
mixpanel.track("Took", {"Supplement": this.text, "Dose": $(this).next('input').val();});
```

![Codepen example with buttons, screenshot](./images/gawVLE.jpg)



The next part is to wrap this in a proper web app so we can login and store new supplements and other things we want to track on the fly without the need to code anything more.
To accomplish this task we'll be using a combination of Angular.js and Firebase to help us with Simple Login via email or Social accounts, allow users privacy and the ability to add new items easily.

{% gist 1bbfacc094a378be285d gawVLE.markdown %}

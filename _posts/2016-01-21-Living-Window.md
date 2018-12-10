---
layout: post
title:  "Living Window"
date:   2016-08-25
---
### Living Window

Getting started with a project is usually the tough part of an idea but the most important by far. Sometimes it can take months or even years for the spark of an idea to mature into something tangible. Other times it can magically take off from our minds and somehow manifest itself before our very eyes.

We’ve been experimenting with retroreflective surfaces for MR(mixed reality) videos and other green screen-less needs. So when the idea for a vibrant window into another reality came about, things came together pretty quickly. We had worked with the parallax effect to bring some depth to a 2d surface using a projector and a Kinect in the past, so we had some previous ideas about how it might work. In the previous demo, we used the Kinect to bind to a skeleton and provide our x,y,z coordinates to in turn move three separate layers of graphics laid out to represent a distant landscape with a background, midground, and foreground. Essentially there was a rock that you were able to look around to reveal something hidden and then your position relative to the screen would trigger a Depth of Field effect as you got closer or further away.

This setup required quite a bit of setup. Including the Kinect, we were running a Quartz Composer app to handle the skeletal binding, the animation of the layers, the focus effect, etc. With this new idea and setup, it needed to be much lighter. Going down the web based route made it much simpler and way more shareable(replicable as well).

![Apple TV Aerial Screen Saver](https://robertcedwards.com/images/1*tKvjOZQgF7OFpKBv7BeeSQ.jpeg)*Apple TV Aerial Screen Saver*

In 2015 Apple updated its Apple TV with beautiful screen savers and the internet was [all](https://github.com/JohnCoates/Aerial) [a](http://benjaminmayo.co.uk/watch-all-the-apple-tv-aerial-video-screensavers) [buzz](http://osxdaily.com/2015/10/31/aerial-apple-tv-screen-savers-for-mac-os-x/) about it. Since it was exactly the kind of content I was looking for, I proceeded to build a prototype using it was the living video source paired with [Parallax.js ](http://matthew.wagerfield.com/parallax/)(and more specifically [this fork](http://topheman.github.io/parallax/) with head tracking support!).

![Parallax.js, now with head tracking thanks to [Tophe](undefined)](https://robertcedwards.com/images/1*bYDwV2h3nW9dSKQY_2FrUQ.png)*Parallax.js, now with head tracking thanks to [Tophe](undefined)*

Their software is web based so it makes for an easy deployment and customization, perfect 💯 !

One of the earlier problems that I ran into was the fact that the library that handles the head tracking was optimized for a seated experience in front of a laptop 💻, which is awesome, but when, paired with a narrow angle of view, made for a small scale experience and we’re looking for something for a standing experience, something more like [🌴](http://emojipedia.org/palm-tree/) or 🌌.

![Logitech C920, Olloclip, and adapters](https://robertcedwards.com/images/1*4CE5OHVmSHP0aQVVDbPQ_Q.jpeg)*Logitech C920, Olloclip, and adapters*

First thoughts were to change out our camera and lensing. We have a few Logitech C920 cameras lying around that we’re using for MR stuff as well so they seemed like a good candidate. Along with a few salvaged lenses from an old Olloclip, we set off to Sketchup to make some adapters.

![[http://www.thingiverse.com/thing:1723714](http://www.thingiverse.com/thing:1723714)](images/1*T70uOqGrqYXhrh_S2UC4mw.png)*[http://www.thingiverse.com/thing:1723714](http://www.thingiverse.com/thing:1723714)*

Ended up with a [few different options](http://www.thingiverse.com/thing:1723714) for the camera and for the Macbook Pro. We had two different lenses but with similar body diameters at the base. There were a few designs created to cover the different needs such as the Logitech webcam, a Macbook Pro, and a Macbook Air, all of which we used for testing.

![Stock MacbookPro camera vs. Olloclip wide angle lens with Parallax.js w/head tracking](images/1*q5ca9Xe0nDGo8Jf8qpTc6w.jpeg)*Stock MacbookPro camera vs. Olloclip wide angle lens with Parallax.js w/head tracking*

They definitely give a much wider angle of usable space without messing with the tracking too much.

Here you can see the difference between the results of the stock Macbook Pro camera versus the wide-angle lens. The difference in the amount of space that is usable went from 60cm(~2') to 160cm (~5'3"), so a fairly sizable amount. This enabled the window to be usable from a much further distance away, which is what we were trying to accomplish.

So combining our lenses along with the Parallax.js library, the Apple Aerial videos, and a projector we were able to achieve quite a spectacular result considering the costs and efforts required.

![Github Project for all to see and contribute!](https://robertcedwards.com/images/1*TZeCTDKXzP4ICKnKfAlkaQ.png)*Github Project for all to see and contribute!*

I’ve published up the [demo](https://robertcedwards.github.io/living-window/) and [code](https://github.com/robertcedwards/living-window) up on Github, so check it out and make some windows! I plan on adding more videos, content and a dropdown of some sort.

---
layout: post
title:  "Unity-VR-&-Arduino.js"
date:   2015-09-05
---
We've been looking into solutions in order to get custom inputs and outputs working inside of Unity.
There have been some early success using C# and javascript to Native with:
```
using System.IO.Ports;

```
There are also plugins in the Asset Store
https://www.assetstore.unity3d.com/en/#!/search/arduino

Unidunio is one of the more mature projects but it seems to not be upadted for Unity 5 quite yet.
https://www.assetstore.unity3d.com/en/#!/content/6804

With Unity 5.2 our examples and test scene that included various ways of interacting with the Arduino all started to fail.
Without recourse we needed to pivot in order to continue on and find a more stable solution.

OSC is a 

https://en.wikipedia.org/wiki/Open_Sound_Control
http://opensoundcontrol.org/introduction-osc

For our purposes we'll need to use a Processing implenlation so we've used it before and integrates well with the Arduino using Firmata.

One of the early articles:
http://www.mono-project.com/archived/howtosystemioports/

{% gist 5555251 gist.md %}


http://r3dstar.co.uk/?p=211

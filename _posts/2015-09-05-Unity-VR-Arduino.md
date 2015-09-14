---
layout: post
title:  "Unity-VR-&-Arduino.js"
date:   2015-09-05
---
We've been looking into solutions in order to get custom inputs and outputs working inside of Unity.
There have been some early success using C# and javascript to Native with:

```C#
using System.IO.Ports;
```

There are also plugins in the Asset Store
https://www.assetstore.unity3d.com/en/#!/search/arduino

Unidunio is one of the more mature projects but it seems to not be upadted for Unity 5 quite yet.
https://www.assetstore.unity3d.com/en/#!/content/6804

```C#
public static SerialPort sp = new SerialPort("COM9", 9600);
```

One of the early articles:
http://www.mono-project.com/archived/howtosystemioports/

With Unity 5.2 our examples and test scene that included various ways of interacting with the Arduino all started to fail.
Without recourse we needed to pivot in order to continue on and find a more stable solution.

OSC is a 

https://en.wikipedia.org/wiki/Open_Sound_Control
http://opensoundcontrol.org/introduction-osc

For our purposes we'll need to use a Processing implenlation so we've used it before and integrates well with the Arduino using Firmata.
Here is a scratch built Processing + Arduino solution written in C#:
http://www.sundh.com/blog/2012/05/unity-processing-arduino/

![Sundh example in processing](https://i.imgflip.com/r1kxr.gif)

This is a great way to understand how OSC, Processing, and Arduino are interacting with a Sender and Receiver script running to serve the data up to Unity via OSC.
We're looking for a more advanced solution that allows us to visually management the scripts controlling the interactions bewteen the various elements with Unity. 



There are a few projects in the Asset Store:
https://www.assetstore.unity3d.com/en/#!/search/osc


UniOSC is the one we'll be focusing on.
https://www.assetstore.unity3d.com/en/#!/content/17658



{% gist 5555251 gist.md %}


http://r3dstar.co.uk/?p=211

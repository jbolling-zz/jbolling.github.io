---
layout: post
title:  "Dynamic Baseline Binocular Stereo using Multirotor UAVs"
date:   2017-09-05 10:12:00 -0800
categories: projects
excerpt: "My thesis at Princeton University used multirotor drones to take stereo video from two different airborne perspectives. The captured video could be viewed through a VR headset to give the impression that the viewer was standing hundreds of feet tall, with eyes set far apart"
---

My thesis at Princeton University used multirotor drones to take stereo video from two different airborne perspectives. After video was captured, it was viewable through a VR headset to give the impression that the viewer was standing hundreds of feet tall, with eyes set far apart (inspired by [this XKCD comic][xkcd]). I worked with [Ankush Gola][ankush-gola] to select hardware, write control code for the UAVs, design additional vision-based sensing systems, implement the various sensor fusion filters, and post-process the captured video to give a stable viewing experience.

![alt text]({{ site.url }}/assets/thesis/Diagram.png "Two drones capturing stereo video")

You can read our full thesis [here][thesis]. No drones were harmed in the making of this thesis, though we did nearly destroy one LiPo battery.

![alt text]({{ site.url }}/assets/thesis/stereoglyph.jpg "post-processed still frame from a test flight")

[ankush-gola]: http://ankushgola.com/
[xkcd]:        https://xkcd.com/941/
[thesis]:      {{ site.url }}/assets/thesis/DynamicBaselineStereo.pdf

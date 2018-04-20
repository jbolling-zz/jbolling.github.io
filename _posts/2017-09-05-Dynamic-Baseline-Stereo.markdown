---
layout: post
title:  "Capturing Dynamic Baseline Stereo Video using Multirotor UAVs"
date:   2017-09-05 10:12:00 -0800
categories: projects
excerpt: "My thesis at Princeton University used multirotor drones to take stereo video from two different airborne perspectives. The captured video could be viewed through a VR headset to give the impression that the viewer was standing hundreds of feet tall, with eyes set far apart."
---

My thesis at Princeton University used multirotor drones to take stereo video from two different airborne perspectives. After video was captured, it was viewable through a VR headset to give the impression that the viewer was standing hundreds of feet tall, with eyes set far apart (inspired by [this XKCD comic][xkcd]). I worked with [Ankush Gola][ankush-gola] to select hardware, write control code for the UAVs, design additional vision-based sensing systems, implement the various sensor fusion filters, and post-process the captured video to give a stable viewing experience.

![alt text]({{ site.url }}/assets/thesis/Diagram.png "Two drones capturing stereo video")

In addition to the software design, we built a laser-based tracking gimbal. It used the [UT390B laser distance meter](http://blog.qartis.com/arduino-laser-distance-meter/) and a webcam to track a pink target ball. The webcam provided 2-dimensional data and the laser captured depth measurements to form a sort of quasi-lidar for single-target tracking. We never got the full system to operate fast enough to use in flight scenarios, but we did use a simplified version (without the laser) to augment the flight telemetry from the drones' existing sensor suites. We wrote an offline sensor fusion module using the Unscented Kalman Filter to integrate the webcam data with the drone IMU measurements. 

![alt text]({{ site.url }}/assets/thesis/gimbal.png "laser-based tracking gimbal")

You can read our full thesis [here][thesis]. No drones were harmed in the making of this thesis, though we did nearly destroy one LiPo battery.

![alt text]({{ site.url }}/assets/thesis/stereoglyph.jpg "post-processed still frame from a test flight")

[ankush-gola]: http://ankushgola.com/
[xkcd]:        https://xkcd.com/941/
[thesis]:      {{ site.url }}/assets/thesis/DynamicBaselineStereo.pdf

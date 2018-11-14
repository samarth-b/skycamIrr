---
layout: post
title:  "Solar panel monitoring with drones"
date:   2016-12-28 23:34:56 +0530
categories: research update
tags: [deeplearning, weather, solar]
image:
  feature: images-hq/drone.jpg
  teaser: images-hq/drone.jpg
  credit: free
  creditlink: ""
---

Images or videos of a solar farm obtained from drone imaging can be used for
health monitoring of panels, dust and/or occlusion detection thermal hotspots (with fine grain imaging), and production anomalies

These are the potential payoffs that have led companies like First Solar and SolarCity to start testing unmanned aircraft systems (UAS) as a business tool over the past few years, according to a [report](http://www.greentechmedia.com/articles/read/flying-robots-the-future-solar-data-farmers-of-america) from the Electric Power Research Institute (EPRI).

> Errors such as micro-cracks, snail trails, potential-induced degradation, and ribbon solder bond failures, among others, can be identified by hovering UAVs, not to mention easy-to-spot problems like dirt and leaves


## Detecting regions of interest in solar farms

![ROI]({{ site.github.url }}/images/output-DJI2.JPG)

Visible spectrum drone images (RGB) can be used for segmenting regions
of interest where the color corresponds to confidence.

## Occlusion detection with high resolution imaging

![Occlusion detect]({{ site.github.url }}/images/output-chalk.jpg)

The region of interest is identified and scaled. Color separation is used to identify the properties of the occluding material. An collusion estimation is made at cell level, and correlated with the material properties to obtain estimated decrease in performance

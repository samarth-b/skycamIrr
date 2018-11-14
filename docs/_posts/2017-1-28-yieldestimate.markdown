---
layout: post
title:  "Yield Estimate: How'd you like them Apples?"
date:   2017-1-28 23:34:56 +0530
categories: research update
tags: [deeplearning, agriculture]
image:
  feature: images-hq/grapes.jpg
  teaser: images-hq/grapes.jpg
  credit: free
  creditlink: ""
---

Estimating yield in fruit plantation is a tiresome manual exercise which is also highly error prone. A farmer typically samples fruits randomly across the farm, and measures fruit parameters like radius, color etc. Then a formula is used to extrapolate these finding to the entire farm.

Our surface anomaly methods can use used to segment the color and region of the fruit objects from local mobile phone images or ground/low-flying drone images from the entire farm. A yield estimation approach can be over layed on the segmented region to provide fine-grain estimation of fruit quality and yield.   


## Detecting grape bunches from studio images

* Vision based approach to identify grape bunch in plantation

* Approximate berry count and radius of the grape can also be computed from which yield can be estimated

* Quality of fruit can also be estimated with a suitable color palette

![ROI]({{ site.github.url }}/images/figure_41.png)

Color contrast stretching is used for segmenting regions
of interest where the color corresponds to confidence.

![ROI]({{ site.github.url }}/images/figure_42.png)


## Detecting grape bunches from mobile phones

* We find that our approach performs well on high resolution images obtained from mobile phones despite harsher imaging conditions

![ROI]({{ site.github.url }}/images/figure_1.png)

![ROI]({{ site.github.url }}/images/figure_2.png)


## Detecting quality of palm oil (work in progress)

* We are currently working on estimating palm oil from images based on color

* Stay tuned for updates!!

![ROI]({{ site.github.url }}/images/palmoil.jpg)

---
layout: post
title:  "DeepSky: Just need to look up to tell the weather!"
date:   2017-03-28 23:34:56 +0530
categories: research update
tags: [deeplearning, weather, solar]
image:
  feature: images-hq/cloud.jpg
  teaser: images-hq/cloud.jpg
  credit: free
  creditlink: ""
---

Ahead-of-time forecasting of incident solar-irradiance on a panel is indicative of energy yield and is essential for efficient grid distribution and planning. Typical approaches are based on meteorological physics models whose parameters are tuned by coarse-grained radiometric tiles sensed from geo-satellites.

This research presents a deep learning approach to observe and estimate short-term weather effects from sky-videos obtained with upward facing wide-lensed cameras and directly forecast solar irradiance. Our approach utilizes dilating convolution filters to learn a full-sky representation at varying scales via joint-training aided by auxiliary weather parameters that are sensed simultaneously. Multiple LSTMs with soft attention then leverage the full-sky representation to forecast the total surface irradiance by estimating flow, density and illuminance of clouds. We showcase results on two datasets obtained from weather stations in North America that captured sky-videos with relatively inexpensive optical hardware. They contain over a million images that span for one and 12 years respectively. Our deep learning approach significantly reduces the mean absolute percentage error for both nowcasting and forecasting.

![conceptDiagram]({{ site.github.url }}/images/conceptDiagram.png)


## DeepSky performance analysis and visualization on sample videos

Here are two sample videos in the month of April from each of the two datasets obtained from two different locations in the United States. We chose these videos, as they illustrate the challenges of irradiance forecasting (torrential rainy days in early summer).

Corresponding to each frame, the interpolated mean of the [hypercolomns][hypercol-ref] is plotted that is indicative of the *focus* of convolution filters. Further, the measured irradiance is plotted along with the nowcast prediction and ahead of time forecast (+1, +2, +3, & +4) hours. Specific observations are made on each video in the caption text.

### Golden, Colorado

![original video]({{ site.github.url }}/images/Gif_Colorado.gif)
![visualization]({{ site.github.url }}/images/videograph_Colorado.gif)

The Colorado video setup (TSI) consists of a sun tracker to protect the lens and equipment from direct exposure to the sun. Hence, the autofocus allows the camera to capture the clouds more clearly. We pick a challenging video from the dataset with large intra-day variations in solar irradiance. Notice, that the error in nowcasting is higher, when the sun tracker miss-fires.

#### Results

![visualization]({{ site.github.url }}/images/skycam-iccv17.jpg)


For details please have a look at our paper titled:

DeepSky: A dilating convLSTMs approach to estimate flow in sky-videos for solar-irradiance forecasting [[pdf]({{ site.github.url }}/images/skycam_v1_CR.pdf)]

[hypercol-ref]: https://arxiv.org/abs/1411.5752

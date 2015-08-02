---
layout: page
title: "Intensity"
category: analysis
date: 2015-07-25 22:46:33
order: 2
tags:
- Analysis
---

###Concepts

All intensity analysis is performed by summing the intensity values of pixels within a number of 3D regions-of-interest (ROI). Further analysis is then derived by performing algebra between these ROIs.

By constructing each ROI to have the same number of pixels. We can make meaningful divisions and subtractions between their sums.

####Spine ROI

A polygon surrounding a spine. Starts as a retangle and then union with the backbone ROI is subtracted. Two parameters specify spine ROI: width and extend head.

####Background ROI

Same size as spine ROI, positioned near spine to minimize background intensity.

####Backbone ROI

In the region of the spine connection

###Parameters

 - **Spine width (um).** Width of spine ROI centered on the spine line.
 - **Extend head (um).** Distance to extend the spine ROI beyond the end of the spine line.
 - **+/- Planes.** The sum of each spine, backbone, and background ROI is expanded in the Z-dimension before the sum of pixels is taken.
 
###Names of analysis outputs

The following table matches what is displayed in the Map Manager Stack Plot [plot panel][1]. [TODO: keep this updated in a google spreadhseet and display .pdf here]

	
[1]: /mapmanager/plot-panel/

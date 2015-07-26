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

All intensity analysis is performed by summing the intensity values of pixels within a number of 3D regions-of-interest (ROI). Further analysis can then be derived by performing simple algebra between these ROIs.

####Spine ROI

A polygon surrounding a spine. Starts as a retangle and then union with spines backbone ROI is subtracted. Two parameters specify spine ROI: width and head extension.

####Background ROI

Same size as spine ROI, positioned near spine to minimize background intensity.

####Backbone ROI

In the region of the spine connection
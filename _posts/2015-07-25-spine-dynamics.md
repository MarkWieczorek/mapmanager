---
layout: page
title: "Spine Dynamics"
category: analysis
date: 2015-07-25 22:46:33
order: 1
tags:
- Analysis
---

### Density Report

A density report is used for individual [stacks][1]. It will calculate the length of each dendritic segment and the density of spines.

Generate a density report for each segment in a stack

 - In a [stack window][1], keyboard 'o' for **o**utput report.
 - In the [Stack Browser][3], select a stack in the list, keyboard 'o' for **o**utput report.
 
```
numSpines		Total number of spines = goodSpines + badSpines
goodSpines		Number of good spines.
badSpines		Number of bad spines.
totalLen		Total segment length (um)
goodLen			Segment length (um) from most distal good spines.
totalDen		Total density of all spines = numSpines / totalLen
goodDen			Density of good spines = goodSpines / goodLen
totalLen3d
goodLen3d
totalDen3d
goodDen3d
```

### Dynamics Report

 
A dynamics report is used for a [map][2]. For each session in a map, it will calculate the length of each segment (um), the density of spines, the number of added spines, the number of subtracted spines, etc., etc.

Generate a spine dynamics report for each segment in a map.
 
 - In any [map plot][2], right-click and select 'Dynamics Report'. If the map plot is displaying 'All Segment', a table for each segment will be opened. Otherwise, one table for the current 'Map Segment ID' will be opened.
 
 
 ```
 numSpines		Total number of spines, goodSpines + badSpines.
 goodSpines		Total number of good spines
 badSpines		Total number of bad spines
 totalLen		Total segment length (um)
 goodLen		Segment length between most distal good spines.
 
 totalDen		Total density = numSpines / totalLen
 goodDen		Density of good spines = goodSpines / goodLen
 
 nAdd			Number of added spines.
 nSub			Number of subtracted spines (at the current session)
 nSub2			Number of subtracted spines (from the previous session)
 tor			Turn-over-ratio = 
 
 pAdd			Percent added = nAdd / goodSpines from previous session * 100
 pSub			Percent subtracted = 
 dAdd			Density added =
 dSub			Density subtracted = 
 
 np				New persistent = 
 nt				New transient = 
 lp				Lost persistent = 
 lt				Lost transient = 
```

### Concepts

#### Stack
Each segment within a stack has a number of spines and a total traced dendritic length. From this we can calculate spine density.

- Number of spines
- Dendrite length
- Spine density : number of spines / dendrite length

#### Map
From one session to the next, the number of added and subtracted spines are counted. From this, the percent and density changes are calculated.

- # Added 
- # Subtracted
- % Added : # added / (number of spines in pervious session) * 100
- % Subtracted :
- Turn-over-ratio : A measure of total dynamics (both addition and subtraction)
- Density Added : 
- Density Subtracted : 

#### Map Lifetime
Observed 

- observed sessions
- observed seconds
- observed days
- observed hours

Lifetime

- sessions
- seconds
- days
- hours

Age

- sessions
- seconds
- days
- hours

#### Svoboda style persistent and transient

Threshold time can be specified as: sessions, seconds, days, or hours.

- New Persistent : New spine that persists for > threshold time
- New Transient :
- Lost Persistent :
- Lost Transient :
- Always Present : Spines present in all sessions

[1]: stack
[2]: map-plot
[3]: stack-browser

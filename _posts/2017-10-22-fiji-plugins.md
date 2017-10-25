---
layout: page
title: "Fiji plugins"
category: post
date: 2017-10-22 00:00:01
order: 2
tags:
- Fiji
---

Map Manager uses a number of custom Fiji plugins to fit segment tracing and convert raw data into a format that can be imported into Map MAnager.

### Tracing segments

This is done seemlesly and only requires an installed Fiji program to be identified in [hard drive paths][2].

### Converting raw data to single channel .tif files

Map Manager can import 3D .tif image stack with 1, 2, or 3 color channels.

Here are the rules:

 - Map Manager **will** open single color channel 3D .tif files.
 - Map Manager will <span style="color:red">not</span> open 3D volumes that have interleaved color channels.
 - Map Manager will <span style="color:red">not</span> open 3D volumes saved as individual .tif files

Fiji plugins are provided to make these conversions fast and easy.

In all these plugins, great care was taken to extract the voxel size, date, and time. This is critical for rapid workflows to always score annotations in um and to make time-series in the correct order.

<p class="important"><B>Important:</B> When stacks are first imported into the stack browser, please verify the voxel size, date, and time are set correctly.
</p>

#### Zeis LSM/CZI

bFolder2MapManager

#### Prairie View

bAlignBatch

#### ScanImage (Vidreo)

bAlignBatch  

[1]: https://github.com/cudmore/bob-fiji-plugins

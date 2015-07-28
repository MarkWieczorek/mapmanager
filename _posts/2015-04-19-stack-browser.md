---
layout: page
title: "Stack Browser"
category: imagingcore
date: 2015-04-19 22:46:33
order: 1
tags:
- Imaging core
---

<IMG class="img-float-left" SRC="../images/mm3/mm3-stack-browser.png" WIDTH="800">

<div class="print-page-break"></div>

 
The stack browser provides an interface to load and browse directories of .tif [stacks][3].

The original documentation is [here][2]

In general, the list on the left represents folders of loaded stacks. Select a folder of stacks on the left and the list on the right will show the individual stacks within that folder.

Double click on a stack in the list on the right and it will open a [stack][3] window to view the actual stack.

###Loading stacks

The simplest way to load a stack is to drag and drop a .tif file onto the Igor program icon. Stacks opened in this way will appear in a special folder (in the list on the left) called 'DragAndDrop'.

**Load ScanImage Directory.** Load a folder of ScanImage .tif stack. The name of the folder will appear in the list on the left. Selecting this folder will populate the list of stacks imported. Double click on a stack (in the list on the right) to view the [stack][3].

**Load Generic Directory.** Load a folder of .tif stacks ignoring any .tif header information. This has some consequences:

 1. The stack will not have a scale. Set this with xxx
 2. If the source .tif stack are multi-channel stacks, Map Manager will blindly import them as one big stack (usually with channels interleaved from slice to slice). Please see bAlignBatch to pre-process your .tif stacks into ch1/ch2 file pairs.
 3. The stacks will not have a date. Thus, [map plots][4] with date/days/hours will not be possible.


###Browsing loaded data

Select your loaded directory on the left  and the loaded stacks will be shown on the right.

Double click a stack in the list on the right to open a [stack][3] window.


[1]: /mapmanager/stack-browser/
[2]: http://www.robertcudmore.org/maptracker/v2/stack-browser/
[3]: /mapmanager/stack/
[4]: /mapmanager/map-plot/

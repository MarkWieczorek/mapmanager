---
layout: page
title: "Making a map"
category: workflow
date: 2015-04-20 22:46:33
order: 2
tags:
- Workflow
---

<IMG class="img-float-left" SRC="images/mm3/time-series/time-series-panel.png" WIDTH="650">

<div class="print-page-break"></div>

A map is a time-series of [stacks][2]. You create a map by appending stacks from the [stack browser][1]. Once a map is made it can be saved, re-opened, annotated, and browsed using the [time-series panel][13].

The time-series panel shows a list of open maps on the left. When a map is selected (het3b in this example), a list of sessions in the map are shown on the right (in this example there are 12 sessions).

#### Open and initialize Map Manager 

 1. Open Igor Pro with MapManager.ipf
 2. Initialize Map Manager with the main menu 'MapManager - Map Manager Panel'.
 
#### 1. Pre-process your raw data so Map Manager can import it
 Map Manager will only import single channel stacks. If your stacks have two color channels, they need to be de-interleaved into two different .tif files. One .tif file for each color channel. See [bAlignBatch][14] for a Fiji plugin that does this.

#### 2. Make a new map
 1. Fill in a new map name and choose the number of channels for each stack in your map.
 2. Create a new map with '<span style="color:green">New Map</span>'.
 3. Append a stack from the [Stack Browser][1] with 'Append Stack'.
 4. Repeat # 3 for each stack.
 5. Save the map with 'Save Map' button.
 
#### <span style="color:red">Important</span>
 - When you make a map, you need to choose the 'Number Of Channels' in each stack/session. Map Manager will only allow one choice of 'Number Of Channels' per map. You cannot mix one and two channel stacks within a map.
 - Make sure the scale of each imported stack is correct. It is hard to change the scale later. You can set the scale of a stack in its stack window with 'shift+p'.
 - Make sure the sessions in your map are imported in the correct order. It is hard to change the order later.
 - As you import stacks from the [stack browser][1] there are some rules that must be followed. You will be prompted when you break these rules. In particular:
   1. The stack scale must be set. Set the scale of a [stack][2] in a stack window with shift+p.
   2. The stack must be loaded. Double click the stack in the [stack browser][1] to load a stack.
   3. When importing 2 channel stacks, both channels must be loaded and you must select the first channel (ending in _ch1) in the stack browser.
 - New maps are saved to a default hard-drive folder. The default folder can be specified the [Hard Drive Paths Panel][10]. Right-click on a map name and select 'Show On HDD' to see the hard-drive folder where the map is saved.
   - On Windows, the default folder is 'My Documents'.
   - On OSX, the default folder is 'Documents'.

#### Congratulations, you just made a Map Manager map. The rest of this tutorial covers specifying and fitting segment backbone lines, adding spines, and connecting spines across timepoints.

#### 3. Create a line segment in each session/stack of the map and fit its backbone in Fiji
Line segments are first specified with control points and then fit using a custom FIJI plugin. Before fitting a line in FIJI, you need to install  the [Bob_Neurite_Tracer_v3][14] plugin in FIJI and you need to specify the path to your FIJI application in the [Hard Drive Paths Panel][10].

See [Fitting Segment In Fiji][15] for help on FIJI versions, installing the plugin and specifying the FIJI application path in Map Manager.

 1. Double-click the first session in your map (in the time-series panel) to open a [stack][2] window.
 2. Create a line segment by follow the instruction in [annotating a stack][4].
    - Turn on Segment Editing with the checkbox next to 'Line Segments'.
    - Click the '+' button to create a new (empty) segment.
    - Create Control Points along a segment with shift+click. Remember, all points are in 3D, make sure the points are in the correct imaging plane.
    - You can delete control points with the 'delete' key.
    - You can move control points with either the 'm' key or right-click menu 'Move'.
    - Once control points are made, fit the backbone line in Fiji. Right-click on your segment in the list and select 'Make from control points - Fiji'.
 3. Repeat steps # 1 and # 2 for each session in your map. Making the same line segment in each session. As you make control points, be sure they are in the same direction along the segment for each session. <del>For some help with the ordering of your control points, open the 'stack db options' panel and turn 'Control Point Help' 'On'.</del>
 4. Set a pivot point in each line segment. Do this by clicking a point in the segment, right-click and select the 'Set As Segment Pivot' menu. The pivot point should refer to the same region of the segment across all session. A good strategy is to choose a region of the segment near an obvious spine that is present in all sessions. Another strategy is to choose a pivot point where some other segment (dendrite) crosses near your segment as these tend to remain stable across time. Try and put the pivot point near the center of the segment, do not place it at either end. The pivot point is used to calculate a line distance along the segment (in um) which in turn will be used to auto-guess connections between spines across sessions.
 
<p class="tip"><B>Tip.</B> When specifying control points and setting segment pivots, you can open multiple stack windows at the same time. Just double-click on each session in the time-series panel. This way, you can see the line segments you are making in each session of your map.</p>


#### 4. Connect your line segments together
 1. Close all stack windows using the <span style="color:blue">Close Windows</span> button in the time-series panel.
 2. Open a new stack run by right-clicking a session in your map and selecting the 'Plot Run +- All' menu.
 3. Turn on the 'Line Segments' checkbox in the left control bar of a stack window. Open the left control bar with keyboard '['.
 4. Sequentialy connect your line segment from one timepoint to the next
   - Select the source timepoint segment (for example, timepoint 1). Make sure you select a point on the segment backbone line.
   - Select the destination timepoint segment (for example, timepoint 2). Again, make sure you select a point on the segment backbone line.
   - In the destination timepoint window (e.g. timepoint 2), press keyboard 'p' for Persistent (or use right-click menu).

<p class="tip"><B>Tip.</B> You can see how your segments are connected by plotting a 'Segment Map' from the time-series panel. In the segment map window, right-click a segent and select 'Plot Run' to plot a run of segments.</p>
   
#### 5. Mark spines in each timepoint
 1. Make sure 'Edit Segments' is off.
 2. Open a single timepoint by double clicking a session in the list.
 3. Follow [annotating a stack][4] to mark spines along your new segment.
 
<p class="tip"><B>Tip.</B> As you are working, keep your eye on the Igor command window. Each action you perform in Map Manager should report a few lines of text here. If this starts to spit out 1000's of lines there is probably a problem.</p>
   

#### 6. Connecting stack db objects from one timepoint to the next

You have two choices here.

#### 6.1 Use the [Find Points Panel][16] to connect objects

Use the Find Points Panel to browse spines in two timepoints. Find Points will also guess for the best connections and allow you to set them manually.

#### 6.2. Auto connect all objects using the [map plot][12]
 - Open an 'Object Map' from the time-series panel.
 - In the spine map, select a spine in the first timepoint, right click and select 'Connect Objects To Next'. This will make automatic connections of all spines from the first session to the next session.
 - Repeat this process for each pairwise session in your stack. You can also right-click and select 'Connect All Objects' to connect spines/objects through the entire map.
 - When working on spines, spines are connected if they are within a minimum distance of each other on their respective segment line. See 'Connect spines within this distance (um)' in the [stack db options panel][7] to set this option.
 
#### 7. Check the auto spine connections and edit as necessary

This is the core of Map Manager and you will spend most of your time doing this. You need to verify the auto connections of each spine and you need to do this between **each** timepoint in your map. If your map has 4 timepoints, you need to verify the auto spine connections between timepoint 1-2, timepoint 2-3, and timepoint 3-4.

 - Open a [run plot][11] of three sequential timepoints by right-clicking a spine in the spine map and selecting 'plot run +- 1'.
 - In the run plot windows, select a spine in the middle timepoint with ctrl+click. This will bring up the spine and its associated connections in all windows of the spine run. If there is no spine in a given timepoint, the image will be snapped to where the spine 'would-be'.
 - From the middle timepoint spine selection, go to the next spine along the segment using keyboard ctrl+right. Go to the previous spine along the segment using keyboard ctrol+left.
 - Correct any errors in the spine dynamics using keyboard 'a' for addition, 's' for subtraction, and 'p' for persistence. See [run plot][11] for details.
 
#### 8. Review your work by using search to query all additions and subtractions

 - Open the [search panel][5] from the time-series panel with the 'Search' button.
 - In the search panel, make sure 'map' is slected and search for all spine additions with the 'Additions' button.
 - All added spines will appear as a list in the search results.
 - Right-click on a spine and select 'plot run +- 1' to bring up a spine run. [HERE I NEED TO CHANGE THE INTERFACE. I NEED A QUICKER WAY OF BRINING UP A SPINE RUN!!!]
 
**THIS IS WHERE I AM ENDING FOR NOW ON July 29, 2015 ... THIS NEEDS TO BE EXPANDED**
 
<BR>
<BR>
<BR>
<BR>
<BR>

## DO NOT READ BELOW HERE !!!!

### [ADVANCED]: Importing a bSpine map

<IMG class="img-float-left" SRC="images/mm3/mm3-import-bspine.png" WIDTH="275">

Importing bSpine maps is tricky. The problem is if your original maps for one time-series (_d1, _d2, etc.) have different sessions. For example, _d1 has sessions from dates 1,2,3 but _d2 has sessions from dates 1,2,6,12 there <span style="color:red">will be an error</span>.

Thus, there are two cases:

 1. Your maps _d1, _d2 etc. all have the same exact sessions
 	This is simple, use 'Batch import bSpine map'. You will be prompted for the first map (you should select _d1). Once this is done, you need to hit all the buttons in '(2) fix' to complete the import and then 'save map' in the time-series panel.
 	
 2. Your maps _d1, _d2 etc. have different sessions.
	<span style="color:red">This DOES NOT WORK.</span>


 **This documentation is not done**
 
 #### Import group
 
 - **Import One bSpine map.** ... not done
 
 - **Append One bSpine map.** ... not done
 
 #### Fix group
 
  - ** I am sick of writing documentation. Please see Bob for instructions. **
 


[1]: stack-browser
[2]: stack
[3]: user-files
[4]: annotating-a-stack
[5]: search-panel
[6]: plot-panel
[7]: stackdb-options-panel
[8]: contrast-panel
[9]: stack-browser
[10]: hdd-paths
[11]: run-plot
[12]: map-plot
[13]: time-series-panel
[14]: https://github.com/cudmore/bob-fiji-plugins
[15]: fitting-segments-in-fiji
[16]: find-points-panel

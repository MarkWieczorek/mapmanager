---
layout: page
title: "Main panel"
category: interface
date: 2015-04-20 22:46:33
order: 1
tags:
- Interface
---


The main map manager panel provides an interface to load, save and browse Map Manager maps. Open the main map manager panel using the menu 'MapManager - Map Manager Panel'

Expand the main map manager panel to access the [map making][13] interface. Use the disclosure triangle/+ at the top of the window near the help/? button.

Once a map is created and saved, the main map manager panel can be minimized again with the disclosure triangle.

The <span style="color:blue">blue</span> buttons operate on the selected map.
  
<IMG class="img-float-center" SRC="images/mm3/mm3-main-panel-big.png" WIDTH="700">

<!--- <IMG class="img-float-left" SRC="images/mm3/mm3-main-panel-small.png" WIDTH="200"> -->

  <B>Load Map.</B> Load a map from the hard-drive. 
  
  <B>Save Map.</B> Save the selected map.
  
  <B>?.</B> Open map manager documentation in your default web browser.
  
###Plot
  
<B>Object Map.</B> Open a [map plot][12] showing the position of spines along dendritic segments vs. session.

<B>Segment Map.</B>  Open a [map plot][12] showing the segments within each session and the connectivity of segments across sessions.

<B>X-Axis.</B> Choose different X-Axis for Object and Segment map plots. Available X-Axis are:

 - Sessions 
 - Datetime
 - Days
 - Hours
 - Zero Sessions
 - Zero Days
 - Zero Hours
    
Datetime, Days and Hours require stacks to have a date/time specified. Specify a custom date/time by turning on 'Edit Date/Time' in the Map Making Tab. The X-Axis options starting with 'Zero' use a session in the map as a zero timepoint. Specify this with 'Zero Session' in the expanded map manager panel. The zero session for a map will have a '*' in its session list. Zero Session is also used by the [Plot Panel][6].
    
###Panels

Each of these buttons will open a different Map Manager panel.

<B>Search.</B> Open the [search panel][5].

<B>Plot.</B> Open the [plot panel][6].

<B>Process.</B> Open the [process panel][8] to set image contrast.

<B>Options.</B> Open the [options panel][7].

<B>Map DB.</B> NOT DOCUMENTED YET..

<B>Layout.</B> Open the [layout/scale panel][14].

<B>Stack Browser.</B> Open the [stack browser panel][9].

###Miscellaneous

<B>Unload stacks.</B> Unload all stacks in the selected map (from Igor memory).

<B>Close Windows.</B> Close all windows associated with the selected map.

<B>Username.</B> This can be specified in the [map manager options panel][7].

<B>Edit Segments.</B> When checked, all editing in a [run plot][11] will edit the persistence of segments (addition, subtraction, and persistent).


###Right-click on a map name in the list for a contextual menu.

<IMG class="img-float-left" SRC="images/mm3/mm3-main-panel-map-right-click.png" WIDTH="100">

<B>Show on HDD.</B> Shows the hard-drive folder where the map is saved.

<B>Map stats.</B> Not implemented

<B>Edit map NV.</B> <span style="color:red">ADVANCED USERS</span>, this shows a map as a text table.

<B>Close map.</B> Close a map, removing it and all associated analysis from Igor memory.

###Plot Tab

###Map Making Tab

###Intensity Tab

###Utility Tab

###Report Tab

<div class="print-page-break"></div>


[1]: /mapmanager/stack-browser/
[2]: /mapmanager/stack/
[3]: /mapmanager/user-files/
[4]: /mapmanager/annotating-a-stack/
[5]: /mapmanager/search-panel/
[6]: /mapmanager/plot-panel/
[7]: /mapmanager/stackdb-options-panel/
[8]: /mapmanager/process-panel/
[9]: /mapmanager/stack-browser/
[10]: /mapmanager/hdd-paths/
[11]: /mapmanager/run-plot/
[12]: /mapmanager/map-plot/
[13]: /mapmanager/making-a-map/
[14]: /mapmanager/scale-panel/

<div class="print-page-break"></div>

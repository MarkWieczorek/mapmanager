---
layout: page
title: "Main panel"
category: interface
date: 2015-04-20 22:46:33
order: 1
tags:
- Interface
---


The main panel provides an interface to load, save and browse map manager maps. Open the main panel using the menu 'mm3 -> Map Manager 3'

Expand the main map maker panel to access the [map making][13] interface.

Once a map is created and saved, the map maker 3 panel can be minimized with the disclosure triangle (at the top of the window near the help/? button).

The <span style="color:blue">blue</span> buttons operate on the selected map.
  
<IMG class="img-float-left" SRC="../images/mm3/mm3-main-panel-small.png" WIDTH="200">

  <B>Load Map.</B> Load a map from the hard-drive. 
  
  <B>Save Map.</B> Save the selected map.
  
  <B>?.</B> Open map manager 3 documentation in your default web browser.
  
####Plot Group
  
<B>Spine Map.</B> Open a [map plot][12] showing the position of spines along dendritic segments vs. session.

<B>Segment Map.</B>  Open a [map plot][12] showing the segments within each session and the connectivity of segments across sessions.

<B>X-Axis.</B> Choose different X-Axis for Spine and Segment map plots. Available X-Axis are:

 - Sessions 
 - Datetime
 - Days
 - Hours
 - Zero Sessions
 - Zero Days
 - Zero Hours
    
Date, Days and Hours require your imported stack to have a date specified. The X-Axis options starting with 'Zero' use a session in the map as a zero timepoint. Specify this with 'Zero Session' and 'Rebuild' in the expanded map manager 3 panel.
    
####Panel Group

Each of these buttons will open a different Map Manager panel.

<B>Search.</B> Open the [search panel][5].

<B>Plot.</B> Open the [plot panel][6].

<B>Buttons.</B> Open a button toolbar with other useful buttons.

<B>Options.</B> Open the [options panel][7].

<B>Utilities.</B> Only for advanced users. Do not use.

<B>Process.</B> Open the [process panel][8] to set image contrast.

<B>Stack Browser.</B> Open the [stack browser panel][9].

<B>HDD Paths.</B> Open a panel to [edit hard-drive paths][10] like the default folder to save and load maps.

####Miscellaneous

<B>Connect Segments.</B> When checked, all editing in a [run plot][11] will edit the persistence of segments (addition, subtraction, and persistent).

<B>Unload stacks.</B> Unload all stacks in the selected map (from Igor memory).

<B>Close Windows.</B> Close all windows associated with the selected map.

Right-click on a map name in the list for a contextual menu.

<IMG class="img-float-left" SRC="../images/mm3/mm3-main-panel-map-right-click.png" WIDTH="100">

<B>Show on HDD.</B> Shows the hard-drive folder where the map is saved.

<B>Map stats.</B> Not implemented

<B>Edit map NV.</B> <span style="color:red">ADVANCED USERS</span>, this shows a map as a text table.

<B>Close map.</B> Close a map, removing it and all associated analysis from Igor memory.


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

<div class="print-page-break"></div>

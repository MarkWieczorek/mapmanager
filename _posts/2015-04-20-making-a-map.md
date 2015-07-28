---
layout: page
title: "Making a map"
category: workflow
date: 2015-04-20 22:46:33
order: 1
tags:
- Workflow
---

<IMG class="img-float-left" SRC="../images/mm3/mm3-main-panel.png" WIDTH="600">

<div class="print-page-break"></div>

A map is a sequence of [stacks][2]. You create a map by appending stacks from the [stack browser][1]. Once a map is made it can be opened, saved, annotated, and browsed using the main [map maker panel][13].

In the Map Manager 3 window, the list of open maps is on the left. When a map is selected, a list of sessions within the map is shown on the right.

Double-click a session to open a [stack][2] window and begin adding [3D annotations][4].

####Making a new map
 1. Create a new map with '<span style="color:green">New Map</span>'.
 2. Append a stack from the [Stack Browser][1] with 'Append Stack'.
 3. Repeat #2 for each stack.
 4. Save the map with 'Save Map' button.
 
####<span style="color:red">Important</span>
 - When you make a map, you need to choose the 'number of channels' in each stack/session. Map Manager will only allow one choice of 'number of channels' per map. You cannot mix one and two channel stacks within a map.
 - Make sure the sessions in your map are imported in the correct order. It is hard to change the order later.
 - Make sure the scale of each imported stack is correct. It is hard to change the scale later.
 - New maps are saved to a default hard-drive folder. The default folder can be specified in a [user file][3] file. Right-click on a map name and select 'Show On HDD' to see the hard-drive folder where the map is saved.
   - On Windows, the default folder is 'My Documents'.
   - On OSX, the default folder is 'Documents'.
 - As you import stacks from the [stack browser][1] there are some rules that must be followed. You will be prompted when you break these rules. In particular:
   1. The stack scale must be set. Set the scale of a [stack][2] in a stack window with shift+p.
   2. The stack must be loaded. Double click the stack in the [stack browser][1] to load a stack.


###Importing a bSpine map
<IMG class="img-float-left" SRC="../images/mm3/mm3-import-bspine.png" WIDTH="275">

Importing bSpine maps is tricky. The problem is if your original maps for one time-series (_d1, _d2, etc.) have different sessions. For example, _d1 has sessions from dates 1,2,3 but _d2 has sessions from dates 1,2,6,12 there <span style="color:red">will be an error</span>.

Thus, there are two cases:

 1. Your maps _d1, _d2 etc. all have the same exact sessions
 	This is simple, use 'Batch import bSpine map'. You will be prompted for the first map (you should select _d1). Once this is done, you need to hit all the buttons in '(2) fix' to complete the import and then 'save map' in the main map manager 3 panel.
 	
 2. Your maps _d1, _d2 etc. have different sessions.
	<span style="color:red">This DOES NOT WORK.</span>


 **This documentation is not done**
 
 ####Import group
 
 - **Import One bSpine map.** ... not done
 
 - **Append One bSpine map.** ... not done
 
 #### Fix group
 
  - ** I am sick of writing documentation. Please see Bob for instructions. **
 


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
[13]: /mapmanager/main-panel/

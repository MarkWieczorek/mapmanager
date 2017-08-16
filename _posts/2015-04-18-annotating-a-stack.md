---
layout: page
title: "Annotating a stack"
category: workflow
date: 2015-02-21 22:46:33
order: 1
tags:
- Imaging core
- Workflow
- Posts
---

This describes a workflow for annotating 3D points in a **single stack**. Please see [making a map][3] to collect a sequence of stacks into a timeseries map.

#### 1. Open and initialize Map Manager

- Open Map Manager in Igor Pro (double-click the Map Manager.ipf file).
- Click in the Igor Pro command window to compile (the command window is titled 'Untitled').
- Open the [Stack Browser][2] window by selecting the main menu 'MapManager - Stack Browser'.

#### 2. Load a stack
- Either  
    Load a directory of .tif files using the 'Load Generic Directory' button.
- Or  
    Drag and drop a single .tif stack onto the Igor Pro program icon.

#### 3. Display a stack

Once a stack is loaded in the [Stack Browser][2], double-click on its name in the list to display the stack in a [Stack][1] window.

#### 4. Add 3D annotations

Each stack can have a list of 3D annotations, we call this a stack database (stack db).

- In a [stack][1] window, open the annotation toolbar with keyboard '['.
- Add a new 3D point with shift+click.
- Delete a point by selecting the point (mouse left-click) and hitting keyboard 'Delete' or 'Backspace'.
- Each point can have a textual note, select the point and press keyboard 'n' to enter a note..
- See the [stack annotations][12] page for complete information.

#### 5. Save your work

- Save stack annotations using the 'Save' button.
- Load saved stack annotations with the 'Load' button.
- <b>Important:</b> You are responsible for saving your annotations. Use the 'Save' button.

### Important concepts

#### Stack scale

Please set the proper X/Y/Z scale before making any annotations. Set the X/Y/Z stack scale in the main stack window with keyboard 'shift+p'.

Once 3D points are created, **the scale can not be changed**.

<p class="important">You need to set the proper X/Y/Z stack scale, in um, with keyboard 'shift+p'. This is a critical step in Map Manager as many measurements are made using um. Once annotations are reated the scale can not be changed.</p>



#### Searching

Open the [Search panel][6] from the left annotation toolbar using the 'Search' button.

The search panel will search stack annotations and return a list of annotations. Once generated, clicking on an annotation in the search results will display the annotation in the main stack window.

Different types of searches are performed with buttons:  

- All : Generate a list of all annotations in a stack.
- Notes : Generate a list of all annotations with notes.  
- Close : Search for annotations that have other annotations within a 3D distance.

If you zoom the stack window (ctrl+mouse wheel or keyboard +) you can snap to different points while maintaining the zoom using the search panel 'Snap' checkbox.

The search results are a static output report. Once a search is performed, if points in the main stack window are modified (add, delete, move) the search results will not be automatically updated. If the points are modified in the main stack window, simply perform the search again.


<div class="print-page-break"></div>


[1]: stack
[2]: stack-browser
[3]: making-a-map
[4]: stackdb-options-panel
[5]: annotating-a-stack
[6]: search-panel
[7]: plot-panel
[8]: map-plot
[9]: fitting-segments-in-fiji
[10]: file-format
[11]: reports
[12]: stack-annotations
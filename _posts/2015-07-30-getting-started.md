---
layout: page
title: "Getting started"
category: workflow
date: 2015-07-30 22:46:33
order: 1
tags:
- Workflow
---

###Installing Igor Pro

 - Igor Pro is a cross platform program that runs on both Windows and Mac OS X.
 - You need to [purchase][2] an Igor Pro license from [Wavemetrics][1], [download][3] the software, and install.
 - To try out Igor Pro, you can download and install a fully functional but time limited [demo version][4].

###Installing Map Manager

 - Once Igor Pro is installed, there is no formal installation of Map Manager
 - Get the source code from Bob.
 - The source code will be in a folder named 'MapManager_date' where 'date' is the date the software was created. The folder will be something like 'MapManager_20151117'.
 - Run the software by double-clicking MapManager.ipf from within your source code folder.
 - To fit lines in FIJI you will have to specify a hard-drive path to FIJI and install a plugin in FIJI. Please see [fitting segments in fiji][7].
 
###Opening Map Manager

 - Open MapManager.ipf into Igor Pro (just double click the MapManager.ipf file).
 - Once in Igor Pro, click in the command window to compile Map Manager and activate the main menus. The command window is in the lower left of your screen and has the window title 'Untitled'.
 - To score a single timepoint stack, select the main menu 'MapManager - Stack Browser' to open the [Stack Browser][6] panel. See [Simple Stack DB][10] for more information.
 - To score a timeseries of stacks (a map), select the main menu 'MapManager - Map Manager Panel' to open the main [Map Manager panel][5]. See [Making A Map][11] for more information.

###Closing Map Manager

When you quit Igor Pro, you will always be prompted with the following dialog. You want to answer **No**. All Map Manager analysis is saved using the 'Save' buttons from within the Map Manager interface.
<IMG class="img-float-left" SRC="../images/mm3/quit-igor.png" WIDTH="450">
<div class="print-page-break"></div>

###Map Manager Options

Global options are primarily set in the [Stack DB Option Panel][9]. There is one set of options that will be saved and reloaded the next time you run Map Manager. You can also save options to your own user file. See [Stack DB Options][9] for mor information.


[1]: https://www.wavemetrics.com/index.html
[2]: https://www.wavemetrics.com/order/order1.php?type=Academic
[3]: https://www.wavemetrics.com/support/versions.htm
[4]: https://www.wavemetrics.com/support/demos.htm
[5]: /mapmanager/main-panel/
[6]: /mapmanager/stack-browser/
[7]: /mapmanager/fitting-segments-in-fiji/
[8]: /mapmanager/user-files/
[9]: /mapmanager/stackdb-options-panel/
[10]: /mapmanager/simple-stack-db/
[11]: /mapmanager/making-a-map/

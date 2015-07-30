---
layout: page
title: "Getting started"
category: post
date: 2015-07-30 22:46:33
order: 1
tags:
- xxx
---

###Installing Igor Pro

Igor Pro is a cross platform environment that runs on both Windows and Mac OS. For lack of a better comparison, Igor Pro is similar to Matlab.

You need to [purchase][2] an Igor Pro license from [Wavemetrics][1], [download][3] the software, and install.

To try out Igor Pro, you can download and install a fully functional but time limited [demo version][4].

As of July 2015, the current Igor version is 6.37.

###Installing Map Manager

 - Once Igor Pro is installed, there is no installation of Map Manager, you just run the software. You need to get the source code from Bob.
 - To fit lines in FIJI you will have to specify a hard-drive path to FIJI and install a plugin in FIJI. Please see [fitting segments in fiji][7].
 
###Opening Map Manager

 - Open bStack.ipf into Igor Pro (just double click the bStack.ipf file).
 - Once in Igor Pro, click in the command window to compile Map Manager and activate the main menus.
 - To score single timepoint stacks, selecting the main menu 'bStack -> Stack Browser' will open the [Stack Browser][6] panel.
 - To score timeseries of stacks (maps), selecting the main menu 'mm3 -> Map Manager 3' will open the [Map Manager panel][5].


###Closing Map Manager

When you quit Igor Pro you will always be prompted with 'Do you want to save changes to experiment "Untitled" before quitting'. You do **NOT** need to do this, always **answer No**. All Map Manager analysis is saved using the 'Save' buttons from within the Map Manager interface.

[1]: https://www.wavemetrics.com/index.html
[2]: https://www.wavemetrics.com/order/order1.php?type=Academic
[3]: https://www.wavemetrics.com/support/versions.htm
[4]: https://www.wavemetrics.com/support/demos.htm
[5]: /mapmanager/main-panel/
[6]: /mapmanager/stack-browser/
[7]: /mapmanager/fItting-segments-in-fiji/
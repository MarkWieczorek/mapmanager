---
layout: page
title: "Fitting segments in Fiji"
category: post
date: 2015-04-21 22:01:06
tags:
- xxx
---

Line segments are fit in FIJI using Map Manager specified control points.

###FIJI Version

You are required to use ImageJ 1.47v, this corresponds to the 'Fiji Life-Line version, 2013 July 15' on the main [FIJI download page][1].

The reason we use this older version of FIJI is that newer versions of FIJI have undocumented changes to the backend JAVA programming interface. Until this is resolved, e will use an older version of FIJI.

Platform specific version can be downloaded here (these are slightly newer but seem to work)

 - Mac: http://fiji.sc/downloads/Life-Line/fiji-macosx-20140602.dmg
 - Windows: http://fiji.sc/downloads/Life-Line/fiji-win64-20140602.zip

###Installing the 'Bob Neurite Tracer' plugin

When you fit a line in FIJI from within Map Manager, you are using the FIJI plugin Bob_Neurite_Tracer_v3.java

To install this plugin

 1. Download Bob_Neurite_Tracer_v3.java [here][4] or from a Github repository [here][2].
 2. Copy Bob_Neurite_Tracer_v3.java into your FIJI plugins directory.
 
###Configuring Map Manager to fit a line In FIJI
 
You need to specify the location of your FIJI program. This is most easily done with a Map Manager [User File][3]. The file needs to contain a line like this...
 
	# specify the location of your FIJI executable. Please use a lifeline version for now.
	#mac
	root:stackdb2:options:gFijiPath="/Users/cudmore/Fiji.app/Contents/MacOS/Imagej-macosx"
	#windows
	#root:stackdb2:options:gFijiPath="C:\Users\cudmore.linden-image2\Desktop\Fiji.app\fiji-win64.exe"


[1]: http://fiji.sc/Downloads
[2]: https://github.com/cudmore/bob-fiji-plugins
[3]: /mapmanager/user-files/
[4]: ../images/Bob_Neurite_Tracer_v3.java

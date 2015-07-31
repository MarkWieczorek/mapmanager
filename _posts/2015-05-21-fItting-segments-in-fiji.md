---
layout: page
title: "Fitting segments in Fiji"
category: post
date: 2015-04-21 22:01:06
tags:
- xxx
---
 
Line segments are fit in FIJI using Map Manager specified control points.

###The version of Fiji is critical

You are required to use ImageJ 1.47v, this corresponds to the 'Fiji Life-Line version, 2013 July 15' on the main [FIJI download page][1].

If you already have a newer version of Fiji installed, this is fine as two versions of Fiji can be installed. They just have to be in different hard-drive folders.

Once downloaded, drag and drop the Fiji.app application folder to your user folder or to your desktop and then copy the Bob_Neurite_Tracer_v3 plugin to the 'plugins' folder inside this Fiji.app application folder.

<p class="important"><B>Important.</B> Do <B>NOT</B> install Fiji into 'Program Files'.</p>

The reason we use this older version of Fiji is that newer versions of Fiji have undocumented changes to the backend JAVA programming interface. Until this is resolved, we will continue to use the older version of Fiji.

Platform specific version can be downloaded here (these are slightly newer but seem to work)

 - Mac: http://fiji.sc/downloads/Life-Line/fiji-macosx-20140602.dmg
 - Windows: http://fiji.sc/downloads/Life-Line/fiji-win64-20140602.zip

###Installing the 'Bob Neurite Tracer' plugin

When you fit a line in Fiji from within Map Manager, you are using the Fiji plugin Bob_Neurite_Tracer_v3.java

To install this plugin

 1. Download Bob_Neurite_Tracer_v3.java [here][4] or from our Github repository [here][2].
 2. Copy Bob_Neurite_Tracer_v3.java into your Fiji 'plugins' folder.
 
###Configuring Map Manager to fit a line In Fiji
 
You need to specify the location of your Fiji program from within Map Manager. This is most easily done using the [Hard Drive Paths][5] panel. Here are the details:

 - Run Map Manager with the bStack.ipf file (this is how you always run Map Manager).
 - Open the [HDD Paths][5] panel using the main menu 'mm3 -> Hard Drive Paths'.
 - In the Map Manager HDD Paths panel, specify the path to your Fiji Application with the 'Set' button.
 - Save these options with the green 'Save' button. The next time you open Map Manager, the path to Fiji should be set.
 
If that does not work, you can specify the location of your Fiji program in a Map Manager [User File][3]. The user file needs to contain a line like this...
 
	# specify the location of your Fiji executable.
	#Please use a lifeline version for now.
	#mac
	root:stackdb2:options:gFijiPath="/Users/cudmore/Fiji.app/Contents/MacOS/Imagej-macosx"
	#windows
	#root:stackdb2:options:gFijiPath="C:\Users\cudmore.linden-image2\Desktop\Fiji.app\fiji-win64.exe"

Make sure the actual file exists. Don't assume the name of Fiji is 'fiji-win64.exe', this name changes from version to version of Fiji. If there is an error in your path, you WILL get an error when fitting lines in Map Manager.

<p class="important"><B>Important.</B> If your line fits do not work from within Map Manager, it is either because you have not specified the full path to your Fiji executable or you have not installed the Bob_Neurite_Tracer_v3.java plugin properly.</p>

[1]: http://fiji.sc/Downloads
[2]: https://github.com/cudmore/bob-fiji-plugins
[3]: /mapmanager/user-files/
[4]: ../images/Bob_Neurite_Tracer_v3.java
[5]: /mapmanager/hdd-paths
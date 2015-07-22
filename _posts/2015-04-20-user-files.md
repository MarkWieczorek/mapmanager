---
layout: page
title: "User files"
category: post
date: 2015-04-20 22:46:33
order: 3
tags:
- Posts
---

User files are a mechanism where global options can be easily loaded. This is useful when you have mutiple users or xxx within one map manager installation.

User files allow you to specify global options.

User files are loaded with main menu 'bStack -> Load User'

Here is an example user file...

	#mac
	root:stackdb2:options:gFijiPath="/Applications/Fiji.app/Contents/MacOS/Imagej-macosx"
	#windows
	#root:stackdb2:options:gFijiPath="C:\Users\cudmore.linden-image2\Desktop\Fiji.app\fiji-win64.exe"

	#default point size for stack db objects
	root:stackdb2:options:gPointSize=3

	#default size for user selections
	root:StackDB2:options:gPointSelSize=5

	#default stack window width
	root:bStack:gStackWindowWidth1=1000

	#default segment radius
	root:line2:options:gDefaultSegmentRadius=0.35

	#set the number of image planes an object is visible
	#controls mask as you scroll up/down with mouse wheel
	root:bStack:gMaskWindow=2

	#turn on real-time intnesity analysis
	root:stackdb2:options:gAnalyzeIntOnNewSpines = 0
	root:stackdb2:options:gShowSpineIntensity = 0

	root:line2:options:gFIlterSWC_BoxWidth = 5
	root:line2:options:gFIlterRadius_BoxWidth = 5

	root:bNV:gUserName="cudmore"

	#stack browser
	root:bStack:gRootHDD=""

	#
	root:bStack:gRootHDD="fourt:jhu:data:"
	#
	root:bStack:gAnalysisPath="Vasculature:Users:cudmore:jhu:vascularAnalysis:"

	# set defaults in ‘Process Image’
	# ch1 defaults
	root:bProcess:gAutoContrast=1
	root:bProcess:gMinContrast=0
	root:bProcess:gMaxContrast=200
	root:bProcess:gColorTable="Green"

	# ch2 default
	root:bProcess:gAutoContrastCh2=1
	root:bProcess:gMinContrastCh2=0
	root:bProcess:gMaxContrastCh2=200
	root:bProcess:gColorTable2="Grays"

	#“”
	
####Specify default user file to save maps:
    root:MapManager3:gMapDriveDir = "vasculature:Users:cudmore:Documents:MapManager3:"
---
layout: page
title: "Release Notes"
category: post
date: 2016-04-22 01:46:33
order: 2
tags:
- faq
---

### 20160422 Update (file version 20151224)

#### New Features

- Jumping spines
- Added jumping to map search

Jumping spines are specified just like other persistent spines. select spines in both time-points and hit keyboard 'p'. When you make jumping spines, the source and destination spines are required to be subtraction and addition respectively.

- Plot run +/- now has option to set 'row' of run

- Added 'Div' option to plot panel.
- Added option to normalize all spines to a constant value

- Segment density report now has segment position information {zMin, zMax, zMean, zMedian, xyAngle, tort}

- Main map manager panel now remembers its position
- Main map plot now remembers its position

- Conrol click on close all windows will now close tables

#### Improvements

- No more limitation on length of file names when importing into stack browser

- Fast left/right mouse click should no longer be a problem

- User clicks during long operations like opening a run should no longer be a problem

- Right-click in map plot to make selection now works for (+/- from mask)

- Stats button in map plot will now report grand mean of all spine masks in plot (previously was only per segment)

- All spine dynamics now plot following colors and size specified in table in options panel
- The size of masks in map plots now follow 'pntSel' in main map manager options panel

- Revamped example user file. tried to make it clear that this can be empty and that values specified will over-ride setting in main options panel

- Added dynamics menu to right-click in map plot


#### Bug Fixes

- Fixed export to text.
If there is an error during export. 'Clear User' then 'Analyze User Map' and try export again. 

- Replotting a run while existing run is linked will continue to correctly link

- Linked windows +/- zoom now works when some windows have left control bar and some do not


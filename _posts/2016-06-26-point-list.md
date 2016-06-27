---
layout: page
title: "Point List"
category: interface
date: 2016-06-26 22:46:33
order: 2
tags:
- Analysis
---

<style>
table{
    border-collapse: collapse;
    border:1px solid #000000;
    margin-left:50px
}

th{
    border:1px solid #000000;
    padding: 5px;
}

td{
    border:1px solid #000000;
    padding: 5px;
}
</style>

<IMG class="img-float-left" SRC="images/mm3/point-list2.png" WIDTH="800">

<div class="print-page-break"></div>

The point list panel displays a list of points for one stack.

To open a point list panel

 - Right-click a stack and select the menu 'Windows ... Point List'.
 - In a stack window, use the 'Point List' button in the left-panel. Open the left-panel with keyboard '['.

### Interface

Select individual points in the list and the selection will propagate to open [stack windows][1], [stack][5] plots and [map][2] plot windows. Use the **center on selection** checkbox to automatically snap selected objects in their stack windw.

### Edit User Type

Turn this on and the point list window will respond to the following keystrokes. Setting the value of 'userType' as:

|Index	|Key	|Result
| :------ | :-------------- | :-------------
|0		|u		|Unknown
|1		|m		|Mushroom
|2		|f		|Filapodia
|3		|l		|Long
|4		|s		|Stubby
|		|Del	|-clear the entry-

<BR>
Counts for each of these user types are included in each segments [density report][4].

### Plotting

Right-click a column header and select **Quick Plot** to plot that stat versus the sequential number of each spine. The sequential number of each spine is the order they were created in, it is not the order along the dendrite.

Any two columns can be plotted as X and Y. Right click a column and select **Set X Stat**, then right-click another column and select **Set Y Stat**. Then use the main **Plot** button to plot X versus Y.

### Columns

To make the table easier to read, columns can be turned on and off with the check-boxes in the **Columns** group.

Clicking on a column will sort the table by that column.

[1]: stack
[2]: map-plot
[3]: stack-browser
[4]: reports
[5]: stack-plot

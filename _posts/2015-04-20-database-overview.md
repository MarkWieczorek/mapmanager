---
layout: page
title: "Database overview"
category: workflow
date: 2015-04-20 22:46:33
order: 1
tags:
- Workflow
---

Map Manager builds a database of 3D objects and line segments within a single [stack][1]. Stacks and their associated 3D objects and line segments can then be connected together into a time-series with a [map][2].

Manage a stack db for a single stack with the [stack db interface][3].

Manage a map with the [map making interface][4].

###Definitions

####Stack

A 3D image.

####Stack Database (**stack db**)

A collection of 3D points and line segments within a single stack.

####Line Segment

A line tracing within a single stack.

####Map

A time-series of stacks and their associated stack db(s).

####Run

A sequence of stacks. A run can follow either 3D points or line segments for each stack in a map.

[1]: /mapmanager/stack/
[2]: /mapmanager/map-plot/
[3]: /mapmanager/annotating-a-stack/
[4]: /mapmanager/making-a-map/

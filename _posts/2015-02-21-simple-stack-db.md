---
layout: page
title: "Simple stack database"
category: post
date: 2015-01-30 22:46:33
order: 5
---

##Introduction

This document describes one of the most simple workflows.

- Open and initialize bStack
- Open a .tif stack
- Add 3D annotations
- Save the database

##Open and initialize bStack

- Open bStack.ipf in Igor (double-click the desktop icon).
- Initialize bStack using menu 'bStack -> Load User' and select 'yunju_branch_points.txt'  
    This will open the Stack Browser window

##Load some stacks
- Either  
    Drag and drop a .tif stack onto the Stack Browser.
- Or  
    Load a directory of .tif files using the 'Load Generic Directory' button.

Once a stack is displayed in the Stack Browser, double-click on a stack in the list to open a [Stack][1] window.

####Add 3D annotations
A stack can be annotated with 3D points, we call this a 'stack db'. Each stack db can be saved and reloaded later.

- Open the stack db interface with keyboard '['
- Add a new 3D point with shift+click
- Save 3D annotations using 'Save' button
- Load previously saved annotations with 'Load' button

- Delete a point by selecting the point (mouse left-click) and hitting keyboard 'Delete' or 'Backspace'

- Each point can have a textual note, select the point and fill in a note in the field below the list of points.

####Search
The search panel allows a stack db to be searched and will generate a list of points.

Open the search panel with the 'Search' button.

Different types of searches  

- All : Generate a list of all stack db points  
- Notes : Generate a list of stack db points with notes  
- Close : Search for points that have other points that are close

Once a search is performed, the search panel will display a list of results. Each row in the list is a point. Single-click on a point in the list and it will be selected in the main stack window.

If you zoom the stack window (keyboard +) you can snap to different points while maintaining the zoom using the 'snap' checkbox.


####Important concepts

- After a stack db is saved, it will automatically be loaded the next time bStack is run and the stack db interface is opened with keyboard '['
- You are responsible for saving your stack db with the 'Save' button  
    If you do not save and you quit Igor, the stack db WILL NOT BE SAVED
    

[1]: /Vascular-Analysis/stack/


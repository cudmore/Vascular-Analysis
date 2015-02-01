---
layout: page
title: "change log"
category: post
date: 2015-01-30 22:01:06
---

###20150109

Finally getting around to some bug fixes

####New Features
1) edges now have notes. use info window, 'i' from main hyperstack window

2) can now search for edges and slabs (previously search was limited to nodes)
	we will use this to step through all slabs and edit radius/pericyte

3) can now mark a slab as pericyte
	in main hyperstack window, keyboard 'p'
	in slab search result list, keyboard 'p'
	in slab diameter panel, with checkbox

####Bug Fixes
- fixed moving cursor bug when turning on ‘manual’ connect.  
	see: print "20150109, removed call to SlabRadius_SetZ() to fix 'manual' bug. May cause errors"  
- decided to NOT fix extra slab when user clicks left-mouse and are no longer holding down ’s’  
    workaround is to just hit 'esc'  
- entering out of bound timepoints will now warn when displaying a hyper stack stack window or FindPnt  
- we no longer warn when switching between auto/manual slab  

- temporary one liner to fix color of nodes (is incorrect defaulting to black)  
    M_Colors[1][0]=65535;M_COlors[1][1]=49151;M_Colors[1][2]=49151



###20150123

####New Features
1) revamped the 'search' panel.
- can now search for different kinds of objects: nodes, edges, slabs
- added feedback on last search type (node/edge/slab) and the number of hits
- better system for opening stacks (and stack runs) when an object is selected in the search results

2) edges now have isDiving and isSurface values
- To set Diving and/or Surface, select an edge and hit 's' to toggle 'isSurface' and 'd' to toggle 'isDiving'
- These keyboard command will work for an edge selection in search results
- ToDo: these keyboard commands will work in the main hyperstack window (problem is that 's' is already mapped to making a new slab)

####Minor Improvements
- when loading a hyperstack and it is already loaded, we will only ask you once and if you accept we will OVERWRITE the already loaded hyperstack
    Previously, we would ask to verify loading each timepoint
- The main Hyperstack panel will always default to timepoint 0 and TP 2 1.




###20150129 Henri started

####New Featurues
- changed system of delete for slab and node. Now just select object and hit 'Delete'
- changed system of move for node and slab. Now just select object and hit 'm'
	Next click will be the new position (including z)
	Esc will cancel out and not move

####Minor Improvements
- main hyperstack panel now has interface to edit raw repo path (use expansion triangle)
	next step is to get some of student scoring data onto solid-state-drive (requires swapping rawRepo)
- stepping forward/back to next slab with left/right arrow keys now stops you at the enf the edge (at the lst slab)
- manual slab cursors are now red

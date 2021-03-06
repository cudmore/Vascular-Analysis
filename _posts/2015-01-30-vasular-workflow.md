---
layout: page
title: "Vascular workflow"
category: workflow
date: 2015-01-30 21:56:18
order: 1
tags:
- Imaging core
- Workflow
---


####(1) Make nodes, tubes and slabs in one timepoint

- See [Vascular tracing][5] for more information  

- Create a node at one vascular branch point (shift+click)
- Create another node at the other end of the same tube (shift+click)
- Create a tube by selecting the first branch point (source) then N+click the second branch point (destinaiton).
- Create slabs along the tube with S+click


#####Check each slab diameter for each new tube
- Once all slabs for a tube are done, review the slabs (and their radii) using left/right arrow keys. Fix slabs with bad radii using the [editing slabs][4] interface

#####Keep in mind
- If marking a subset of tubes, only mark tubes where you would put more than one slab, e.g. don't score super short tubes.  
- If marking a subset of tubes, keep an eye on the depth (image plane) of your tubes. You should only mark tubes that are in and around layer II/III somas. Use keyboard '2' to switch to channel 2, the somas appear as black dots.
- If a tube has a pericyte, try and get a slab centered on it. If this is not possible, specify 'has pericyte' for the edge using the [Point Info][3] window.  
- Annotate your images (using node and tube notes) with anything that is out of the ordinary or just cool.  


####(2) Make similar nodes, tubes and slabs in the next timepoint
- You can open sequential timepoints using the [Find Points][1] window

####(3) Connect nodes from one timepoint to the next using [Find Points][1] window
- Open FInd Points for two consecutive timepoints, e.g. timepoint 4 and 5.
- Selecting a row in the list in Find Points will open two stacks, snap the images to the same region and highlight the selected node (if they are connected).
- Use keyboard arrow keys in the Find Points list to scroll through nodes. Keyboard left will flash the programs best guess, Keyboard right will flash the actual connection.
- Keyboard shift + right-arrow will transfer the Guess to the Dst.
- If the guess is not to your liking, select the nodes you want to connect (in their stack windows), right-click on the desired destination node and select 'FindPnt -> Dst' menu. 

####(4) Quality control


- Check all slab diameters using [search][2] 'All Slabs'. Scroll through the list of slabs for a timepoint and the slab selected in the list will be selected in the image

####(5) Marking tubes as diving, surface, has pericyte and marking branch order

- See [Scoring tubes][6] for more information.
- In one timepoint, mark all tubes as diving (keyboard 'd') or surface (keyboard 's'). If a tube is neither, leave this blank.
- In the same timepoint, mark the branch order of each tubes 0..9. If you can't determine the branch-order of a tube, leave it blank.
- Mark tubes with pericytes (keyboard 'p')

[1]: /Vascular-Analysis/find-points/ "find-points"
[2]: /Vascular-Analysis/search/ "search"
[3]: /Vascular-Analysis/point-info/ "point-info"
[4]: /Vascular-Analysis/editing-slabs/ "editing-slabs"
[5]: /Vascular-Analysis/vascular-tracing/ "vascular-tracing"
[6]: /Vascular-Analysis/scoring-tubes/ "scoring-tubes"

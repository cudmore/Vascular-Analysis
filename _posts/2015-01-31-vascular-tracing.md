---
layout: page
title: "Vascular tracing"
category: interface
order: 2
---

All three types of object (nodes, edges and slabs) have a similar interface to select, create, move and delete. All objects are placed in x/y and z where z is the currently viewed imaging plane.

####Nodes (Nodes are vascular branch points)
- Select: left-click (will turn yellow)  
- Create: shift+click  
- Move: select and press keyboard 'm', next click will be new posiiton  
- Delete: select and press keyboard 'Del'  
- Notes: Use the Point Info window (open with shift+?)  

####Edges (Edges are vascular tubes that connect one branch point to another)
- Select: left-click a slab within the edge
- Create: Making a new edge is a two step process  
	(1) select the source node  
	(2) N-click the destination node (a line will be formed between them)  
- Move: Edges cannot be moved
- Delete: right-click and select 'Delete Edge'
- Notes: Use the Point Info window (open with shift+?)

####Slabs (Slabs are the actual tracing along a vascular tube)
- Select: left-click
- Create: S-Click
- Move: select and press keyboard 'm', next click will be new posiiton
- Delete: select and press keyboard 'Del'
- Notes: Slabs do not have notes


> Once a slab is selected you can scroll to the next/previous slab using keyboard left/right.

<div></div>

> It is sometimes hard to select a slab if it is not in the currently viewed imaging plane.
> Scroll the image up or down a bit and try again.

<p class="important">
All objects are placed in x/y and z. Where z is the currently viewed imaging plane.
</p>
<p class="important">
Only one edge between any two branch points.
</p>
<p class="important">
When a node, edge, or slab is selected it will be visible in all imaging planes, not just the currently viewed imaging plane.
</p>

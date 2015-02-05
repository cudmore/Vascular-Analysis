---
layout: page
title: "Find points"
category: interface
date: 2015-02-01 22:46:33
order: 4
---

The Find Points window allows nodes and edges to be connected between sequential timepoints in a hyperstack.  

Open Find Points for a source and destination timepoint in the main [Hyperstack Panel][1].  


###Nodes

<figure>
<IMG SRC="../images/findpnts_example.jpg" WIDTH="900">
<figcaption>FInd Points for nodes with Src node 7 connected to Dst node 8.</figcaption>
</figure>


The goal is to fill in the Dst column with the correct nodes, e.g. a mapping of each node in the Src timepoint with a node in the Dst timepoint.

FInd Points will show you a list of nodes in the first timepoint (Src) with their corresponding connection in the second timepoint (Dst).

When you first open Find Points there will be no Dst nodes filled in, that is your job.

The 'guess' column is the programs best guess for which nodes are connected. This guess is created using [Pivot Points][2].

You basically have two choices for each Src node:

- If you like the Guess, transfer the Guess to the Dst by selecting the row in Find Points and using keyboard 'shift + right-arrow'. That is 'hold shift and hit the right-arrow'.

- If the guess is not to your liking, select the source node and the destination node to connect (in their respective image stacks) and right-click on the destination node (still in the image stack) and select menu 'FindPnt -> Dst'.

Scrolling through the list will highlight nodes in the Src and Dst at the same time. Once a row is selected, left-arrow will flash the Guess and right-arrow will flash the Dst.


###Edges

<figure>
<IMG SRC="../images/findpnts_edges.jpg" WIDTH="900">
<figcaption>Find Points for edges with Src edge 4 connected to Dst edge 4.</figcaption>
</figure>


Expand the FInd Points window with the disclosure triangle (top right of the window) to see a similar list for edges.

Edges in red are edges that have a mismatch between their starting and ending nodes.

You don't actually edit the connections between edges, you edit the connections between nodes and the edges will follow. This works because we only allow one edge between and two nodes (think about it).

Goal is to modify your node connecitons until the edges are as good as they can get.


[1]: /Vascular-Analysis/hyperstack-panel/
[2]: /Vascular-Analysis/pivot-points/ "Pivot Points"

---
layout: page
title: "Find points"
category: interface
date: 2015-02-01 22:46:33
order: 4
---

The Find Points window will display two timepoints simultaneously and provides an interface to manage the connections between both nodes and edges across timepoints.  

Open Find Points from the main [Hyperstack Panel][1] by specifying 'Timepoint' and 'Timepoint 2'. Select a row in Find Points and both the source and destination stacks will be opened.

<P class="important">
When you first click a node row in the Find Points window, you are opening two image stacks. This will take some time. Let the program finish opening the stacks before you continue interacting with the interface.
</p>

####Interface

The Find Points window displays a list of nodes in the source timepoint (Src column). For each node in the source timepoint, Find Points shows the corresponding connected node (if there is one) in the second timepoint (Dst column).

The Guess column shows the best guess for the corresponding node in the second timepoint. This guess uses each timepoints [Pivit point][2].

Once a node is selected, the keyboard can be used to scroll through the nodes in the Find Points list and nodes will be selected simultaneously in both the source and destination image stacks.

- Up arrow : Scroll to the previous node
- Down arrow : Scroll ot the next node
- Left arrow : Flash the Src node (in first timepoint) and Guess node (in second timepoint).
- Right arrow : Flash the Src node (in first timepoint) and Dst node (in second timepoint).
- shift + right-arrow : Transfer the Guess node to Dst node
- Del : Delete the Dst node (not the node itself, just the correspondence)

###Nodes

<figure>
<IMG SRC="../images/findpnts_example.jpg" WIDTH="900">
<figcaption>Find Points for nodes with Src node 7 connected to Dst node 8.</figcaption>
</figure>


The goal is to fill in the Dst column with the correct nodes, e.g. a mapping of each node in the Src timepoint with a node in the Dst timepoint.

Find Points will show you a list of nodes in the first timepoint (Src) with their corresponding connection in the second timepoint (Dst).

The 'Guess' column is the programs best guess for which nodes are connected. This guess is created using [Pivot Points][2].

Scroll through each source node and do the following:

- If the Guess is correct, transfer the Guess to the Dst by selecting the row in Find Points and using keyboard 'shift + right-arrow'. That is 'hold shift and hit the right-arrow'.
- If the Guess is not current, select the source node and the destination node to connect (in their respective image stacks) and right-click on the destination node (still in the image stack) and select menu 'FindPnt -> Dst'.
- Use 'Del' key to remove a node from the Dst column.

If a node in the second timepoint does not have a match in the first timepoint it is appended to the end of the list. This node can be selected as usual and allows for a reverse lookup from the second timepoint to the first.

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

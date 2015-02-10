---
layout: page
title: "Pivot points"
category: interface
date: 2015-02-01 22:46:33
order: 7
---

Pivot points allow 3D image stacks to be aligned from one timepoint to the next.

Any node can be a pivot point. In an image stack, select a node and press 'Capture Pivot' button.

When a node is selected as a pivot point for one timepoint, any other nodes connected to that node (with Find Point) will become the pivot point for that timepoint.

If each itmepoint has  aPivot Point then we have a 'reference frame' by which to align the image stacks between timepoints.

If the 'Guess' in [Find Points][1] starts to be wrong or does not show up at all, assign a node as a pivot point near the nodes you are working on and the 'Guess' should get better.

Pivot points appear in image [stacks][3] as a blue circle. Pivot points appear as blue cells in [Find Points][1].

####Put another way

For each source node we generate a guess node using a pivot point in the two images. A pivot point is a special node that the user identifies as being the same in both images. By using the 3D position of this pivot, we can search from the source image to the destination image and look for nodes near that pivot (the closest match becomes the Guess). This allows for the actual registration of your image stacks to be fairly innacurate/bad from one timepoint ot the next. This begins to fail if the density of the nodes is high, we have trouble deciding who is actually the connecting node. This also starts to fail is there is a lot of angular rotation between sequential timepoints. This final problem can be greatly reduced by moving the pivot point near where you want to get a good Guess.


####See Also

[Find Points][1],
[Workflow][2]

[1]: /Vascular-Analysis/find-points/ "find-points"
[2]: /Vascular-Analysis/workflow/ "workflow"
[3]: /Vascular-Analysis/stack/ "stack"


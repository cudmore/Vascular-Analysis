---
layout: page
title: "Scoring tubes"
category: post
date: 2015-01-30 22:46:33
order: 2
---

####Introduction

We want to add some more annotation to each vascular tube. We will be scoring each tube to describe:

1. If it is a diving artery/vein
2. If it is a surface tube
3. Its branch order off a main diving artery/vein (the actual diving arteries/veins get branch order 0)
4. Whether or not the tube has a pericyte.

Because your tubes are connected across timepoints using [FindPnts][1] we can annotate tubes in <b>just one timepoint</b> and assuming the tubes don't change (with respect to these annotations) we can generalize these annotations across all timepoints.

You want to choose a timepoint for this new tube annotation that is early on and still easy to see. Just don't use the first timepoint.

####Scoring tube properties

The main hyperstack stack window now has a 'Score Tubes' checkbox. When the 'Score Tubes' checkbox is on and you select an edge, the stack window will respond to the following keystrokes:

- d : Diving (will turn off Surface)
- s : Surface (will turn off DIving)
- p : Has Pericyte
- 0 : Branch order 0 (use this for diving arteries/veins)
- 1 : Branch order 1
- .
- .
- .
- 9 : Branch orer 9
- Del : Clear branch order

If you cannot determine the branch order of a tube, you want the branch order to be empty. Use keyboard 'Del' or just blank out 'Branch Order' in the 'Point Info' window.

You can also bring up the [Point Info][2] window (use keyboard shift+?) and set these values using check boxes for Diving, Surface and 'Has Pericyte' and a numerical field for 'Branch Order'.

####How to get started

- Open a stack window
- Turn on 'Score Tubes' checkbox
- Open point info window (shift + ?)
- Select a tube
- Try out some key strokes: d, s,p, 0, 1, 2, 3, ...
- See how the annotation changes in the point info window

- You want to make sure you get all your tubes annotatd. Clicking around on different tubes in the stack window is not that reliable (you might miss a tube). Use the [Search][3] window to generate a list of all tubes and go through each tube one-by-one.

[1]: /Vascular-Analysis/findpnts/
[2]: /Vascular-Analysis/point-info/
[3]: /Vascular-Analysis/search/

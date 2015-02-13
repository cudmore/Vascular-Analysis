---
layout: page
title: "example user file"
category: post
date: 2015-01-30 22:01:06
---

####Specify setting in Igor command window

Set 2 default window widths. Switch between them with keyboard ']'. Values specify the width of the stack window in screen pixels.

> root:bStack:gStackWindowWidth1 = 350  
> root:bStack:gStackWindowWidth2 = 767.5

####Making a user file
- Make a .txt file in /bHyperstack_Defaults/Users/
- Load the file from within Igor using menu 'Hyperstack -> Hyperstack - Load User File'

####Example user.txt file

	root:bNV:gUserName="Micek"
	
	root:Hyperstack:gHyperstackWindowSize="Small"
	
	#root:Hyperstack:gHyperstackRootHDD="Work:jhu:Hyperstack:"
	root:Hyperstack:gHyperstackRootHDD="d:Users:cudmore:Hyperstack:"
	
	#root:Hyperstack:gHyperstackRawRepo="Work:jhu:hyperstack:rawRepo:"
	root:Hyperstack:gHyperstackRawRepo="d:Users:cudmore:hyperstack:rawRepo:"
	
	#root:Hyperstack:gDatabasePath="Work:jhu:hyperstack:intermediate_hyperstack:micek:"
	root:Hyperstack:gDatabasePath="d:Users:cudmore:hyperstack:micek:"
	
	root:Hyperstack:gLoadAndPlotOnLoad=0
	
	#root:bStack:gIAmSuperuser=1
	
	#micek
	#gHyperstackRootHDD = "d:Users:cudmore:Hyperstack:"
	#gDatabasePath = "d:Users:cudmore:hyperstack:micek:"
	#gHyperstackRawRepo = "d:Users:cudmore:hyperstack:rawRepo:"

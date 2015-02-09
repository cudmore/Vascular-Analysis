---
layout: page
title: "How to use Jekyll"
category: post
date: 2015-01-30 22:01:06
---

####How to do some things in [Jekyll][2]

<iframe width="560" height="315" src="http://www.youtube.com/embed/PWf4WUoMXwg" frameborder="0"> </iframe>

As of Feb 2015 I discovered Jekyll and this has rocked my world. Beautifully done. No more Word-Press for me !!!

####Install on OSX

> sudo gem install jekyll


####Making posts and pages
To make a blog post, the blog-post.md file needs to start with this yaml [front matter][1]  

	---
	layout: page
	title: "example user file"
	category: post
	date: 2015-01-30 22:01:06
	---

To make a new page new-page.md the starting yaml front matter looks like  

	---
	layout: page
	title: "Opening and Closing Igor Pro"
	category: gettingstarted
	date: 2015-01-30 22:38:12
	order: 3
	---

####Making external hypertext links

Reference links look like this

    This links to [Jekyll front-matter page][1]
    This links to [Daring Fireball][2]
    
	[1]: http://jekyllrb.com/docs/frontmatter/ "Jekyll Front-Matter"
    [2]: https://daringfireball.net/projects/markdown/basics "Markdown Bascis"
    

####Internal Links
I edited [_config.yml][3] like this  

	# Dates are not included in permalinks
	#permalink: none
	permalink: /:title

I do not need to add anyhting special to my yaml frontmatter!  

And now
    this works as link to [stack]({{site.baseurl}}/stack/)
this works as link to [stack]({{site.baseurl}}/stack/)

    this also works, [Link to stack page][3]
    [4]: {{site.baseurl}}/stack/ "stack"

this also works, [Link to stack page][4]



####On the mac
I am keeping my local Jekyll sites in /Users/cudmore/Sites/Vascular-Analysis  

To run Jekyll on a Mac,

    cd /Users/cudmore/Sites/Vascular-Analysis
    jekyll serve --watch
    
View the site locally with  

    http://localhost:4000/Vascular-Analysis/
    
View the site on Github

    http://cudmore.github.io/Vascular-Analysis/

####Convert markdown to pdf

 > cd /Users/cudmore/Sites/Vascular-Analysis/_posts  
 > //with TOC  
 > gimli -y -m -s ../css/main.css -w '--toc --footer-right "[page]/[toPage]"' -o pdf  
 > //without toc, -w  is passing commands to backend wkhtmltopdf  
 > gimli -y -m -s ../css/main.css -w '--footer-right "[page]/[toPage]"' -o pdf  
 

gimli -y -m -s ../css/main.css -w '--footer-right "[page]/[toPage]"' -o ../pdf   
gimli -y -m -s ../css/main.css -w '--header-left "[webpage]" --header-right "[page]/[toPage]"' -o ../pdf  
 
####Started using imageoptim-cli
> http://www.smashingmagazine.com/2013/12/17/imageoptim-cli-batch-compression-tool/


[1]: http://jekyllrb.com/docs/frontmatter/ "Jekyll Front-Matter"
[2]: http://jekyllrb.com
[3]: http://jekyllrb.com/docs/configuration/
[4]: {{site.baseurl}}/stack/ "stack"

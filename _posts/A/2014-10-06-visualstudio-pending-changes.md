---
layout: post
title:  "Visual studio pending changes problem + fix"
date:   2014-10-06 12:16:44
categories: blog
tags: ["Visual Studio 2013", "TFS", "Source control"]
---

I was recently running into an issues with Visual Studio 2013 source control which was somewhat annoying. In the "pending changes" window Visual Studio was showing a bunch of file which supposedly was changed but when I did a compare to show changes there where none. Normally this is not an issue as it only only effects one or two files. On my current project we use [Item Generator Tool](https://marketplace.sitecore.net/en/Modules/Custom_Item_Generator.aspx) to generate some of the project files based on content in Sitecore. Whenever we make changes to item templates in Sitecore we need to use the tool to update the code. Unfortunately in this scenario Visual Studio 2013 insist that all the files has changed(when looking in the pending changes window) when in fact only one or two files actually has changes. After a quick search I found this blog post describing a solution to this problem. The blog post can be found [here](http://thesoftwarecondition.com/blog/2011/05/01/tfs-pending-changes-ignoring-files-which-are-identical-to-the-originals/). 

How to solve problem

Install TFS power tools. 
[Here](http://visualstudiogallery.msdn.microsoft.com/f017b10c-02b4-4d6d-9845-58a06545627f)

SET PATH=%PATH%;"C:\Program Files (x86)\Microsoft Team Foundation Server 2013 Power Tools";

Start a Visual Studio command prompt and change directory to the affected workspace. Then run this command.

	tfpt uu /noget /r *
 

The tool will then ask you this 
 
	Do you wish to undo these redundant pending changes? (Y/N)
 
Answering yes will automatically undo items on all the items which has not changed. Now you only need to do a compare on the files that has actually changed :)
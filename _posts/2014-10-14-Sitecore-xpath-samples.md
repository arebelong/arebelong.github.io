---
layout: post
date:   2014-10-15 15:02:44
categories: blog
tags: ["Sitecore", "Sitecore tips and tricks", "XPath", "Sitecore beginner"]
---

In Sitecore there are som fields for which you can write an xpath expression as source eg. to populate a dropdownlist or multilist. 

Sitecore provides a tool which allows you to test your queries as you write them. This tool can be found in Sitecore administration. Sitecore -> All Applications -> Development tools -> Developer Center

![Screenshot of Developer Center](/images/2014/2014-10-15 07_18_55-Sitecore.png)

##Sample queries

Note when using testing the below queries in the Developer Center you need to remove this part 'query:'. This is only needed when adding the query to the source in the template. 

#Ancestor sample
Find root item matching the templateid and follow the path from there. In a multisite scenario this query can be handy. It will find the root of a specific type in this case I have set it to the template used to create new sites. From there I can traverse to a known directory structure. 

	Sample site structure
	uk    ->Settings->Sometool
	german->Settings->Sometool

	query:./ancestor-or-self::*[@@templateid='{11EB82C7-A446-466C-8D7F-A0BC3265B26E}']/Settings/Sometool/*
	
Get all children of the current item of a specific template

	query:./*[@@templateid='{1A198BA6-90DB-4303-8567-484D7FC59DBC}']


Get all children of the current item which match either of two different templates

	query:./*[@@templateid = '{01AD6D2C-1D56-4C00-9334-80598889C9E4}' or @@templateid = '{7588751A-3C6E-43C6-A254-66E5257558F3}']
	
More examples can be find on this blog. 
[http://sitecoreadventures.blogspot.dk/2011/03/using-source-property.html](http://sitecoreadventures.blogspot.dk/2011/03/using-source-property.html)
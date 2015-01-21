---
layout: post
date:   2014-10-08 19:52:44
categories: blog
tags: ["Jekyll", "Pagination"]
---

How to add paginatino to your jekyll site

[http://jekyllrb.com/docs/pagination/](http://jekyllrb.com/docs/pagination/)

Add to _config

paginate: 5

	<!-- This loops through the paginated posts -->
	{% for post in paginator.posts %}
	  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
	  <p class="author">
	    <span class="date">{{ post.date }}</span>
	  </p>
	  <div class="content">
	    {{ post.content }}
	  </div>
	{% endfor %}
	
	<!-- Pagination links -->
	<div class="pagination">
	  {% if paginator.previous_page %}
	    <a href="/page{{ paginator.previous_page }}" class="previous">Previous</a>
	  {% else %}
	    <span class="previous">Previous</span>
	  {% endif %}
	  <span class="page_number ">Page: {{ paginator.page }} of {{ paginator.total_pages }}</span>
	  {% if paginator.next_page %}
	    <a href="/page{{ paginator.next_page }}" class="next">Next</a>
	  {% else %}
	    <span class="next ">Next</span>
	  {% endif %}
	</div>


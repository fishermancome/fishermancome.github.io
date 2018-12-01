---
layout: page
---

<ul class="myposts">
	{% for post in site.posts %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
	<span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
	{% endfor %}
</ul>
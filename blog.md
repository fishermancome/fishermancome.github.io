---
layout: page
---

{% for post in site.posts %}
<div class="post-review">
	<a href="{{ post.url }}" class="post-url">
		<h2 class="post-title">
			{{ post.title }}
		</h2>
		{% if post.subtitle %}
		<h3>
			{{ post.subtitle }} 
		</h3>
		{% endif %}
		<div class="post-content-preview">
			{{ post.content | strip_html | truncate:200 }}
		</div>
	</a>
	<span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
</div>
{% endfor %}

<style>
	h2 {
		color:#000;
	}

	h3{
		color:#444;
		font-size: 15px;
	}
	.post-url {
		text-decoration: none;
		color:#555;
	}
	.post-url:hover{
		text-decoration: none;
		color:pink;
		background-color: pink;
	}
</style>
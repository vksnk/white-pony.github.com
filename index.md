---
layout: page
title: white-pony's blog
---
{% include JB/setup %}

<ul class="posts">
	{% for post in site.posts limit: 15 %}
		<div class="front">
		<div align="right" class="date-container">{{ post.date | date:"%A, %e %B %Y" | upcase }}</div>
		<h3><a href="{{ post.url }}">{{ post.title }} </a></h3>

	        {{ post.content }}
      </div>
      {% if forloop.last == false %}
      </br>
      <hr class="front">
      </br>
	{% endif %}
	{% endfor %}
</ul>
---
permalink: /
title: Home
---

# All of posts.
{%- if site.posts.size > 0 -%}
<ul class="posts">
	{%- for post in site.posts -%}

		{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
	- [{{ post.url | relative_url }}]: {{ post.title | escape }} {{ post.date | date: date_format }}
			{%- if site.show_excerpts -%}
			{{ post.excerpt }}
			{%- endif -%}
	{%- endfor -%}
{%- endif -%}

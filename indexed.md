---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

{% for post in site.posts %}
<li>
<a href="{{ post.url }}">{{ post.title }}</a>
<p>{{ post.excerpt }}</p>
</li>
{% endfor %}

---
layout: default
title: Write-up {OWASP Mutillidae II} | Coming soon

---

<h1>Write-up {OWASP Mutillidae II}</h1>
<hr/>

{% for category in site.categories %}
{% if category[0] == "mutillidaeII" %}
    {% for posts in category %}
    {% for post in posts %}
{% if post.title %}

		{% if post.custom-link %}
<h2><a href="{{ post.custom-link }}"><small>{{ post.date | date: "%d %B, %Y" }}</small>{{ post.title }}</a></h2>
		{% else %}
<h2><a href="{{ post.url }}"><small>{{ post.date | date: "%d %B, %Y" }}</small>{{ post.title }}</a></h2>
		{% endif %}
<p>{{ post.excerpt | truncatewords:25 }}</p>
<hr/>

{% endif %}
   {% endfor %}
   {% endfor %}
{% endif %}
{% endfor %}

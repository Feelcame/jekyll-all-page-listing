---
date: 2021-06-01T01:19:52+03:00
---

### index


### All pages:

<div id="navigation">
{% for p in site.pages | sort: 'date', 'last' %}{% if p.dir == page.dir %}
<p><a href="{{ p.url | prepend: site.baseurl }}">{{ p.title }}</a> 
<time class="shaded">{{ p.date | date: "%Y-%m-%d" | default: "гггг-мм-дд" }}</time></p>
{% endif %}{% endfor %}
</div>

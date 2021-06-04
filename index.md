---
date: 2021-01-01T00:00:00+00:00
---

### index
Эта папка - ({{ page.dir }})

<a href="./testdir">другая папка - ./testdir</a> 

### All pages:

{% assign allpages = site.pages | sort: 'date' %}
{% for p in allpages %}{% if p.dir == page.dir %}
<p><a href="{{ p.url | prepend: site.baseurl }}">{{ p.title }}</a> 
{{ p.date | date: "%Y-%m-%d" | default: "гггг-мм-дд" }}</p>
{% endif %}{% endfor %}

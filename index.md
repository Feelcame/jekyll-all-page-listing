---
date: 2021-01-01T00:00:00+00:00
---

### index
Эта папка - ({{ page.dir }})
<a href="./testdir">другая папка - ./testdir</a> 

### All pages:

<div id="navigation">
{% for p in site.pages | sort: 'date', 'last' %}{% if p.dir == page.dir %}
<p><a href="{{ p.url | prepend: site.baseurl }}">{{ p.title }}</a> 
<time class="shaded">{{ p.date | date: "%Y-%m-%d" | default: "гггг-мм-дд" }}</time></p>
{% endif %}{% endfor %}
</div>

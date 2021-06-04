---
date: 2021-01-01T00:00:00+00:00
---

### index
Эта папка - ({{ page.dir }})

<a href="./testdir">другая папка - ./testdir</a> 

### All pages:
{% assign allpageswithdate = site.pages %}
{% for p in allpageswithdate %}
{% if p.date != true %}
неверная дата...  
{% p.date = page.date %}
{% endif %}{% endfor %}


{% assign allpages = site.pages | sort: 'date' | reverse %}
{% for p in allpages %}{% if p.dir == page.dir %}
<p><a href="{{ p.url | prepend: site.baseurl }}">{{ p.title }}</a> 
{{ p.date | date: "%Y-%m-%d" | default: "гггг-мм-дд" }}</p>
{% endif %}{% endfor %}

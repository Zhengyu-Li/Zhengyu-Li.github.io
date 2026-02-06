---
layout: page
title: Publications
# description: List of publications
# permalink: /publications/
---

## Conference Papers

{% for p in site.data.publications.conference %}
<div class="box">

<h4>
  <a href="{{ p.url }}">{{ p.title }}</a>
</h4>

<p class="note">
  {{ p.authors | join: ", " }}<br>
  <em>{{ p.venue }}</em>  {{ p.year }}
</p>


<p>
  {% if p.pdf %}<a href="{{ p.pdf }}">[PDF]</a>{% endif %}
  {% if p.code %} · <a href="{{ p.code }}">[Code]</a>{% endif %}
</p>

</div>
{% endfor %}


<!-- ## Journal Articles

{% for p in site.data.publications.journal %}
<div class="box">

<h4>
  <a href="{{ p.url }}">{{ p.title }}</a>
</h4>

<p class="note">
  {{ p.authors | join: ", " }}  
  <em>{{ p.venue }}</em>, {{ p.year }}
</p>

<p>{{ p.abstract }}</p>

<p>
  {% if p.pdf %}<a href="{{ p.pdf }}">[PDF]</a>{% endif %}
  {% if p.code %} · <a href="{{ p.code }}">[Code]</a>{% endif %}
</p>

</div>
{% endfor %}

--- -->
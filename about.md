---
layout: about
title: About Me
# description: About me
---

## Education

{% for edu in site.data.cv.education %}
**{{ edu.period }}**  
**{{ edu.degree }} in {{ edu.major }}**, {{ edu.institution }}  

{% if edu.courses %}
**Courses**
{% for c in edu.courses %}
- {{ c }}
{% endfor %}
{% endif %}

{% endfor %}

---

## Experience

{% for e in site.data.cv.experience %}
**{{ e.period }}**  
**{{ e.title }}**, [{{ e.company }}]({{ e.company_url }})

{{ e.description }}

{% if e.highlights %}
**Highlights**
{% for h in e.highlights %}
- {{ h }}
{% endfor %}
{% endif %}

{% endfor %}


<!-- ## Volunteer

{% for v in site.data.cv.volunteer %}
**{{ v.period }}**  
**{{ v.title }}**, [{{ v.organization }}]({{ v.organization_url }})

{{ v.description }}

{% if v.highlights %}
**Highlights**
{% for h in v.highlights %}
- {{ h }}
{% endfor %}
{% endif %}

{% endfor %}

--- -->



<!-- ---

## Awards

{% for a in site.data.cv.awards %}
**{{ a.date }}**  
**{{ a.title }}**, {{ a.issuer }}

{{ a.description }}

{% endfor %}

---

## Publications

{% for p in site.data.cv.publications %}
**{{ p.date }}**  
**[{{ p.title }}]({{ p.url }})**, {{ p.publisher }}

{{ p.description }}

{% endfor %}

---

## References

{% for r in site.data.cv.references %}
> {{ r.quote }}  
> — *{{ r.name }}*
{% endfor %} -->

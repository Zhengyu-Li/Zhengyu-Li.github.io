---
layout: page
title: Portfolio
description: Time, held loosely.
permalink: /portfolio/
---

<div class="portfolio-tabs" id="portfolio-tabs">
{% for t in site.data.portfolio.themes %}
  <button class="portfolio-tab" data-target="{{ t.id }}">
    {{ t.title }}
  </button>
{% endfor %}
</div>


{% for t in site.data.portfolio.themes %}
<div class="portfolio-section" id="{{ t.id }}" style="display:none">

<p class="note">{{ t.description }}</p>

<div class="grid">
{% for img in t.images %}
  <div class="col-4">
    <figure class="portfolio-item">
        <img src="{{ img.src }}" alt="{{ img.caption }}">
        {% if img.caption %}
        <figcaption class="portfolio-overlay">
            <span class="portfolio-note">{{ img.caption }}</span>
        </figcaption>
    {% endif %}
    </figure>
  </div>
{% endfor %}
</div>

</div>
{% endfor %}

<script>
(function () {
  const tabs = document.querySelectorAll('#portfolio-tabs .portfolio-tab');
  const sections = document.querySelectorAll('.portfolio-section');

  function show(id) {
    sections.forEach(s => s.style.display = s.id === id ? 'block' : 'none');
    tabs.forEach(t => t.classList.toggle('active', t.dataset.target === id));
  }

  tabs.forEach(t => {
    t.addEventListener('click', () => show(t.dataset.target));
  });

  if (tabs.length > 0) show(tabs[0].dataset.target);
})();
</script>

---
layout: default
permalink: /gallery/
title: Gallery
description: Life Beyond the Lab — a personal photo journal, 2023–2026.
nav: true
nav_order: 3
stylesheet: /assets/css/photo-journal.css
images:
  lightbox2: true
---

<article class="photo-journal">
  <header class="journal-header">
    <p class="journal-eyebrow">A personal photo journal <span>2023–2026</span></p>
    <h1>Life Beyond<br>the Lab</h1>
    <div class="journal-intro">
      <p>A few memorable moments with my labmates.</p>
      <nav class="journal-years" aria-label="Browse photos by year">
        {% for year in site.data.gallery %}
          <a href="#year-{{ year.year }}">{{ year.year }}</a>
        {% endfor %}
      </nav>
    </div>
  </header>

{% for year in site.data.gallery %}
{% assign first_year = forloop.first %}

<section class="journal-section" aria-labelledby="year-{{ year.year }}">
<div class="journal-section-heading">
<h2 id="year-{{ year.year }}">{{ year.year }}</h2>
<span>{{ year.chapter }}</span>
</div>
<div class="journal-grid">
{% for photo in year.photos %}
{% capture caption %}{{ photo.date }} — {{ photo.title }}. {{ photo.story }}{% endcapture %}
<figure class="journal-photo{% if photo.layout %} journal-photo--{{ photo.layout }}{% endif %}">
<a class="journal-image" href="{{ photo.path | relative_url }}" data-lightbox="life-beyond-the-lab" data-title="{{ caption | strip | escape }}" aria-label="View full photograph: {{ photo.title | escape }}">
<img src="{{ photo.path | relative_url }}" width="{{ photo.width }}" height="{{ photo.height }}" alt="{{ photo.alt | escape }}" {% if first_year and forloop.first %}loading="eager" fetchpriority="high"{% else %}loading="lazy"{% endif %} decoding="async">
<span class="journal-enlarge" aria-hidden="true">View photograph <span>↗</span></span>
</a>
<figcaption>
<time datetime="{{ photo.datetime }}">{{ photo.date }}</time>
<h3>{{ photo.title }}</h3>
<p>{{ photo.story }}</p>
</figcaption>
</figure>
{% endfor %}
</div>
</section>
{% endfor %}

  <div class="journal-end"><span>2023–2026</span><a href="#">Back to top ↑</a></div>
</article>

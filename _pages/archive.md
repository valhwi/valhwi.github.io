---
layout: archive
title: Archive
permalink: /archive/
---

<main>
  <div class="gallery">
    {% for i in (1..45) %}
      <div class="gallery-item">
        <img src="{{ '/images/' | append: i | append: '.jpg' | relative_url }}" alt="Photo {{ i }}">
      </div>
    {% endfor %}
  </div>
</main>

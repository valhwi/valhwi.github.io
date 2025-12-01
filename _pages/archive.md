---
layout: archive
title: Archive
permalink: /archive/
author_profile: false
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

<style>
.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}

.gallery-item img {
  width: 200px; /* adjust size as needed */
  height: 200px;
  object-fit: cover;
  filter: grayscale(100%);
  transition: filter 0.3s ease, transform 0.3s ease;
  border-radius: 10px; /* rounded corners */
}

.gallery-item img:hover {
  filter: grayscale(0%);
  transform: scale(1.05); /* optional zoom effect on hover */
}
</style>

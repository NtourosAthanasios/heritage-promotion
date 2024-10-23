---
layout: page
title: POIs List
permalink: /pois/

---

<div class="pois-container">
  {% for p in site.pois %}
    <div class="poi-box">
      <a href="{{ p.url | relative_url }}">
        <h3>{{ p.title }}</h3>
        <p>{{ p.description }}</p> <!-- Αν έχετε περιγραφή -->
      </a>
    </div>
  {% endfor %}
</div>





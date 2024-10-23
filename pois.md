---
layout: page
title: POIs List
permalink: /pois/

---

<div class="pois-container">
  {% for p in site.pois %}
    <div class="poi-box">
      <a href="{{ p.url | relative_url }}">
         {% if poi.image %}
          <img src="/heritage-promotion{{ poi.image }}" alt="/heritage-promotion{{ poi.title }} image"/>
        {% endif %}
        <h3>{{ p.title }}</h3>
        <p>{{ p.description }}</p>
      </a>
    </div>
  {% endfor %}
</div>

<style>
.pois-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 20px; 
}

.poi-box {
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  border-radius: 8px; 
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  margin: 10px; 
  padding: 15px; 
  width: 30%; 
  transition: transform 0.3s ease, box-shadow 0.3s ease; 
}

.poi-box:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

</style>




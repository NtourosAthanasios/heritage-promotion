---
layout: page
title: POIs List
permalink: /pois/

---

<div class="pois-container">
  {% for p in site.pois %}
    <div class="poi-box">
      <a href="{{ p.url | relative_url }}">
        <img src="{{ p.image | relative_url }}" alt="{{ p.title }}" class="poi-image"> <!-- Display the image -->
        <h3>{{ p.title }}</h3>
        <p>{{ p.description }}</p>
      </a>
    </div>
  {% endfor %}
</div>

<style>
.pois-container {
  display: flex;
  flex-wrap: wrap; /* Να επιτρέπεται η αλλαγή γραμμών */
  justify-content: space-around; /* Ισομερή διάταξη */
  padding: 20px; /* Εσωτερικό περιθώριο */
}

.poi-box {
  background-color: #f0f0f0; /* Χρώμα φόντου */
  border: 1px solid #ccc; /* Περιθώριο */
  border-radius: 8px; /* Στρογγυλεμένες γωνίες */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Σκιά */
  margin: 10px; /* Εξωτερικό περιθώριο */
  padding: 15px; /* Εσωτερικό περιθώριο */
  width: 30%; /* Πλάτος του box */
  transition: transform 0.3s ease, box-shadow 0.3s ease; /* Μετάβαση για hover effect */
}

.poi-box:hover {
  transform: scale(1.05); /* Μεγέθυνση στο hover */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* Αυξημένη σκιά στο hover */
}

.poi-box a {
  text-decoration: none; /* Αφαίρεση υπογράμμισης */
  color: #333; /* Χρώμα κειμένου */
}

.poi-box h3 {
  margin: 0 0 10px; /* Περιθώριο κάτω */
}

.poi-box p {
  margin: 0; /* Μηδενικό περιθώριο */
}
</style>




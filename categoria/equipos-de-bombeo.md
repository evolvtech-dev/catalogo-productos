---
layout: default
title: Equipos de bombeo
permalink: /categoria/equipos-de-bombeo/
---

# Equipos de bombeo

{% assign items = site.products | where: "category", "equipos-de-bombeo" %}

<div class="products-grid">
  {% for p in items %}
    <a class="product-card" href="{{ p.url | relative_url }}">
      <div class="product-image">
        <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
      </div>
      <div class="product-body">
        <h3>{{ p.title }}</h3>
        <p>{{ p.summary }}</p>
      </div>
    </a>
  {% endfor %}
</div>

{% if items == empty %}
<p>No hay productos en esta categoría todavía.</p>
{% endif %}

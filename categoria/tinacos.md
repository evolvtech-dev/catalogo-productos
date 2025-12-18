---
layout: default
title: Tinacos
permalink: /categoria/tinacos/
---

# Tinacos

{% assign items = site.products | where: "market", "Tinacos" %}

<div class="products-grid">
  {% for p in items %}
    <a class="product-card" href="{{ p.url | relative_url }}">
      <div class="product-image">
        <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
      </div>
      <div class="product-body">
        <h3>{{ p.title }}</h3>
        <p>{{ p.summary }}</p>
        <div class="product-meta">
          {% if p.badge %}<span class="badge">{{ p.badge }}</span>{% endif %}
          {% if p.category %}<span class="badge badge-soft">{{ p.category }}</span>{% endif %}
        </div>
      </div>
    </a>
  {% endfor %}
</div>

{% if items == empty %}
<p>No hay productos en esta categoría todavía.</p>
{% endif %}

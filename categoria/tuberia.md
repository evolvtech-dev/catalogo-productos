---
layout: default
title: Tubería
permalink: /categoria/tuberia/
---

# Tubería

{% assign slug = "tuberia" %}
{% assign items = "" | split: "" %}

{% for p in site.products %}
  {% assign m = p.market | default: "" | downcase
    | replace:'á','a' | replace:'é','e' | replace:'í','i' | replace:'ó','o' | replace:'ú','u' | replace:'ñ','n'
    | replace:' ','-' | replace:'&','y' | replace:'/','-' %}
  {% if m == slug %}
    {% assign items = items | push: p %}
  {% endif %}
{% endfor %}

{% assign items = items | sort: "order" %}

<div class="products-grid">
  {% for p in items %}
    <a class="product-card" href="{{ p.url | relative_url }}">
      <div class="product-image"><img src="{{ p.image | relative_url }}" alt="{{ p.title | replace: '"', '' }}"></div>
      <div class="product-body">
        <h3>{{ p.title | replace: '"', '' }}</h3>
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

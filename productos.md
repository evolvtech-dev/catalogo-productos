---
layout: default
title: "Catálogo de productos"
permalink: /productos/
---

<section class="hero">
  <h1>Catálogo de productos</h1>
  <p class="lead">Consulta nuestras soluciones organizadas por industria y categoría. Todos los productos incluyen ficha técnica e imagen.</p>
</section>

<!-- FILTROS POR INDUSTRIA (mercado) -->
<section style="margin-top:24px">
  <h2>Industrias que atendemos</h2>
  <div style="display:flex;flex-wrap:wrap;gap:12px;margin-top:12px">
    {% assign industrias = site.products | map: "market" | uniq | sort %}
    {% for m in industrias %}
      {% if m %}
      <a href="#{{ m | slugify }}" class="button">{{ m }}</a>
      {% endif %}
    {% endfor %}
  </div>
</section>

<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<!-- PRODUCTOS AGRUPADOS POR INDUSTRIA -->
{% assign mercados = site.products | map: "market" | uniq | sort %}
{% for mercado in mercados %}
  {% if mercado %}
  <section id="{{ mercado | slugify }}" style="margin-bottom:48px">
    <h2>{{ mercado }}</h2>
    {% assign categorias = site.products | where: "market", mercado | map: "category" | uniq | sort %}
    {% for cat in categorias %}
      {% assign items = site.products | where: "market", mercado | where: "category", cat %}
      <h3 id="{{ cat | slugify }}">{{ cat }}</h3>
      <div class="grid">
        {% for p in items %}
        <article class="card">
          <a class="card-media" href="{{ p.url | relative_url }}">
            {% if p.image %}
            <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
            {% endif %}
          </a>
          <div class="card-body">
            <h3 class="card-title"><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
            {% if p.summary %}<p class="card-text">{{ p.summary }}</p>{% endif %}
            <a class="button" href="{{ p.url | relative_url }}">Ver detalles</a>
          </div>
        </article>
        {% endfor %}
      </div>
    {% endfor %}
  </section>
  {% endif %}
{% endfor %}

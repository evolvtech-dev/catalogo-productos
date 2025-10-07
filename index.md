---
layout: default
title: "Inicio"
---

<!-- HERO PRINCIPAL -->
<section class="hero">
  <h1>Comercializadora de Plásticos Potosina</h1>
  <p class="lead">Catálogo informativo de soluciones y productos plásticos con fichas técnicas e imágenes.</p>
</section>

<!-- SECCIÓN DE PRODUCTOS -->
<section id="productos">
  <h2>Productos</h2>
  <div class="grid">
    {% assign productos = site.products | sort: 'order' %}
    {% for p in productos %}
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
</section>

<!-- SECCIÓN DE MARCAS -->
<hr style="border:0;border-top:1px solid var(--border);margin:28px 0">

<section id="marcas">
  <h2>Marcas que distribuimos</h2>
  <p class="lead">Trabajamos con fabricantes líderes para garantizar calidad, disponibilidad y respaldo técnico.</p>

  <div class="brand-grid" style="display:grid;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));gap:16px;align-items:center">
    <div class="brand-card"><img alt="Oatey" src="{{ '/assets/images/marcas/oatey.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="Spears" src="{{ '/assets/images/marcas/spears.jpg' | relative_url }}"></div>
    <div class="brand-card"><img alt="Cepex" src="{{ '/assets/images/marcas/cepex.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="GF" src="{{ '/assets/images/marcas/gf.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="Garlock" src="{{ '/assets/images/marcas/garlock.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="PCP" src="{{ '/assets/images/marcas/pcp.webp' | relative_url }}"></div>
    <div class="brand-card"><img alt="Tecno Plastic" src="{{ '/assets/images/marcas/tecno-plastic.png' | relative_url }}"></div>
    <div class="brand-card"><img alt="Serrot" src="{{ '/assets/images/marcas/serrot.jpg' | relative_url }}"></div>
  </div>
</section>

<!-- CTA FINAL -->
<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section class="cta" style="padding:24px;border:1px solid var(--border);border-radius:18px;background:linear-gradient(135deg,var(--brand),var(--brand-2));color:#0b0f19">
  <h2 style="margin:0 0 8px">¿Necesitas una cotización?</h2>
  <p style="margin:0 0 12px">Contáctanos para recibir asesoría y el catálogo completo de productos.</p>
  <div style="display:flex;gap:12px;flex-wrap:wrap">
    <a class="button" href="mailto:contacto@ctp.mx?subject=Cotización%20Catálogo%20CTP">Solicitar por correo</a>
    <a class="button" href="https://wa.me/524421234567" target="_blank" rel="noopener">WhatsApp</a>
  </div>
</section>

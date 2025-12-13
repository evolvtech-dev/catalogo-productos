---
layout: default
title: "Inicio"
---

<!-- HERO PRINCIPAL -->
<section class="hero">
  <h1>Comercializadora de Plásticos Potosina</h1>
  <p class="lead">Catálogo informativo de soluciones y productos plásticos industriales.</p>
</section>

<!-- SECCIÓN DE CATEGORÍAS -->
<section id="categorias">
  <h2>Categorías de productos</h2>
  <div class="grid">
    {% assign categorias = site.products | map: "category" | uniq | sort %}
    {% for cat in categorias %}
      {% assign prod = site.products | where: "category", cat | first %}
      {% if prod %}
      <article class="card">
        <a class="card-media" href="{{ '/categoria/' | append: cat | slugify | append: '/' | relative_url }}">
          {% if prod.image %}
          <img src="{{ prod.image | relative_url }}" alt="{{ cat }}">
          {% endif %}
        </a>
        <div class="card-body">
          <h3 class="card-title">{{ cat }}</h3>
          <p class="card-text">Ver productos de {{ cat | downcase }}.</p>
          <a class="button" href="{{ '/categoria/' | append: cat | slugify | append: '/' | relative_url }}">Explorar</a>
        </div>
      </article>
      {% endif %}
    {% endfor %}
  </div>
</section>

<!-- CTA FINAL -->
<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">
<section class="cta cta--pro" style="padding:28px;border:1px solid var(--border);border-radius:22px;background:linear-gradient(135deg,var(--panel),#0c1326);">
  <h2 style="margin:0 0 12px">¿Listo para cotizar?</h2>
  <p class="lead" style="margin:0 0 16px;color:var(--muted)">Contáctanos y recibe atención personalizada para tus proyectos industriales.</p>
  <div style="display:flex;gap:12px;flex-wrap:wrap">
    <a class="button" href="mailto:ventas@ctpslp.com.mx?subject=Cotización%20Catálogo%20CTP">Enviar correo</a>
    <a class="button" href="https://wa.me/524447142939" target="_blank" rel="noopener">WhatsApp</a>
    <a class="button" href="tel:4444594310">Llamar ahora</a>
  </div>
</section>

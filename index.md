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

<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="beneficios">
  <h2>¿Por qué elegir Comercializadora de Plásticos Potosina?</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:24px;margin-top:16px">
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Amplio catálogo</h3>
      <p>Ofrecemos soluciones plásticas de marcas líderes en el mercado, con disponibilidad inmediata.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Asesoría técnica</h3>
      <p>Nuestro equipo te ayuda a elegir el producto correcto según tu aplicación y requerimiento industrial.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Experiencia comprobada</h3>
      <p>Más de 15 años de trayectoria atendiendo a los sectores industrial, agrícola, minero y de construcción.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Envíos a todo México</h3>
      <p>Contamos con logística nacional y alianzas para entregas rápidas y seguras.</p>
    </div>
  </div>
</section>

<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="aplicaciones">
  <h2>Aplicaciones</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:24px;margin-top:16px">
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Agua y saneamiento</h3>
      <p>Sistemas de conducción de agua, drenaje, riego agrícola y plantas de tratamiento.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Química e industrial</h3>
      <p>Procesos químicos, manejo de fluidos corrosivos y líneas de producción.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Construcción</h3>
      <p>Instalaciones hidráulicas y sanitarias con materiales certificados de alta durabilidad.</p>
    </div>
    <div style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <h3>Minería y energía</h3>
      <p>Aplicaciones en drenaje de químicos, floculación y conducción de agua en minería.</p>
    </div>
  </div>
</section>

<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="testimonios">
  <h2>Nuestros clientes opinan</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:24px;margin-top:16px">
    <blockquote style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <p>“Siempre recibimos asesoría técnica rápida y productos en tiempo. ¡Un excelente servicio!”</p>
      <footer style="color:var(--muted)">— Cliente industrial, Querétaro</footer>
    </blockquote>
    <blockquote style="background:var(--card);padding:20px;border-radius:16px;border:1px solid var(--border)">
      <p>“Material de primera calidad. Hemos sustituido tuberías metálicas por plásticas con excelentes resultados.”</p>
      <footer style="color:var(--muted)">— Proveedor de construcción</footer>
    </blockquote>
  </div>
</section>


<!-- CTA FINAL -->
<hr style="border:0;border-top:1px solid var(--border);margin:32px 0">

<section id="contacto" class="cta cta--pro"
  style="position:relative;overflow:hidden;padding:28px;border:1px solid var(--border);border-radius:22px;background:radial-gradient(1200px 400px at -10% -30%, rgba(79,70,229,.35), transparent 60%), radial-gradient(1200px 400px at 110% 130%, rgba(34,211,238,.35), transparent 60%), linear-gradient(135deg,var(--panel),#0c1326);">
  <div style="position:absolute;inset:-2px;border-radius:24px;pointer-events:none;box-shadow:0 0 120px rgba(79,70,229,.25),0 0 120px rgba(34,211,238,.25) inset;"></div>

  <header style="display:flex;align-items:center;gap:12px;margin-bottom:12px">
    <!-- Icono carta (correo) -->
    <svg width="28" height="28" viewBox="0 0 24 24" fill="none" aria-hidden="true">
      <path d="M3 7a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v10a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V7Z" stroke="url(#g1)" stroke-width="1.6"/>
      <path d="M4 7l8 6 8-6" stroke="url(#g2)" stroke-width="1.6" fill="none"/>
      <defs>
        <linearGradient id="g1" x1="0" y1="0" x2="1" y2="1">
          <stop stop-color="#22d3ee"/><stop offset="1" stop-color="#4f46e5"/>
        </linearGradient>
        <linearGradient id="g2" x1="0" y1="0" x2="1" y2="1">
          <stop stop-color="#22d3ee"/><stop offset="1" stop-color="#4f46e5"/>
        </linearGradient>
      </defs>
    </svg>
    <h2 style="margin:0">Contáctanos</h2>
  </header>

  <p class="lead" style="margin:0 0 16px;color:var(--muted)">
    Estamos listos para asesorarte y brindarte una cotización personalizada.
  </p>

  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:12px;margin-bottom:18px">
    <div class="contact-item" style="display:flex;align-items:center;gap:10px;background:var(--card);border:1px solid var(--border);border-radius:14px;padding:12px">
      <!-- Icono teléfono -->
      <svg width="22" height="22" viewBox="0 0 24 24" fill="none" aria-hidden="true">
        <path d="M6.6 4h2.2l1.4 3.2-1.6 1.2a12.5 12.5 0 0 0 6 6l1.2-1.6L19.9 15v2.2c0 .9-.7 1.6-1.6 1.6A14.9 14.9 0 0 1 4 6.6C4 5.7 4.7 5 5.6 5H6.6Z" stroke="currentColor" stroke-width="1.6"/>
      </svg>
      <p style="margin:0"><strong>Teléfono:</strong> <a href="tel:4444594310">444 459 4310</a></p>
    </div>

    <div class="contact-item" style="display:flex;align-items:center;gap:10px;background:var(--card);border:1px solid var(--border);border-radius:14px;padding:12px">
      <!-- Icono WhatsApp -->
      <svg width="22" height="22" viewBox="0 0 24 24" fill="none" aria-hidden="true">
        <path d="M20.5 11a8.5 8.5 0 1 1-16.7 2.7L3 21l7.5-1.9A8.5 8.5 0 1 1 20.5 11Z" stroke="#22d3ee" stroke-width="1.4"/>
        <path d="M9.5 8.8c0 3.2 3.5 5.7 4.9 5.7.5 0 1.3-.4 1.5-.9l.6-1.3-2-.7-.9.8c-1.2-.4-2.5-1.7-2.9-2.9l.8-.9-.7-2-.9.6c-.5.3-.9 1-.9 1.6Z" fill="#22d3ee"/>
      </svg>
      <p style="margin:0"><strong>WhatsApp:</strong> <a href="https://wa.me/524447142939" target="_blank" rel="noopener">444 714 2939</a></p>
    </div>

    <div class="contact-item" style="display:flex;align-items:center;gap:10px;background:var(--card);border:1px solid var(--border);border-radius:14px;padding:12px">
      <!-- Icono mail -->
      <svg width="22" height="22" viewBox="0 0 24 24" fill="none" aria-hidden="true">
        <path d="M3.3 6.5h17.4v11H3.3v-11Z" stroke="currentColor" stroke-width="1.4"/>
        <path d="M4 7l8 6 8-6" stroke="currentColor" stroke-width="1.4"/>
      </svg>
      <p style="margin:0"><strong>Correo:</strong> <a href="mailto:ventas@ctpslp.com.mx">ventas@ctpslp.com.mx</a></p>
    </div>
  </div>

  <div style="display:flex;gap:12px;flex-wrap:wrap">
    <a class="button" href="mailto:ventas@ctpslp.com.mx?subject=Cotización%20Catálogo%20CTP">Enviar correo</a>
    <a class="button" href="https://wa.me/524447142939" target="_blank" rel="noopener">Chatear por WhatsApp</a>
    <a class="button" href="tel:4444594310">Llamar ahora</a>
  </div>
</section>



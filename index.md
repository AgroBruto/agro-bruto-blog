---
layout: default
title: "Home"
---

# 🌾 Agro Bruto
## Horizonte Agro Bruto 720°

### Inteligência Estratégica para o Agronegócio

O **Agro Bruto** é seu hub de análise e inteligência para o agronegócio brasileiro e sul-americano. Acompanhamos os movimentos que moldam o presente e o futuro do setor.

## 🔍 Nossas Especialidades

<div class="specialties-grid">
  <div class="specialty-card">
    <h3>🚂 Radar Logístico</h3>
    <p>Infraestrutura, ferrovias e corredores logísticos</p>
    <a href="{{ site.baseurl }}/radar-logistico">Explorar →</a>
  </div>
  
  <div class="specialty-card">
    <h3>🌍 Geopolítica Global</h3>
    <p>Mercados internacionais e acordos comerciais</p>
    <a href="{{ site.baseurl }}/geopolitica">Explorar →</a>
  </div>
  
  <div class="specialty-card">
    <h3>📈 Inteligência de Mercado</h3>
    <p>Commodities, preços e análise econômica</p>
    <a href="{{ site.baseurl }}/mercado">Explorar →</a>
  </div>
</div>

## 📊 Últimas Análises

{% for post in site.posts limit:3 %}
<article class="post-preview">
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <div class="post-meta">
    <span class="date">{{ post.date | date: "%d/%m/%Y" }}</span>
    <span class="category">{{ post.category }}</span>
  </div>
  <p>{{ post.excerpt }}</p>
</article>
{% endfor %}

<a href="{{ site.baseurl }}/posts" class="view-all">Ver todas as análises →</a>

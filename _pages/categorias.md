---
layout: page
title: "Categorias"
permalink: /categorias/
---

# Nossas Especialidades

{% for category in site.data.categories %}
<div class="category-card" style="border-left: 4px solid {{ category.color }}; padding: 1.5rem; margin: 2rem 0; background: #f8f9fa;">
    <h2>{{ category.title }}</h2>
    <p>{{ category.description }}</p>
    
    {% assign category_posts = site.posts | where: "category", category.name %}
    <p><strong>{{ category_posts.size }} posts publicados</strong></p>
    
    {% if category_posts.size > 0 %}
    <h4>Últimos Posts:</h4>
    <ul>
    {% for post in category_posts limit: 3 %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%d/%m/%Y" }}</li>
    {% endfor %}
    </ul>
    
    <a href="{{ "/categoria/" | append: category.name | relative_url }}" class="btn">Ver todos os posts →</a>
    {% endif %}
</div>
{% endfor %}

---
layout: page
title: "Arquivo"
permalink: /arquivo/
---

# Arquivo de Posts

## Posts por Ano

### 2025

{% assign posts_2025 = site.posts | where_exp: "post", "post.date contains '2025'" %}
{% for post in posts_2025 %}
- **{{ post.date | date: "%d/%m" }}** - [{{ post.title }}]({{ post.url | relative_url }}) *{{ post.category }}*
{% endfor %}

### 2024

{% assign posts_2024 = site.posts | where_exp: "post", "post.date contains '2024'" %}
{% for post in posts_2024 %}
- **{{ post.date | date: "%d/%m" }}** - [{{ post.title }}]({{ post.url | relative_url }}) *{{ post.category }}*
{% endfor %}

## Posts por Categoria

{% for category in site.data.categories %}
### {{ category.title }}

{% assign category_posts = site.posts | where: "category", category.name %}
{% for post in category_posts limit: 5 %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%d/%m/%Y" }}
{% endfor %}

{% if category_posts.size > 5 %}
[Ver todos os posts de {{ category.title }}]({{ "/categoria/" | append: category.name | relative_url }})
{% endif %}

{% endfor %}

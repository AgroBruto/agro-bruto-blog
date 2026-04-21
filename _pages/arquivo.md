---
layout: page
title: "Arquivo"
permalink: /arquivo/
---

# Arquivo de Posts

## Posts por Ano

### 2026

{% assign posts_2026 = site.posts | where_exp: "post", "post.date contains '2026'" %}
{% for post in posts_2026 %}
- **{{ post.date | date: "%d/%m" }}** - [{{ post.title }}]({{ post.url | relative_url }}) *{{ post.category }}*
{% endfor %}

### 2025

{% assign posts_2025 = site.posts | where_exp: "post", "post.date contains '2025'" %}
{% for post in posts_2025 %}
- **{{ post.date | date: "%d/%m" }}** - [{{ post.title }}]({{ post.url | relative_url }}) *{{ post.category }}*
{% endfor %}

## Posts por Categoria

{% for category in site.data.categories %}
### {{ category.title }}

{% assign category_posts = site.posts | where: "category", category.name %}
{% for post in category_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%d/%m/%Y" }}
{% endfor %}

{% endfor %}

---
layout: default
title: Dataset Literário
---
<head><link rel="icon" href="{{ '/favicon.png' | relative_url }}" type="image/x-icon"></head>

<img src="{{ '/assets/images/logo.png' | relative_url }}"  alt="Logo" style="max-width: 200px;"/>

# Bem-vindo ao Dataset Literário

Cada livro é um registro.

Leitura ativa é uma query: busca temas, padrões e relações.

📚 Dataset em expansão: clássicos, contemporâneos, não-ficção... e alguns outliers.

---

{% for post in site.posts %}
- 📖 _{{ post.date | date: "%d/%m/%Y" }}_ — [{{ post.title }}]({{ post.url | relative_url  }}) — {{ post.author }} — {{ post.my_rating }}★
{% endfor %}

---

<!--
<strong>Filtrar por tags:</strong>
{% assign tag_list = site.posts | map: "tags" | join: "," | split: "," | uniq | sort_natural %}
{% for tag in tag_list %}
  <a href="/tags/{{ tag | slugify }}">{{ tag }}</a>
{% endfor %}
-->
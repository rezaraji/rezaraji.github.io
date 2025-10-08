---
layout: default
title: Projects
---

# 👋 Hi, I’m Reza

Welcome to my portfolio — a showcase of projects I’ve built and explored over time.

## 🚧 Projects

<ul class="cards">
{% assign sorted = site.projects | sort: 'date' | reverse %}
{% for p in sorted %}
  <li class="card">
    <a href="{{ p.url | relative_url }}">
      {% if p.cover %}
        <img src="{{ p.cover | relative_url }}" alt="{{ p.title }} cover" />
      {% endif %}
      <h3>{{ p.title }}</h3>
      <p>{{ p.summary }}</p>
      <p class="meta">
        {% if p.year %}{{ p.year }}{% endif %}
        {% if p.tags %} · {{ p.tags | join: ", " }}{% endif %}
      </p>
    </a>
    <p class="links">
      {% if p.repo %}<a href="{{ p.repo }}">Code</a>{% endif %}
      {% if p.demo %} · <a href="{{ p.demo }}">Live</a>{% endif %}
    </p>
  </li>
{% endfor %}
</ul>

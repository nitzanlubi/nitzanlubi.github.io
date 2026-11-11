---
permalink: /media/
title: "Media"
classes: wide
---

<div class="media-grid">
{% for item in site.data.media %}
  <div class="media-tile">
    <h3>{{ item.outlet }}</h3>
    {% if item.url != "" %}<a class="media-card" href="{{ item.url }}" target="_blank" rel="noopener">{% else %}<div class="media-card">{% endif %}
      {% if item.image != "" %}<img src="{{ item.image | escape }}" alt="{{ item.outlet }}: {{ item.title | escape }}" referrerpolicy="no-referrer">{% else %}<div class="media-noimage">{{ item.title }}</div>{% endif %}
      <div class="media-caption">{{ item.title }}<span class="media-date">{{ item.date }}</span></div>
    {% if item.url != "" %}</a>{% else %}</div>{% endif %}
  </div>
{% endfor %}
</div>

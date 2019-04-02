---
title: _writing (list)
subtitle:
description: A plain list with all items in the 'writing' category.
featured_image:
---
_{{ page.description }}_

---
2019:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2019" %}
["{{ post.title }}"]({{ post.url }})  
Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}
---
2018:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2018" %}
["{{ post.title }}"]({{ post.url }})  
Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}
---
2017:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2017" %}
["{{ post.title }}"]({{ post.url }})  
Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}
---
2014:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2014" %}
["{{ post.title }}"]({{ post.url }})  
Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}
---
2013:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2013" %}
["{{ post.title }}"]({{ post.url }})  
Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}

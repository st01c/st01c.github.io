---
title: _talks
subtitle: a selection of talks and guest lectures available to stream online
description: A list with selected items in the _talks category.
featured_image:
---

2025:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2025" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---
2024:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2024" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---
2023:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2023" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---
2022:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2022" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---
2021:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2021" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---
2020:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2020" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---
2019:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2019" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---
2018:
{% for post in site.posts %}
  {% if post.category == "talk" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2018" %}
**{{ post.title }}** [&#8618;]({{ post.url }}) <br>
{{ post.date | date: "%a %d %b" }} -- {{ post.venue }} -- {{ post.type }} <br> tags: {{ post.tagz }}
      {% endif %}
  {% endif %}
{% endfor %}
---

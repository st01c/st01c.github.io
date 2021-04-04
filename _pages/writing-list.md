---
title: _writing
subtitle:
description: A plain list with all items in the _writing category.
featured_image:
---

2021:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2021" %}
**"{{ post.title }}"** [&#8618;]({{ post.url }}) <br>
_{{ post.publication }}_ -- {{post.type}} <br> >{{ post.tagz }}<
      {% endif %}
  {% endif %}
{% endfor %}
---
2020:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2020" %}
**"{{ post.title }}"** [&#8618;]({{ post.url }}) <br>
_{{ post.publication }}_ -- {{post.type}} <br> >{{ post.tagz }}<
      {% endif %}
  {% endif %}
{% endfor %}
---
2019:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2019" %}
**"{{ post.title }}"** [&#8618;]({{ post.url }}) <br>
_{{ post.publication }}_ -- {{post.type}} <br> >{{ post.tagz }}<
      {% endif %}
  {% endif %}
{% endfor %}
---
2018:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2018" %}
**"{{ post.title }}"** [&#8618;]({{ post.url }}) <br>
_{{ post.publication }}_ -- {{post.type}} <br> >{{ post.tagz }}<
      {% endif %}
  {% endif %}
{% endfor %}
---
2017:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2017" %}
**"{{ post.title }}"** [&#8618;]({{ post.url }}) <br>
_{{ post.publication }}_ -- {{post.type}} <br> >{{ post.tagz }}<
      {% endif %}
  {% endif %}
{% endfor %}
---
2014:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2014" %}
**"{{ post.title }}"** [&#8618;]({{ post.url }}) <br>
_{{ post.publication }}_ -- {{post.type}} <br> >{{ post.tagz }}<
      {% endif %}
  {% endif %}
{% endfor %}
---
2013:
{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2013" %}
**"{{ post.title }}"** [&#8618;]({{ post.url }}) <br>
_{{ post.publication }}_ -- {{post.type}} <br> >{{ post.tagz }}<
      {% endif %}
  {% endif %}
{% endfor %}
---

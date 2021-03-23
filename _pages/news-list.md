---
title: _news (list)
subtitle:
description: A plain list with all items in the 'news' category.
featured_image:
---


{% assign var01 = "now" | date: "%Y" %}
print contents of variable: {{ var01 }}

/turn var01 into a number/
{% assign var01 = var01 | plus: 0 %}
print var01 -2


{% assign my_variable = false %}
{% if my_variable != true %}
  This statement is valid.
{% endif %}


This page was last updated at {{ "now" | date: "%Y-%m-%d %H:%M" }}.





type conversion test:

to convert a string to a number just add 0 to the variable:

{% assign var01 = var01 | plus:0 %}

Not super elegant but it works!

{% decrement var01 %}
Print decremented variable {{ var01 }}


==

create date number:

{% assign current_year_num = "now" | date: "%Y" | times: 365 %}
{% assign current_month_num = "now" | date: "%m" | times: 30 %}
{% assign current_day_num = "now" | date: "%d" | plus: 0 %}
{% assign current_date_num = current_year_num | plus: current_month_num | plus: current_day_num %}

{{ current_date_num }}



==




<!-- grap current date, extract the year, make it a number, minus 3 -->

<!-- {{ "now" | date: "%Y" | plus: 0 | minus: 3 }} -->



<!-- this is working! -->

{% assign ago = "now" | date: "%Y" | plus: 0 | minus: 3 %}

Print the ago variable: {{ ago }}

{% if ago > 2017 %}
  {{ "YES!" }}
{% else %}
  {{ "NO!" }}
{% endif %}


{% assign month = "now" | date:"%m" | plus: 0 %}
Print month: {{ month }}

============

FINAL BIG TEST (with day numbers)

{% assign current_year_num = "now" | date: "%Y" | times: 365 %}
{% assign current_month_num = "now" | date: "%m" | times: 30 %}
{% assign current_day_num = "now" | date: "%d" | plus: 0 %}
{% assign current_date_num = current_year_num | plus: current_month_num | plus: current_day_num %}


_ffuture:

{% for post in site.posts %}
      {% assign post_year_num = post.date | date: "%Y" | times: 365 %}
      {% assign post_month_num = post.date | date: "%m" | times: 30 %}
      {% assign post_day_num = post.date | date: "%d" | plus: 0 %}
      {% assign current_post_date_num = post_year_num | plus: post_month_num | plus: post_day_num %}
      {% if current_post_date_num > current_date_num %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}

---

_ccurrent:

{% for post in site.posts %}
      {% assign post_year_num = post.date | date: "%Y" | times: 365 %}
      {% assign post_month_num = post.date | date: "%m" | times: 30 %}
      {% assign post_day_num = post.date | date: "%d" | plus: 0 %}
      {% assign current_post_date_num = post_year_num | plus: post_month_num | plus: post_day_num %}
      {% assign recent_date_limit = current_date_num | minus: 180 %}
      {% if current_post_date_num >= recent_date_limit %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}

---

_ppast:

{% for post in site.posts %}
      {% assign post_year_num = post.date | date: "%Y" | times: 365 %}
      {% assign post_month_num = post.date | date: "%m" | times: 30 %}
      {% assign post_day_num = post.date | date: "%d" | plus: 0 %}
      {% assign current_post_date_num = post_year_num | plus: post_month_num | plus: post_day_num %}
      {% assign past_date_limit = current_date_num | minus: 180 %}
      {% if current_post_date_num < past_date_limit %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}







BIG TEST:

_future:

{% assign current_year = "now" | date: "%Y" | plus: 0 %}
{% assign current_month = "now" | date: "%m" | plus: 0 %}
{% assign current_day = "now" | date: "%d" | plus: 0 %}

{% for post in site.posts %}
      {% assign post_year = post.date | date: "%Y" | plus: 0 %}
      {% assign post_month = post.date | date: "%m" | plus: 0 %}
      {% assign post_day = post.date | date: "%d" | plus: 0 %}
      {% if post_year >= current_year and post_month >= current_month and post_day > current_day %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}

---

_current:

{% assign current_year = "now" | date: "%Y" | plus: 0 %}
{% assign current_month = "now" | date: "%m" | plus: 0 %}
{% assign current_month_lower_limit = "now" | date: "%m" | plus: 0 | minus: 6%}
{% assign current_day = "now" | date: "%d" | plus: 0 %}

{% for post in site.posts %}
      {% assign post_year = post.date | date: "%Y" | plus: 0 %}
      {% assign post_month = post.date | date: "%m" | plus: 0 %}
      {% assign post_day = post.date | date: "%d" | plus: 0 %}
      {% if post_year == current_year and post_month > current_month_lower_limit and post_month <= current_month and post_day < current_day %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}

---

_past:

{% assign current_year = "now" | date: "%Y" | plus: 0 %}
{% assign current_month = "now" | date: "%m" | plus: 0 %}
{% assign current_month_lower_limit = "now" | date: "%m" | plus: 0 | minus: 6%}
{% assign current_day = "now" | date: "%d" | plus: 0 %}

{% for post in site.posts %}
      {% assign post_year = post.date | date: "%Y" | plus: 0 %}
      {% assign post_month = post.date | date: "%m" | plus: 0 %}
      {% assign post_day = post.date | date: "%d" | plus: 0 %}
      {% if post_year == current_year and post_month > current_month_lower_limit and post_month <= current_month and post_day < current_day %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}




---

{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2018" %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date_to_long_string }} // Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}

---

_less new:

{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == var01-2 %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date_to_long_string }} // Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}



---

_new:

{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign current_year = now | date:"%Y" %}
      {% assign year = post.date | date:"%Y" %}
      {% if year >= current_year %}
**"{{ post.title }}"** [Read here]({{ post.url }})
{{ post.date | date_to_long_string }} // Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}
---
_recent:

{% for post in site.posts %}
  {% if post.category == "writing" %}
      {% assign year = post.date | date:"%Y" %}
      {% assign current_year = now | date:"%Y" %}
      {% if year < current_year %}
**"{{ post.title }}"** [Read here]({{ post.url }})
{{ post.date | date_to_long_string }} // Tags: {{ post.tagz }}.
      {% endif %}
  {% endif %}
{% endfor %}
---
2018:
{% for post in site.posts %}
      {% assign year = post.date | date:"%Y" %}
      {% if year == "2018" %}
**"{{ post.title }}"** [Read here]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}
---

---
title: _news
subtitle:
description: A plain list with all items in the 'news' category.
featured_image:
---

<!-- tests


{% assign var01 = "now" | date: "%Y" %}
print contents of variable: {{ var01 }}



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

 -->



<!-- grap current date, extract the year, make it a number, minus 3 -->

<!-- {{ "now" | date: "%Y" | plus: 0 | minus: 3 }} -->



<!-- this is working! -->


<!--

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

-->


<!--

_future:

{% for post in site.posts %}
      {% assign post_year_num = post.date | date: "%Y" | times: 365 %}
      {% assign post_month_num = post.date | date: "%m" | times: 30 %}
      {% assign post_day_num = post.date | date: "%d" | plus: 0 %}
      {% assign current_post_date_num = post_year_num | plus: post_month_num | plus: post_day_num %}
      {% if current_post_date_num > current_date_num %}
**"{{ post.title }}"** [Read]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}

---
-->
_current:

{% for post in site.posts %}
      {% assign post_year_num = post.date | date: "%Y" | times: 365 %}
      {% assign post_month_num = post.date | date: "%m" | times: 30 %}
      {% assign post_day_num = post.date | date: "%d" | plus: 0 %}
      {% assign current_post_date_num = post_year_num | plus: post_month_num | plus: post_day_num %}
      {% assign recent_date_limit = current_date_num | minus: 180 %}
      {% if current_post_date_num >= recent_date_limit %}
**"{{ post.title }}"** [Read]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}

---

_past:

{% for post in site.posts %}
      {% assign post_year_num = post.date | date: "%Y" | times: 365 %}
      {% assign post_month_num = post.date | date: "%m" | times: 30 %}
      {% assign post_day_num = post.date | date: "%d" | plus: 0 %}
      {% assign current_post_date_num = post_year_num | plus: post_month_num | plus: post_day_num %}
      {% assign past_date_limit = current_date_num | minus: 180 %}
      {% if current_post_date_num < past_date_limit %}
**"{{ post.title }}"** [Read]({{ post.url }}) <br>
{{ post.date | date: "%b %d %Y" }} // {{ post.category }} // tags: {{ post.tagz }}
      {% endif %}
{% endfor %}

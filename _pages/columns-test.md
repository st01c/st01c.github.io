---
title: ''
subtitle: ''
description:
featured_image:
---

<!-- works but not used -->

<html>
<head>
<style>
img {
  width: 70%;
}
</style>
</head>
<body>

<div class="row">

 <div class="column">
 <p> Website of Martin Zeilinger, <a href="https://rke.abertay.ac.uk/en/persons/martin-zeilinger"> Senior Lecturer in Computational Arts and Technology</a> at Abertay University in Dundee/Scotland.</p>
 <p> Research and curation in:<br>
  <ul>
      <li>AI art</li>
      <li>art and criticism on/of the blockchain</li>
      <li>intellectual property and cultural ownership issues in digital art</li>
      <li>experimental videogame culture</li>
    </ul>
  </p>
<p> <a href="about">More</a>.</p>
 <hr style="width:70%">
<p> <b>_current:</b><br>
  {% for post in site.posts %}
      {% assign pin_var = post.pinned | plus: 0%}
      {% if pin_var == 1 %}
          <p> <i>{{ post.title }}</i><br> {{ post.date | date: "%b %d %Y" }} ({{ post.category }}) <a href="{{ post.url }}">>></a></p>
      {% endif %}
  {% endfor %}
  <hr style="width:70%">

</p>
</div>
<div class="column">
<p>
<img src="/images/content/tactical-entanglements-cover.jpg" alt="book cover">
</p>
<p> <a href="/blog/tactical-entanglements"> meson press April 2021</a> </p>
<p> Available as paperback and Open Access eBook (PDF) </p>
</div>

</div>

</body>
</html>

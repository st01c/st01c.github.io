---
title: ' '
subtitle:
description:
featured_image:
---

<!-- not used -->

<html>
<head>
<style>
img {
  width: 65%;
}
</style>
</head>
<body>

<div class="row">

 <div class="column">
 <p> &#8598; <b>Research and curation in:</b> <br>
  <ul>
      <li>AI art</li>
      <li>art and criticism on/of the blockchain</li>
      <li>intellectual property & cultural ownership issues in digital art</li>
      <li>experimental videogame culture</li>
    </ul>
  </p>
<p> <a href="https://rke.abertay.ac.uk/en/persons/martin-zeilinger"> Senior Lecturer in Computational Arts and Technology</a> at Abertay University in Dundee/Scotland.</p>
<p> <a href="/about">More...</a></p>
<hr>
<p> <b>_recent and _upcoming:</b><br>
  {% for post in site.posts %}
      {% assign pin_var = post.pinned | plus: 0%}
      {% if pin_var == 1 %}
          <p> '{{ post.title }}'<br> {{ post.date | date: "%b %d %Y" }} -- {{ post.category }} <a href="{{ post.url }}">&#8618;</a></p>
      {% endif %}
  {% endfor %}
  <hr>

</p>
</div>
<div class="column">
<p>
<img src="/images/content/zeilinger-brochure-eng.png" alt="book cover">
</p>
<p> <a href="/blog/tactical-entanglements"> meson press (June 2021)</a> </p>
<p> Available as paperback and Open Access eBook </p>
</div>

</div>

</body>
</html>

---
layout: page
title: Mur dels patrocinadors
category: mur
---

<div class="posts">
  {% for post in site.categories['patrocinadors'] reversed %}
  <div class="post">

    {{ post.content }}
    
    <h2 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>

  </div>
  {% endfor %}
</div>
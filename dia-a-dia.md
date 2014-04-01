---
layout: page
title: Dia a dia
category: mur-diari
---

<div class="posts">
  {% for post in site.categories['general'] %}
  <div class="post">
    
    <h2 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h2>

    <span class="post-date">{{ post.date | date_to_string }}</span>

    {{ post.excerpt }} <p class="text-center"><a href="{{ post.url }}"><i class="fa fa-lg fa-plus-square-o"></i></a></p>

  </div>
  {% endfor %}
</div>
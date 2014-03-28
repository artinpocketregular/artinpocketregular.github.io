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

    {{ post.excerpt }} <p><a href="{{ post.url }}"><i class="fa fa-plus-square-o"></i></a></p>

  </div>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="/page{{paginator.next_page}}">Més vell</a>
  {% else %}
    <span class="pagination-item older">Més vell</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="/">Més nou</a>
    {% else %}
      <a class="pagination-item newer" href="/page{{paginator.previous_page}}">Més nou</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Més nou</span>
  {% endif %}
</div>

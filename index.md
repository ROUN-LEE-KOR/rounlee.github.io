---
layout: home        # 또는 별도 home 레이아웃(_layouts/home.html)을 만들 예정이라면 `home`
title:  "Welcome to RounWorld"
permalink: /
---

<div class="homepage-nav" style="text-align:center; margin-top:3rem;">
  {% for item in site.menu %}
  <div class="nav-item" style="display:inline-block; width:200px; margin:1rem; vertical-align:top;">
    <h2><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
    {% if item.children %}
    <ul style="list-style:none; padding:0;">
      {% for child in item.children %}
      <li><a href="{{ child.url | relative_url }}">{{ child.title }}</a></li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
  {% endfor %}
</div>

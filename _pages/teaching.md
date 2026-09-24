---
layout: page
title: Teaching
permalink: /teaching/
description: 
nav: true
nav_order: 3
---

{% for item in site.data.teaching.teaching %}
<div class="cv-item" style="margin-bottom: 2rem;">
  <div style="display: flex; justify-content: space-between; align-items: baseline;">
    <h3 style="margin: 0;">{{ item.institution }}</h3>
    <span style="font-style: italic; color: #666;">{{ item.location }}</span>
  </div>
  
  {% for role in item.roles %}
  <div style="margin-top: 0.75rem;">
    <div style="display: flex; justify-content: space-between; font-weight: 600;">
      <span>{{ role.title }}</span>
      <span>{{ role.start_date }} – {{ role.end_date }}</span>
    </div>
    <ul style="margin-top: 0.4rem; margin-bottom: 0.8rem;">
      {% for course in role.courses %}
      <li>{{ course }}</li>
      {% endfor %}
    </ul>
  </div>
  {% endfor %}
</div>
{% endfor %}

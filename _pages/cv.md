---
layout: page
title: CV
permalink: /cv/
nav: true
nav_order: 4
description: 
---

<div style="margin-bottom: 2rem; text-align: right;">
  <a href="{{ site.data.cv.cv.pdf_cv_link | relative_url }}" target="_blank" rel="noopener noreferrer" style="font-weight: 600; text-decoration: underline;">
    [Download PDF]
  </a>
</div>

<!-- Summary -->
<h2 style="border-bottom: 1px solid #ddd; padding-bottom: 0.3rem; margin-bottom: 1rem;">Summary</h2>
<div style="margin-bottom: 2rem; font-size: 1.1rem; line-height: 1.6;">
  {{ site.data.cv.cv.summary }}
</div>

<!-- Research Interests -->
<h2 style="border-bottom: 1px solid #ddd; padding-bottom: 0.3rem; margin-bottom: 1rem;">Research Interests</h2>
<div style="margin-bottom: 2rem;">
  <ul style="margin-top: 0.4rem;">
    {% for item in site.data.cv.cv.sections['Research Interests'] %}
    <li style="margin-bottom: 0.4rem;"><strong>{{ item.label }}:</strong> {{ item.details }}</li>
    {% endfor %}
  </ul>
</div>

<!-- Education -->
<h2 style="border-bottom: 1px solid #ddd; padding-bottom: 0.3rem; margin-bottom: 1rem;">Education</h2>
{% for item in site.data.cv.cv.sections['Education'] %}
<div style="margin-bottom: 1.5rem;">
  <div style="display: flex; justify-content: space-between; align-items: baseline;">
    <h3 style="margin: 0; font-size: 1.25rem;">{{ item.institution }}</h3>
    <span style="font-style: italic; color: #666;">{{ item.location }}</span>
  </div>
  
  <div style="margin-top: 0.2rem;">
    <div style="display: flex; justify-content: space-between; font-weight: 600;">
      <span>{{ item.degree }}</span>
      <span>{{ item.start_date }} – {{ item.end_date }}</span>
    </div>
    {% if item.highlights %}
    <ul style="margin-top: 0.4rem; margin-bottom: 0;">
      {% for highlight in item.highlights %}
      <li>{{ highlight }}</li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
</div>
{% endfor %}

<!-- Technical Toolkit -->
<h2 style="border-bottom: 1px solid #ddd; padding-bottom: 0.3rem; margin-bottom: 1rem;">Technical Toolkit</h2>
<div style="margin-bottom: 2rem;">
  <ul style="margin-top: 0.4rem;">
    {% for item in site.data.cv.cv.sections['Technical Toolkit'] %}
    <li style="margin-bottom: 0.4rem;"><strong>{{ item.label }}:</strong> {{ item.details }}</li>
    {% endfor %}
  </ul>
</div>

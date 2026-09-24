---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 2
description: 
---

<!-- Working Papers -->
<h2 style="border-bottom: 1px solid #ddd; padding-bottom: 0.3rem; margin-bottom: 1rem;">Working Papers</h2>
{% for item in site.data.research.working_papers %}
<div style="margin-bottom: 1.5rem;">
  <div style="display: flex; justify-content: space-between; align-items: baseline;">
    <h3 style="margin: 0; font-size: 1.15rem; font-weight: normal;">
      "{{ item.title }}"
      {% if item.coauthors %}
      <span style="font-size: 0.95rem; font-weight: normal; color: #555;">({{ item.coauthors }})</span>
      {% endif %}
    </h3>
    {% if item.pdf %}
    <span>
      <a href="{{ item.pdf | relative_url }}" target="_blank" rel="noopener noreferrer" style="font-weight: 600; text-decoration: underline;">
        [{{ item.status | default: 'Draft' }}]
      </a>
    </span>
    {% endif %}
  </div>
</div>
{% endfor %}

<!-- Publications -->
<h2 style="border-bottom: 1px solid #ddd; padding-bottom: 0.3rem; margin-bottom: 1rem;">Publications</h2>
{% for item in site.data.research.publications %}
<div style="margin-bottom: 1.5rem;">
  <div style="display: flex; justify-content: space-between; align-items: baseline;">
    <h3 style="margin: 0; font-size: 1.15rem; font-weight: normal;">
      "{{ item.title }}"
      {% if item.coauthors %}
      <span style="font-size: 0.95rem; font-weight: normal; color: #555;">({{ item.coauthors }})</span>
      {% endif %}
    </h3>
    <span style="font-style: italic; color: #666;">
      {{ item.journal }}{% if item.year %}, {{ item.year }}{% endif %}
    </span>
  </div>
  {% if item.url %}
  <div style="margin-top: 0.2rem;">
    <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer" style="font-size: 0.9rem; text-decoration: underline;">
      [Publisher Link]
    </a>
  </div>
  {% endif %}
</div>
{% endfor %}

<!-- Work in Progress -->
<h2 style="border-bottom: 1px solid #ddd; padding-bottom: 0.3rem; margin-bottom: 1rem;">Work in Progress</h2>
{% for item in site.data.research.work_in_progress %}
<div style="margin-bottom: 1.5rem;">
  <h3 style="margin: 0 0 0.4rem 0; font-size: 1.15rem; font-weight: normal;">"{{ item.title }}"</h3>
  {% if item.abstract %}
  <p style="margin: 0; font-style: italic; color: #444; line-height: 1.5;">
    {{ item.abstract }}
  </p>
  {% endif %}
</div>
{% endfor %}

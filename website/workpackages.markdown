---
layout: page
title: Workpackages
permalink: /workpackages/
---

<div class="wp-list">
  <!-- Sort mathematically by the number -->
  {% assign sorted_wps = site.workpackages | sort: "number" %}
  
  {% for wp in sorted_wps %}
    <div class="wp-card">
      
      <!-- The Number Logo -->
      <div class="wp-logo">
        WP{{ wp.number }}
      </div>
      
      <!-- The Content -->
      <div class="wp-content">
        <h3>{{ wp.title }}</h3>
        
        {% if wp.leader %}
          <p class="wp-leader"><strong>Lead:</strong> {{ wp.leader }}</p>
        {% endif %}
        
        <div class="wp-description">
          {{ wp.content | markdownify }}
        </div>
      </div>

    </div>
  {% endfor %}
</div>
---
layout: page
title: Publications
permalink: /publications/
---

<div class="publications-list">
  {% assign sorted_pubs = site.publications | sort: "sorting" %}
  
  {% for pub in sorted_pubs %}
    <div class="pub-card">
      
      <h5 class="pub-title">{{ pub.title }}</h5 >
      <p class="pub-author">{{ pub.author }}</p>
      <p class="pub-venue">{{ pub.venue_shortname }}</p>
      
      <!-- The Badges Area -->
      <div class="pub-badges">
        {% if pub.artifact %}
          <a href="{{ pub.artifact }}" class="badge badge-artifact" target="_blank" rel="noopener noreferrer">Artifact</a>
        {% endif %}
        
        {% if pub.doi %}
          <a href="{{ pub.doi }}" class="badge badge-doi" target="_blank" rel="noopener noreferrer">DOI</a>
        {% endif %}
        
        {% if pub.preprint %}
          <a href="{{ pub.preprint }}" class="badge badge-preprint" target="_blank" rel="noopener noreferrer">Preprint</a>
        {% endif %}
      </div>

    </div>
  {% endfor %}
</div>
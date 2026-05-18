---
layout: page
title: People
permalink: /people/
---


<div class="people-grid">
  {% assign sorted_people = site.people | sort: "sorting" %}

  {% for person in sorted_people %}
    <div class="person-card">
      {% if person.image %}
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-image">
      {% else %}
      <img src="{{ '/assets/images/people/silhouette.svg' | relative_url }}" alt="placeholder for profile picture" class="person-image">
      {% endif %}
      
<h4>
  {% if person.link %}
    <a href="{{ person.link }}" target="_blank">{{ person.name }}</a>
  {% else %}
    {{ person.name }}
  {% endif %}
</h4>
      <p class="person-affiliation">{{ person.affiliation }}</p>

      <p class="person-role">{{ person.role }}</p>
      
      {% if person.email %}
        <a href="mailto:{{ person.email }}">Contact</a>
      {% endif %}
      
      <div class="person-bio">
        {{ person.content | markdownify }}
      </div>
    </div>
  {% endfor %}
</div>
---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---

# Promt: Probably the Best Moment to Terminate

Promt is a <a href="https://www.wwtf.at/funding/programmes/ict/ICT25-017/">WWTF</a> funded project, aiming to answer fundamental algorithmic questions related to verification of probabilistic programs. It is a joint project between <a href="https://ista.ac.at/de/forschung/chatterjee-gruppe/">IST Austria</a> and the <a href="https://forsyte.at/">FORSYTE</a> and <a href="https://trustcps.eu/">WWTF</a> groups from TU Wien. The project is split into three workpackages, each led by a principal investigator from one of the groups.

## Workpackages

<div class="wp-list">
  {% assign sorted_wps = site.workpackages | sort: "number" %}
  
  {% for wp in sorted_wps %}
    <details class="wp-card">
      
      <summary class="wp-summary">
        
        <div class="wp-logo">
          WP{{ wp.number }}
        </div>
        
        <div class="wp-summary-info">
          <h3>{{ wp.title }}</h3>
          
          {% if wp.leader %}
            <p class="wp-leader"><strong>Lead:</strong> {{ wp.leader }}</p>
          {% endif %}
        </div>
        
      </summary>
      
      <div class="wp-expanded-content">
        {{ wp.content | markdownify }}
      </div>

    </details>
  {% endfor %}
</div>
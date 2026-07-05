---
layout: page
title: Publications
permalink: /publications/
---

<div class="publication-page">
  <p class="page-intro">
    Selected manuscripts and papers connected to visual-tactile perception, deformable object manipulation, assistive robotics, and robotic cloth manipulation.
  </p>

  <div class="publication-list">
    {% for pub in site.data.publications %}
      <article class="publication-item">
        <img src="{{ pub.image | relative_url }}" alt="{{ pub.title | escape }}" loading="lazy">
        <div>
          <h2><a href="{{ pub.pdf }}">{{ pub.title }}</a></h2>
          <p>{{ pub.authors }}</p>
          <p><em>{{ pub.venue }}</em>, {{ pub.year }}</p>
          <p>{{ pub.abstract }}</p>
          <div class="project-links">
            {% if pub.pdf %}<a href="{{ pub.pdf }}">Paper</a>{% endif %}
            {% if pub.code %}<a href="{{ pub.code }}">Code</a>{% endif %}
            {% if pub.projectpage %}<a href="{{ pub.projectpage }}">Project</a>{% endif %}
          </div>
        </div>
      </article>
    {% endfor %}
  </div>
</div>

<h2 id="publication" class="section-heading">
  <i class="fa-solid fa-file-lines" aria-hidden="true"></i>
  <span>Publication</span>
</h2>

<div class="publication-list">
{% for link in site.data.publications.main %}
  <article class="publication-card">
    {% if link.image %}
    {% assign publication_image = link.image | replace_first: './', '/' %}
    <a class="publication-media" href="{{ link.pdf }}" target="_blank" rel="noopener">
      <img src="{{ publication_image | relative_url }}" class="publication-image" alt="{{ link.title }} preview">
    </a>
    {% endif %}
    <div class="publication-copy">
      <div class="publication-title">{% if link.pdf %}<a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}</div>
      {% if link.conference %}
      <div class="publication-meta">{{ link.conference }}</div>
      {% endif %}
      {% if link.description %}
      <div class="publication-desc">{{ link.description }}</div>
      {% endif %}
      <div class="publication-links">
        {% if link.pdf %}
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">PDF</a>
        {% endif %}
        {% if link.page %}
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Project Page</a>
        {% endif %}
      </div>
    </div>
  </article>
{% endfor %}
</div>

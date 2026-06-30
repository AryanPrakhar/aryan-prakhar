<h2 id="projects" class="section-heading">
  <i class="fa-solid fa-diagram-project" aria-hidden="true"></i>
  <span>Featured Project</span>
</h2>

<div class="feature-list">
{% for project in site.data.projects.main %}
  <article class="feature-card">
    <div class="feature-media">
      {% assign project_image = project.image | replace_first: './', '/' %}
      <img src="{{ project_image | relative_url }}" alt="{{ project.title }} logo" class="feature-image">
    </div>
    <div class="feature-copy">
      <div class="feature-topline">
        <a class="feature-title" href="{{ project.repo }}" target="_blank" rel="noopener">{{ project.title }}</a>
        {% if project.status %}
        <span class="feature-status">[{{ project.status }}]</span>
        {% endif %}
      </div>
      {% if project.subtitle %}
      <div class="feature-subtitle">{{ project.subtitle }}</div>
      {% endif %}
      {% if project.duration %}
      <div class="feature-kicker">{{ project.duration }}</div>
      {% endif %}
      <div class="feature-desc">{{ project.description }}</div>
      {% if project.repo %}
      <div class="feature-links">
        <a href="{{ project.repo }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">GitHub Repo</a>
      </div>
      {% endif %}
    </div>
  </article>
{% endfor %}
</div>

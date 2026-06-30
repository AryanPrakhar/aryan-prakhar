<h2 id="projects" style="margin: 2px 0px -15px;">Featured Project</h2>

<div class="entry-list" style="margin-top: 20px;">
{% for project in site.data.projects.main %}
  <div class="entry-card">
    <div class="entry-media">
      <img src="{{ project.image }}" alt="{{ project.title }} logo" class="entry-image entry-image-plain">
    </div>
    <div class="entry-copy">
      <div class="entry-heading">
        <div class="entry-title">
          {% if project.repo %}<a href="{{ project.repo }}" target="_blank" rel="noopener">{{ project.title }}</a>{% else %}{{ project.title }}{% endif %}
        </div>
        {% if project.status %}
        <div class="entry-status" aria-label="Project status: {{ project.status }}">
          <span class="entry-status-dot" aria-hidden="true"></span>
          <span>[{{ project.status }}]</span>
        </div>
        {% endif %}
      </div>
      {% if project.subtitle %}
      <div class="entry-meta">{{ project.subtitle }}</div>
      {% endif %}
      {% if project.duration %}
      <div class="entry-kicker">{{ project.duration }}</div>
      {% endif %}
      <div class="entry-desc">{{ project.description }}</div>
      {% if project.repo %}
      <div class="links" style="margin-top: 8px;">
        <a href="{{ project.repo }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">GitHub Repo</a>
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

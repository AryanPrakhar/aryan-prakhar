<h2 id="experience" class="section-heading">
  <i class="fa-solid fa-briefcase" aria-hidden="true"></i>
  <span>Experience</span>
</h2>

<div class="entry-list">
{% for company in site.data.industry.main %}
  <div class="entry-card">
    {% if company.logo %}
    <div class="entry-media">
      {% assign company_logo = company.logo | replace_first: './', '/' %}
      <img src="{{ company_logo | relative_url }}" alt="{{ company.name }} logo" class="entry-image entry-image-plain">
    </div>
    {% endif %}
    <div class="entry-copy">
      <div class="entry-title">
        {% if company.website %}<a href="{{ company.website }}" target="_blank" rel="noopener">{{ company.name }}</a>{% else %}{{ company.name }}{% endif %}
      </div>
      <div class="entry-meta">{{ company.position }}, {{ company.duration }}</div>
      <div class="entry-desc">{{ company.description }}</div>
      {% if company.project %}
      <div class="links" style="margin-top: 8px;">
        <a href="{{ company.project }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Project</a>
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

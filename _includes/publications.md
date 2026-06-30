<h2 id="publication" style="margin: 2px 0px -15px;">Publication</h2>

<div class="publications" style="margin-top: 20px;">
<ol class="bibliography">
{% for link in site.data.publications.main %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 0;">
    {% if link.image %}
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1 publication-teaser" alt="{{ link.title }} preview">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 0;padding-left: 20px;">
    <div class="title">{% if link.pdf %}<a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>{% else %}{{ link.title }}{% endif %}</div>
    {% if link.conference %}
    <div class="periodical"><em>{{ link.conference }}</em></div>
    {% endif %}
    {% if link.description %}
    <div class="periodical" style="margin-top: 8px;">{{ link.description }}</div>
    {% endif %}
    <div class="links" style="margin-top: 8px;">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Project Page</a>
      {% endif %}
    </div>
  </div>
</div>
</li>
{% endfor %}
</ol>
</div>

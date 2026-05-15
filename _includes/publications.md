<h2 id="publications" class="section-heading publications-heading">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr publication-media">
    {% if link.image %}
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" alt="{{ link.title }} teaser" loading="lazy">
    {% endif %}
    {% if link.conference_short %}
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9 publication-content">
      {% if link.pdf %}
      <div class="title"><a href="{{ link.pdf }}" target="_blank" rel="noopener noreferrer">{{ link.title }}</a></div>
      {% else %}
      <div class="title">{{ link.title }}</div>
      {% endif %}
      <div class="author">{{ link.authors }}</div>
      <div class="periodical">
        <em>{{ link.venue | default: link.conference }}</em>{% if link.year %}, {{ link.year }}{% endif %}{% if link.doi %}, doi:{{ link.doi }}{% endif %}
      </div>
    <div class="links">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">PDF</a>
      {% endif %}
      {% if link.doi %}
      <a href="https://doi.org/{{ link.doi }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">DOI</a>
      {% endif %}
      {% if link.arxiv %}
      <a href="https://arxiv.org/abs/{{ link.arxiv }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">arXiv</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Project Page</a>
      {% endif %}
      {% if link.bibtex %}
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">BibTeX</a>
      {% endif %}
      {% if link.status %}
      <strong class="publication-status">{{ link.status }}</strong>
      {% elsif link.notes %}
      <strong class="publication-status">{{ link.notes }}</strong>
      {% endif %}
      {% if link.others %}
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>

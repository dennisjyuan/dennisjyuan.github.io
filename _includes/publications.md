<h2 id="publications">Publications</h2>

<p class="section-note">Full list, newest first. Also on <a href="{{ site.google_scholar }}" target="_blank" rel="noopener">Google Scholar</a>.</p>

<ol class="pub-list">
{% for paper in site.data.publications.main %}
  <li class="pub{% if paper.highlight %} pub-highlight{% endif %}">
    <div class="pub-title">{{ paper.title }}</div>
    <div class="pub-authors">{{ paper.authors }}</div>
    {% if paper.note %}<div class="pub-note">{{ paper.note }}</div>{% endif %}
    <div class="pub-venue">{{ paper.venue }}, {{ paper.year }}</div>
    {% if paper.links %}
    <div class="pub-links">
      {% for link in paper.links %}<a href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a>{% endfor %}
    </div>
    {% endif %}
  </li>
{% endfor %}
</ol>

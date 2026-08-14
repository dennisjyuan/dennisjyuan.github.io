<h2 id="research">Research</h2>

<div class="themes">
{% for theme in site.data.themes.main %}
  <div class="theme" id="theme-{{ theme.id }}">
    <h3 class="theme-title"><span class="theme-num">{{ forloop.index }}</span>{{ theme.name }}</h3>
    <div class="theme-summary">{{ theme.summary | markdownify }}</div>
    {% assign theme_papers = site.data.publications.main | where: "theme", theme.id %}
    {% if theme_papers.size > 0 %}
    <ul class="theme-papers">
      {% for paper in theme_papers %}
      <li>
        <span class="tp-title">{{ paper.title }}</span>
        <span class="tp-venue">{{ paper.venue_short }} {{ paper.year }}</span>
        {% if paper.links %}
        {% for link in paper.links %}<a class="tp-link" href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a>{% endfor %}
        {% endif %}
      </li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
{% endfor %}
</div>

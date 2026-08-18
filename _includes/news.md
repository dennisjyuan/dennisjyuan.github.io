<h2 id="news">News</h2>

{% if site.data.news.cover.enabled %}
{% assign c = site.data.news.cover %}
<div class="cover-card">
  <div class="cover-art">
    {% if c.link %}<a href="{{ c.link }}" target="_blank" rel="noopener">{% endif %}
    <img src="{{ c.image }}" alt="{{ c.alt }}" loading="lazy">
    {% if c.link %}</a>{% endif %}
  </div>
  <div class="cover-body">
    <div class="cover-heading">{{ c.heading }}</div>
    {% if c.summary %}<p class="cover-summary">{{ c.summary }}</p>{% endif %}
    <p class="cover-credit">{{ c.credit }}</p>
  </div>
</div>
{% endif %}

<ul class="news-list">
{% for item in site.data.news.main %}
  <li{% if forloop.index > 4 %} class="news-extra"{% endif %}>
    <span class="news-date">{{ item.date }}</span>
    <span class="news-text">{{ item.text }}</span>
    {% if item.image %}
    <span class="news-thumb">
      {% if item.image_link %}<a href="{{ item.image_link }}" target="_blank" rel="noopener">{% endif %}
      <img src="{{ item.image }}" alt="{{ item.image_alt }}" loading="lazy">
      {% if item.image_link %}</a>{% endif %}
      {% if item.image_credit %}<span class="thumb-credit">{{ item.image_credit }}</span>{% endif %}
    </span>
    {% endif %}
  </li>
{% endfor %}
</ul>

{% if site.data.news.main.size > 4 %}
<p class="news-toggle"><a href="#news" onclick="document.querySelectorAll('.news-extra').forEach(function(e){e.classList.toggle('news-shown')});this.textContent=(this.textContent.indexOf('more')>-1?'show less':'show more');return false;">show more</a></p>
{% endif %}

<h2 id="news">News</h2>

<ul class="news-list">
{% for item in site.data.news.main %}
  <li{% if forloop.index > 4 %} class="news-extra"{% endif %}>
    <span class="news-date">{{ item.date }}</span>
    <span class="news-text">{{ item.text }}</span>
  </li>
{% endfor %}
</ul>

{% if site.data.news.main.size > 4 %}
<p class="news-toggle"><a href="#news" onclick="document.querySelectorAll('.news-extra').forEach(function(e){e.classList.toggle('news-shown')});this.textContent=(this.textContent.indexOf('more')>-1?'show less':'show more');return false;">show more</a></p>
{% endif %}

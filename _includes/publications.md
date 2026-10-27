<h2 id="publications">Publications</h2>

<p class="section-note">Newest first. Also on <a href="{{ site.google_scholar }}" target="_blank" rel="noopener">Google Scholar</a>.</p>

{% assign selected_papers = site.data.publications.main | where: "selected", true %}
<h3 class="pub-subhead" id="selected-publications">Selected publications</h3>
<p class="section-note">First-author and equal-contribution papers.</p>
{% include pub-list.html papers=selected_papers %}

<h3 class="pub-subhead" id="all-publications">All publications</h3>
{% include pub-list.html papers=site.data.publications.main %}

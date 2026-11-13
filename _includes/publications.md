<h2 id="publications" style="margin: 2px 0px 15px;">Publications</h2>

<div class="publications">
<ol class="bibliography" style="list-style: none; padding-left: 0; margin: 0;">

{% for link in site.data.publications.main %}

<li style="margin-bottom: 1.4em;">
<div class="pub-row">
  {% if link.image or link.conference_short %}
  <div class="col-sm-3 abbr" style="position: relative; padding-right: 15px;">
    {% if link.image %}
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width:100%;">
    {% endif %}
    {% if link.conference_short %}
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  {% endif %}
  <div class="col-sm-9" style="position: relative;">
    <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    {% if link.code or link.page or link.bibtex or link.notes or link.others %}
    <div class="links" style="margin-top: 4px;">
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %}
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %}
      <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %}
      {{ link.others }}
      {% endif %}
    </div>
    {% endif %}
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>

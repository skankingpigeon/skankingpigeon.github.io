# Welcome

## Notebook Directories

{% comment %} Loop through all pages and extract unique folder names {% endcomment %}
{% assign folders = "" | split: "," %}
{% for note in site.pages %}
  {% if note.url contains "/" and note.url != "/" %}
    {% assign parts = note.url | split: "/" %}
    {% if parts.size > 2 %}
      {% assign folder_name = parts[1] | capitalize %}
      {% assign folders = folders | push: folder_name | uniq %}
    {% endif %}
  {% endif %}
{% endfor %}

{% comment %} Display pages grouped under their respective folder headers {% endcomment %}
{% for folder in folders %}
  ### {{ folder }}
  <ul>
  {% for note in site.pages %}
    {% assign parts = note.url | split: "/" %}
    {% assign current_folder = parts[1] | capitalize %}
    {% if current_folder == folder %}
      <li>
        <a href="{{ note.url | relative_url }}">{{ note.title | default: note.name }}</a>
      </li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}

## See installation instructions for:

- [osm-seed](https://github.com/developmentseed/osm-seed)

<!-- Jump to:
{%- for chartmap in site.data.index.entries %}
- [Development Releases: {{ chartmap[0] }}](#development-releases-{{ chartmap[0] | slugify }})
{%- endfor %} -->
## Stable releases

{% for chartmap in site.data.index.entries %}
  {% if site.stableCharts contains chartmap[0] %}
| Version | Date | App. version |
|---------|------|---------------------|
    {%- assign sortedcharts = chartmap[1] | sort: 'created' | reverse -%}
    {%- for chart in sortedcharts -%}
      {%- unless chart.version contains "-" %}
| [{{ chart.version }}]({{ chart.urls[0] }}) | {{ chart.created | date_to_long_string }} | {{ chart.appVersion }} |
      {%- endunless -%}
    {%- endfor %}
  {%- endif %}
{% endfor %}

## Development releases

{% for chartmap in site.data.index.entries %}
| Version | Date | App. version |
|---------|------|---------------------|
  {%- assign sortedcharts = chartmap[1] | sort: 'created' | reverse %}
  {%- for chart in sortedcharts %}
    {%- if chart.version contains "dev" %}
| [{{ chart.version }}]({{ chart.urls[0] }}) | {{ chart.created | date_to_long_string }} | {{ chart.appVersion }} |
    {%- endif -%}
  {%- endfor %}
{% endfor %}

## Other releases

{% for chartmap in site.data.index.entries %}
| Version | Date | App. version |
|---------|------|---------------------|
  {%- assign sortedcharts = chartmap[1] | sort: 'created' | reverse %}
  {%- for chart in sortedcharts %}
    {%- if chart.version contains "-n" %}
| [{{ chart.version }}]({{ chart.urls[0] }}) | {{ chart.created | date_to_long_string }} | {{ chart.appVersion }} |
    {%- endif -%}
  {%- endfor %}
{% endfor %}

---
layout: base
---
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}

<div id="countdown">

{% if site.data.launch.certainty == "TBD" %}

    {% if site.data.launch.launch | minus: nowunix | times: 0.00001157407 > 45 %}
        {% capture launch %}{{ site.data.launch.launch | minus: nowunix | divided_by: 2592000 }}{% endcapture %}
        <h1>L&minus; about {{ launch | split: '.' | first }} months</h1>
        <p>(launch date to be decided)</p>
    {% endif %}
{% endif %}
</div>

Next PSAS launch: <a href="{{ site.data.launch.link }}">{{ site.data.launch.name }}</a>

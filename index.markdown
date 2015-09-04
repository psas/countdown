---
layout: page
title: Launch Countdown
---
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}

<div>

{% if site.data.launch.certainty == "TBD" %}
  <h1>
    {% assign m = site.data.launch.launch | date: "%B" %}
    {% case m %}
      {% when 'January' or 'February' %}Winter
      {% when 'March' or 'April' %}Spring
      {% when 'May' or 'June' %}Early Summer
      {% when 'July' or 'August' or 'September' %}Late Summer
      {% when 'October' %}Fall
      {% when 'November' or 'December' %}Winter
      {% endcase %}
    {{ site.data.launch.launch | date: '%Y'}}</h1>
  <h2 class="warning">Launch Date TBD</h2>
  <div id="countdown">
    <span id="launch" class="count-decoration">L</span><span id="minus" class="count-decoration">&minus;</span><span>?</span>
  </div>
{% elsif site.data.launch.certainty == "NET" %}
  <h3>No Earlier Than:</h3>
  <h1>{{ site.data.launch.launch | date: "%A, %B %-d, %Y" }}</h1>
{% elsif site.data.launch.certainty == "Date" %}
  <h1>Morning of {{ site.data.launch.launch | date: "%A, %B %-d, %Y" }}</h1>
  <div id="countdown">
    <span id="launch" class="count-decoration">L</span><span id="minus" class="count-decoration">&minus;</span><span>1d 12:23:34</span>
  </div>
{% else %}
  <h1>{{ site.data.launch.launch | date: "%H:%M %P %A, %B %-d, %Y" }}</h1>
{% endif %}
</div>

Next PSAS launch: <a href="{{ site.data.launch.link }}">{{ site.data.launch.name }}</a>

[Countdown API Documentation](docs)

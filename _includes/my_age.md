{% assign today = site.time | date: '%s' %}
{% assign start = '1995-09-13' | date: '%s' %}
{% assign seconds = today | minus: start %}

{% assign my_age = seconds | divided_by: 31536000 &}

{% assign today = null %}
{% assign start = null %}
{% assign seconds = null %}

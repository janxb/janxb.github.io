{% assign additional_documents = "" | split: "" %}
{% for file in site.static_files %}
	{% if file.path contains 'static/documents' %}
		{% assign additional_documents = additional_documents | push: file %}
	{% endif %}
{% endfor %}


{% if additional_documents != empty %}
{% for document in additional_documents %}- <a href="{{document.path}}">{{ document.name | replace: "_", "\_<wbr>" }}</a>
{% endfor %}
{% endif %}

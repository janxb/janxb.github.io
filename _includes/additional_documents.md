{% assign additional_documents = "" | split: "" %}
{% for file in site.static_files %}
	{% if file.path contains 'static/documents' %}
		{% assign additional_documents = additional_documents | push: file %}
	{% endif %}
{% endfor %}


{% if additional_documents != empty %}
## Additional Documents
{% for document in additional_documents %}
- <a href="{{document.path}}">{{document.name}}</a>
{% endfor %}
{% endif %}
